---
title: 'Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault | Microsoft Docs'
description: 'Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages, keyvault-platforms
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 8b758274203748bb6e04c03dec5de38fb77947b4
ms.sourcegitcommit: b0105f322f91bb4dbde47f6da35b3c12271d5b03
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43239502"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="4585e-103">Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="4585e-104">Ce démarrage rapide vous montre comment stocker un secret dans Key Vault et le récupérer à l’aide d’une application web.</span><span class="sxs-lookup"><span data-stu-id="4585e-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="4585e-105">Pour afficher la valeur du secret, vous devrez exécuter cette procédure sur Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="4585e-106">Le démarrage rapide utilise des identités de service administrées (MSI) et Node.js</span><span class="sxs-lookup"><span data-stu-id="4585e-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="4585e-107">Création d’un coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="4585e-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="4585e-108">Stockage d’un secret dans Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="4585e-109">Récupération d’un secret à partir de Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="4585e-110">Création d’une application web Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="4585e-111">[Activation d’identités de service administrées (MSI)](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="4585e-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="4585e-112">Octroi des autorisations requises à l’application web pour lire des données venant de Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="4585e-113">Avant de procéder, assurez-vous d’être familiarisé avec les [concepts de base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="4585e-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

>[!NOTE]
<span data-ttu-id="4585e-114">Pour comprendre pourquoi le tutoriel ci-dessous est la meilleure pratique, il est nécessaire de comprendre certains concepts.</span><span class="sxs-lookup"><span data-stu-id="4585e-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="4585e-115">Key Vault est un référentiel central pour stocker les secrets par programmation.</span><span class="sxs-lookup"><span data-stu-id="4585e-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="4585e-116">Mais pour cela, les applications / utilisateurs doivent d’abord s’authentifier sur Key Vault, et donc présenter un secret.</span><span class="sxs-lookup"><span data-stu-id="4585e-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="4585e-117">Pour suivre les meilleures pratiques de sécurité, ce premier secret doit faire l’objet d’une rotation périodique.</span><span class="sxs-lookup"><span data-stu-id="4585e-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="4585e-118">Mais avec [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), les applications qui s’exécutent dans Azure bénéficient d’une identité administrée automatiquement par Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="4585e-119">Cela permet de résoudre le **problème d’introduction de secrets** où les utilisateurs / applications peuvent suivre les meilleures pratiques et n’ont pas à se soucier de la rotation du premier secret</span><span class="sxs-lookup"><span data-stu-id="4585e-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4585e-120">Composants requis</span><span class="sxs-lookup"><span data-stu-id="4585e-120">Prerequisites</span></span>

<span data-ttu-id="4585e-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="4585e-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="4585e-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-122">[Node JS](https://nodejs.org/en/) ::: zone-end</span></span>

<span data-ttu-id="4585e-123">::: zone pivot="dotnet, windows"</span><span class="sxs-lookup"><span data-stu-id="4585e-123">::: zone pivot="dotnet, windows"</span></span>
* <span data-ttu-id="4585e-124">[Visual Studio 2017 version 15.7.3 ou version ultérieure](https://www.microsoft.com/net/download/windows) avec les charges de travail suivantes :</span><span class="sxs-lookup"><span data-stu-id="4585e-124">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="4585e-125">Développement web et ASP.NET</span><span class="sxs-lookup"><span data-stu-id="4585e-125">ASP.NET and web development</span></span>
  * <span data-ttu-id="4585e-126">Développement multiplateforme .NET Core</span><span class="sxs-lookup"><span data-stu-id="4585e-126">.NET Core cross-platform development</span></span>
* <span data-ttu-id="4585e-127">[SDK .NET Core 2.1 ou version ultérieure](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-127">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) :::zone-end</span></span>

<span data-ttu-id="4585e-128">::: zone pivot="dotnet, mac"</span><span class="sxs-lookup"><span data-stu-id="4585e-128">::: zone pivot="dotnet, mac"</span></span>
* <span data-ttu-id="4585e-129">Consultez [les nouveautés de Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/).</span><span class="sxs-lookup"><span data-stu-id="4585e-129">See [What’s New in Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/).</span></span>
<span data-ttu-id="4585e-130">:::zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-130">:::zone-end</span></span>

* <span data-ttu-id="4585e-131">Git ([télécharger](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="4585e-131">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="4585e-132">Un abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-132">An Azure subscription.</span></span> <span data-ttu-id="4585e-133">Si vous n’avez pas d’abonnement Azure, créez un [compte gratuit](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="4585e-133">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="4585e-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4585e-134">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="4585e-135">Disponible pour Windows, Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="4585e-135">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="4585e-136">Connexion à Azure</span><span class="sxs-lookup"><span data-stu-id="4585e-136">Login to Azure</span></span>

<span data-ttu-id="4585e-137">Pour vous connecter à Azure à l’aide de l’interface CLI, vous pouvez taper la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4585e-137">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="4585e-138">Créer un groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="4585e-138">Create resource group</span></span>

<span data-ttu-id="4585e-139">Créez un groupe de ressources avec la commande [groupe az create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="4585e-139">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="4585e-140">Un groupe de ressources Azure est un conteneur logique dans lequel des ressources Azure sont déployées et administrées.</span><span class="sxs-lookup"><span data-stu-id="4585e-140">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="4585e-141">Sélectionnez un nom de groupe de ressources et renseignez l’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="4585e-141">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="4585e-142">L’exemple suivant crée un groupe de ressources nommé *<YourResourceGroupName>* à l’emplacement *eastus*.</span><span class="sxs-lookup"><span data-stu-id="4585e-142">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="4585e-143">Le groupe de ressources que vous venez de créer est utilisé tout au long de ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="4585e-143">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="4585e-144">Créer un Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-144">Create an Azure Key Vault</span></span>

<span data-ttu-id="4585e-145">Ensuite, vous créez un coffre de clés en utilisant le groupe de ressources créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="4585e-145">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="4585e-146">Bien que « ContosoKeyVault » soit utilisé comme le nom du coffre de clés dans cet article, vous devez utiliser un nom unique.</span><span class="sxs-lookup"><span data-stu-id="4585e-146">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="4585e-147">Fournissez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4585e-147">Provide the following information:</span></span>

* <span data-ttu-id="4585e-148">Nom du coffre - **Sélectionnez un nom de coffre de clés ici**.</span><span class="sxs-lookup"><span data-stu-id="4585e-148">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="4585e-149">Nom du groupe de ressources - **Sélectionnez un nom de groupe de ressources ici**.</span><span class="sxs-lookup"><span data-stu-id="4585e-149">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="4585e-150">Emplacement - **USA Est**.</span><span class="sxs-lookup"><span data-stu-id="4585e-150">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="4585e-151">À ce stade, votre compte Azure est le seul autorisé à effectuer des opérations sur ce nouveau coffre.</span><span class="sxs-lookup"><span data-stu-id="4585e-151">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="4585e-152">Ajouter un secret au coffre de clés</span><span class="sxs-lookup"><span data-stu-id="4585e-152">Add a secret to key vault</span></span>

<span data-ttu-id="4585e-153">Nous allons ajouter un secret pour montrer comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="4585e-153">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="4585e-154">Vous pouvez stocker une chaîne de connexion SQL ou toute autre information que vous devez conserver en toute sécurité mais que vous devez rendre disponible à votre application.</span><span class="sxs-lookup"><span data-stu-id="4585e-154">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="4585e-155">Dans ce tutoriel, le mot de passe sera appelé **AppSecret** et stocke la valeur de **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="4585e-155">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="4585e-156">Tapez les commandes ci-dessous pour créer un secret dans Key Vault, appelé **AppSecret** et qui va stocker la valeur **MySecret** :</span><span class="sxs-lookup"><span data-stu-id="4585e-156">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="4585e-157">Pour afficher sous forme de texte brut la valeur contenue dans le secret :</span><span class="sxs-lookup"><span data-stu-id="4585e-157">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="4585e-158">Cette commande affiche les informations du secret, y compris l’URI.</span><span class="sxs-lookup"><span data-stu-id="4585e-158">This command shows the secret information including the URI.</span></span> <span data-ttu-id="4585e-159">Après ces étapes, vous devez avoir un URI pointant vers un secret dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4585e-159">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="4585e-160">Notez ces informations.</span><span class="sxs-lookup"><span data-stu-id="4585e-160">Write this information down.</span></span> <span data-ttu-id="4585e-161">Vous en aurez besoin dans une étape ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4585e-161">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="4585e-162">Cloner le référentiel</span><span class="sxs-lookup"><span data-stu-id="4585e-162">Clone the Repo</span></span>

<span data-ttu-id="4585e-163">Clonez le référentiel afin de créer une copie locale vous permettant de modifier la source en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4585e-163">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="4585e-164">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="4585e-164">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="4585e-165">Installer des dépendances</span><span class="sxs-lookup"><span data-stu-id="4585e-165">Install dependencies</span></span>

<span data-ttu-id="4585e-166">Ici, nous installons les dépendances.</span><span class="sxs-lookup"><span data-stu-id="4585e-166">Here we install the dependencies.</span></span> <span data-ttu-id="4585e-167">Exécutez les commandes suivantes cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="4585e-167">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="4585e-168">Ce projet a utilisé 2 modules de nœud :</span><span class="sxs-lookup"><span data-stu-id="4585e-168">This project used 2 node modules:</span></span>

* [<span data-ttu-id="4585e-169">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="4585e-169">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="4585e-170">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="4585e-170">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="4585e-171">Publier l’application web dans Azure</span><span class="sxs-lookup"><span data-stu-id="4585e-171">Publish the web application to Azure</span></span>

<span data-ttu-id="4585e-172">Voici les quelques étapes que nous devons faire</span><span class="sxs-lookup"><span data-stu-id="4585e-172">Below are the few steps we need to do</span></span>

* <span data-ttu-id="4585e-173">La 1ère étape consiste à créer un plan [Azure App Service](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="4585e-173">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="4585e-174">Vous pouvez stocker plusieurs applications web dans ce plan.</span><span class="sxs-lookup"><span data-stu-id="4585e-174">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="4585e-175">Nous créons maintenant une application web.</span><span class="sxs-lookup"><span data-stu-id="4585e-175">Next we create a web app.</span></span> <span data-ttu-id="4585e-176">Dans l’exemple suivant, remplacez <app_name> par un nom d’application unique (les caractères autorisés sont a-z, 0-9 et -).</span><span class="sxs-lookup"><span data-stu-id="4585e-176">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="4585e-177">Le runtime est défini sur NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="4585e-177">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="4585e-178">Pour afficher tous les runtimes pris en charge, exécutez az webapp list-runtimes</span><span class="sxs-lookup"><span data-stu-id="4585e-178">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="4585e-179">Une fois l’application web créée, Azure CLI affiche une sortie similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="4585e-179">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    <span data-ttu-id="4585e-180">Accédez à votre application web nouvellement créée et vous devriez voir une application web qui fonctionne.</span><span class="sxs-lookup"><span data-stu-id="4585e-180">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="4585e-181">Remplacez <app_name> par un nom d’application unique.</span><span class="sxs-lookup"><span data-stu-id="4585e-181">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="4585e-182">La commande ci-dessus crée également une application prenant en charge Git qui vous permet de déployer vers Azure à partir de votre git local.</span><span class="sxs-lookup"><span data-stu-id="4585e-182">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="4585e-183">Le git local est configuré avec l’URL de « https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git »</span><span class="sxs-lookup"><span data-stu-id="4585e-183">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="4585e-184">Créer un utilisateur de déploiement Une fois la commande précédente terminée, vous pouvez ajouter un Azure à distance à votre référentiel Git local.</span><span class="sxs-lookup"><span data-stu-id="4585e-184">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="4585e-185">Remplacez <url> par l’URL du Git distant de la section Activer Git pour votre application.</span><span class="sxs-lookup"><span data-stu-id="4585e-185">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
<span data-ttu-id="4585e-186">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-186">::: zone-end</span></span>

<span data-ttu-id="4585e-187">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="4585e-187">::: zone pivot="dotnet"</span></span>

## <a name="open-and-edit-the-solution"></a><span data-ttu-id="4585e-188">Ouvrir et modifier la solution</span><span class="sxs-lookup"><span data-stu-id="4585e-188">Open and edit the solution</span></span>

<span data-ttu-id="4585e-189">Modifiez le fichier program.cs pour exécuter l’exemple avec le nom de votre coffre de clés spécifique :</span><span class="sxs-lookup"><span data-stu-id="4585e-189">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="4585e-190">Naviguez jusqu’au dossier key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="4585e-190">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="4585e-191">Ouvrir le fichier de key-vault-dotnet-core-quickstart.sln dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="4585e-191">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="4585e-192">Ouvrez le fichier Program.cs et remplacez l’espace réservé *YourKeyVaultName* par le nom de votre coffre de clés créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="4585e-192">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="4585e-193">Cette solution utilise les bibliothèques NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) et [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="4585e-193">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="4585e-194">Exécuter l’application</span><span class="sxs-lookup"><span data-stu-id="4585e-194">Run the app</span></span>

<span data-ttu-id="4585e-195">Dans le menu principal de Visual Studio 2017, sélectionnez **Déboguer** > **Démarrer** sans débogage.</span><span class="sxs-lookup"><span data-stu-id="4585e-195">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="4585e-196">Lorsque le navigateur s’affiche, accédez à la page **À propos**.</span><span class="sxs-lookup"><span data-stu-id="4585e-196">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="4585e-197">La valeur d’**AppSecret** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4585e-197">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="4585e-198">Publier l’application web dans Azure</span><span class="sxs-lookup"><span data-stu-id="4585e-198">Publish the web application to Azure</span></span>

<span data-ttu-id="4585e-199">Publiez cette application dans Azure pour l’afficher en direct en tant qu’application web, et pour afficher la récupération de la valeur du secret :</span><span class="sxs-lookup"><span data-stu-id="4585e-199">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="4585e-200">Dans Visual Studio, sélectionnez le projet **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="4585e-200">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="4585e-201">Sélectionnez **Publier** > **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="4585e-201">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="4585e-202">Créer un nouvel **App Service**, puis sélectionnez **Publier**.</span><span class="sxs-lookup"><span data-stu-id="4585e-202">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="4585e-203">Modifiez le nom de l’application en **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="4585e-203">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="4585e-204">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="4585e-204">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]

<span data-ttu-id="4585e-205">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-205">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="4585e-206">Activer les identités de service administrées</span><span class="sxs-lookup"><span data-stu-id="4585e-206">Enable managed service identities</span></span>

<span data-ttu-id="4585e-207">Azure Key Vault permet de stocker en toute sécurité des informations d’identification et d’autres clés et secrets, mais votre code doit s’authentifier sur Azure Key Vault pour les récupérer.</span><span class="sxs-lookup"><span data-stu-id="4585e-207">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="4585e-208">Managed Service Identity simplifie la résolution de ce problème en donnant aux services Azure une identité automatiquement administrée dans Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4585e-208">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="4585e-209">Vous pouvez utiliser cette identité pour vous authentifier sur n’importe quel service prenant en charge l’authentification Azure AD, y compris Key Vault, sans avoir d’informations d’identification dans votre code.</span><span class="sxs-lookup"><span data-stu-id="4585e-209">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="4585e-210">Revenez à l’interface Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="4585e-210">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="4585e-211">Exécutez la commande assign-identity pour créer l’identité de cette application :</span><span class="sxs-lookup"><span data-stu-id="4585e-211">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="4585e-212">L’exécution de cette commande dans cette procédure revient à accéder au portail et à régler **Managed Service Identity** sur **Activer** dans les propriétés de l’application web.</span><span class="sxs-lookup"><span data-stu-id="4585e-212">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="4585e-213">Octroyer des autorisations à votre application pour lire des secrets dans Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-213">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="4585e-214">Prenez note de la sortie quand vous publiez l’application dans Azure.</span><span class="sxs-lookup"><span data-stu-id="4585e-214">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="4585e-215">Elle doit être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="4585e-215">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="4585e-216">Ensuite, exécutez cette commande en utilisant le nom de votre coffre de clés et la valeur de **PrincipalId** :</span><span class="sxs-lookup"><span data-stu-id="4585e-216">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="4585e-217">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="4585e-217">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="4585e-218">Déployer l’application Node sur Azure et récupérer la valeur du secret</span><span class="sxs-lookup"><span data-stu-id="4585e-218">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="4585e-219">Maintenant que tout est configuré.</span><span class="sxs-lookup"><span data-stu-id="4585e-219">Now that everything is set.</span></span> <span data-ttu-id="4585e-220">Exécutez la commande suivante pour déployer l’application sur Azure</span><span class="sxs-lookup"><span data-stu-id="4585e-220">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="4585e-221">Lorsque c’est fait et que vous parcourez https://<app_name>.azurewebsites.net, vous pouvez voir la valeur du secret.</span><span class="sxs-lookup"><span data-stu-id="4585e-221">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="4585e-222">Assurez-vous d’avoir remplacé le nom <YourKeyVaultName> par le nom de votre coffre ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-222">Make sure that you replaced the name <YourKeyVaultName> with your vault name ::: zone-end</span></span>

<span data-ttu-id="4585e-223">::: zone pivot="dotnet" Maintenant lorsque vous exécutez l’application, vous devriez voir la valeur de votre secret récupérée.</span><span class="sxs-lookup"><span data-stu-id="4585e-223">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="4585e-224">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-224">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="4585e-225">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4585e-225">Next steps</span></span>

<span data-ttu-id="4585e-226">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="4585e-226">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="4585e-227">Page d'accueil d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-227">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="4585e-228">Documentation d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-228">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="4585e-229">SDK Azure pour Node</span><span class="sxs-lookup"><span data-stu-id="4585e-229">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="4585e-230">[Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-230">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="4585e-231">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="4585e-231">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="4585e-232">Page d'accueil d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-232">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="4585e-233">Documentation d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="4585e-233">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="4585e-234">SDK Azure pour .NET</span><span class="sxs-lookup"><span data-stu-id="4585e-234">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="4585e-235">[Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="4585e-235">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>