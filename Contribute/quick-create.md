---
title: 'Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault | Microsoft Docs'
description: 'Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 27ebd3e348fc231d8b82e6c17f282bd9ca4afb9f
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308821"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a><span data-ttu-id="2da9a-103">Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-103">Quickstart: Set and retrieve a secret from Azure Key Vault</span></span>

<span data-ttu-id="2da9a-104">Ce démarrage rapide vous montre comment stocker un secret dans Key Vault et le récupérer à l’aide d’une application web.</span><span class="sxs-lookup"><span data-stu-id="2da9a-104">This quickstart shows you how to store a secret in Key Vault and how to retrieve it using a Web app.</span></span> <span data-ttu-id="2da9a-105">Pour afficher la valeur du secret, vous devrez exécuter cette procédure sur Azure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-105">To see the secret value you would have to run this on Azure.</span></span> <span data-ttu-id="2da9a-106">Le démarrage rapide utilise des identités de service administrées (MSI) et Node.js</span><span class="sxs-lookup"><span data-stu-id="2da9a-106">The quickstart uses Node.js and Managed service identities (MSIs)</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="2da9a-107">Création d’un coffre de clés.</span><span class="sxs-lookup"><span data-stu-id="2da9a-107">Create a Key Vault.</span></span>
> * <span data-ttu-id="2da9a-108">Stockage d’un secret dans Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2da9a-108">Store a secret in Key Vault.</span></span>
> * <span data-ttu-id="2da9a-109">Récupération d’un secret à partir de Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2da9a-109">Retrieve a secret from Key Vault.</span></span>
> * <span data-ttu-id="2da9a-110">Création d’une application web Azure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-110">Create an Azure Web Application.</span></span>
> * <span data-ttu-id="2da9a-111">[Activation d’identités de service administrées (MSI)](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span><span class="sxs-lookup"><span data-stu-id="2da9a-111">[Enable managed service identities](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).</span></span>
> * <span data-ttu-id="2da9a-112">Octroi des autorisations requises à l’application web pour lire des données venant de Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2da9a-112">Grant the required permissions for the web application to read data from Key vault.</span></span>

<span data-ttu-id="2da9a-113">Avant de procéder, assurez-vous d’être familiarisé avec les [concepts de base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span><span class="sxs-lookup"><span data-stu-id="2da9a-113">Before you proceed make sure that you are familiar with the [basic concepts](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).</span></span>

> [!NOTE]
> <span data-ttu-id="2da9a-114">Pour comprendre pourquoi le tutoriel ci-dessous est la meilleure pratique, il est nécessaire de comprendre certains concepts.</span><span class="sxs-lookup"><span data-stu-id="2da9a-114">To understand why the below tutorial is the best practice we need to understand a few concepts.</span></span> <span data-ttu-id="2da9a-115">Key Vault est un référentiel central pour stocker les secrets par programmation.</span><span class="sxs-lookup"><span data-stu-id="2da9a-115">Key Vault is a central repository to store secrets programmatically.</span></span> <span data-ttu-id="2da9a-116">Mais pour cela, les applications / utilisateurs doivent d’abord s’authentifier sur Key Vault, et donc présenter un secret.</span><span class="sxs-lookup"><span data-stu-id="2da9a-116">But to do so applications / users need to first authenticate to Key Vault i.e. present a secret.</span></span> <span data-ttu-id="2da9a-117">Pour suivre les meilleures pratiques de sécurité, ce premier secret doit faire l’objet d’une rotation périodique.</span><span class="sxs-lookup"><span data-stu-id="2da9a-117">To follow security best practices this first secret needs to be rotated periodically as well.</span></span> <span data-ttu-id="2da9a-118">Mais avec [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), les applications qui s’exécutent dans Azure bénéficient d’une identité administrée automatiquement par Azure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-118">But with [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) applications that run in Azure are given an identity which is automatically managed by Azure.</span></span> <span data-ttu-id="2da9a-119">Cela permet de résoudre le **problème d’introduction de secrets** où les utilisateurs / applications peuvent suivre les meilleures pratiques et n’ont pas à se soucier de la rotation du premier secret</span><span class="sxs-lookup"><span data-stu-id="2da9a-119">This helps solve the **Secret Introduction Problem** where users / applications can follow best practices and not have to worry about rotating the first secret</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2da9a-120">Composants requis</span><span class="sxs-lookup"><span data-stu-id="2da9a-120">Prerequisites</span></span>

<span data-ttu-id="2da9a-121">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="2da9a-121">::: zone pivot="nodejs"</span></span>
* <span data-ttu-id="2da9a-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="2da9a-122">[Node JS](https://nodejs.org/en/) ::: zone-end ::: zone pivot="dotnet"</span></span>
* <span data-ttu-id="2da9a-123">[Visual Studio 2017 version 15.7.3 ou version ultérieure](https://www.microsoft.com/net/download/windows) avec les charges de travail suivantes :</span><span class="sxs-lookup"><span data-stu-id="2da9a-123">[Visual Studio 2017 version 15.7.3 or later](https://www.microsoft.com/net/download/windows) with the following workloads:</span></span>
  * <span data-ttu-id="2da9a-124">Développement web et ASP.NET</span><span class="sxs-lookup"><span data-stu-id="2da9a-124">ASP.NET and web development</span></span>
  * <span data-ttu-id="2da9a-125">Développement multiplateforme .NET Core</span><span class="sxs-lookup"><span data-stu-id="2da9a-125">.NET Core cross-platform development</span></span>
* <span data-ttu-id="2da9a-126">[SDK .NET Core 2.1 ou version ultérieure](https://www.microsoft.com/net/download/windows) :::zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-126">[.NET Core 2.1 SDK or later](https://www.microsoft.com/net/download/windows) ::: zone-end</span></span>
* <span data-ttu-id="2da9a-127">Git ([télécharger](https://git-scm.com/downloads)).</span><span class="sxs-lookup"><span data-stu-id="2da9a-127">Git ([download](https://git-scm.com/downloads)).</span></span>
* <span data-ttu-id="2da9a-128">Un abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-128">An Azure subscription.</span></span> <span data-ttu-id="2da9a-129">Si vous n’avez pas d’abonnement Azure, créez un [compte gratuit](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="2da9a-129">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) before you begin.</span></span>
* <span data-ttu-id="2da9a-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-130">[Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 or later.</span></span> <span data-ttu-id="2da9a-131">Disponible pour Windows, Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="2da9a-131">This is available for Windows, Mac, and Linux.</span></span>

## <a name="login-to-azure"></a><span data-ttu-id="2da9a-132">Connexion à Azure</span><span class="sxs-lookup"><span data-stu-id="2da9a-132">Login to Azure</span></span>

<span data-ttu-id="2da9a-133">Pour vous connecter à Azure à l’aide de l’interface CLI, vous pouvez taper la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2da9a-133">To log in to Azure using the CLI, you can type:</span></span>

```azurecli
az login
```

## <a name="create-resource-group"></a><span data-ttu-id="2da9a-134">Créer un groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="2da9a-134">Create resource group</span></span>

<span data-ttu-id="2da9a-135">Créez un groupe de ressources avec la commande [groupe az create](/cli/azure/group#az-group-create).</span><span class="sxs-lookup"><span data-stu-id="2da9a-135">Create a resource group with the [az group create](/cli/azure/group#az-group-create) command.</span></span> <span data-ttu-id="2da9a-136">Un groupe de ressources Azure est un conteneur logique dans lequel des ressources Azure sont déployées et administrées.</span><span class="sxs-lookup"><span data-stu-id="2da9a-136">An Azure resource group is a logical container into which Azure resources are deployed and managed.</span></span>

<span data-ttu-id="2da9a-137">Sélectionnez un nom de groupe de ressources et renseignez l’espace réservé.</span><span class="sxs-lookup"><span data-stu-id="2da9a-137">Please select a Resource Group name and fill in the placeholder.</span></span>
<span data-ttu-id="2da9a-138">L’exemple suivant crée un groupe de ressources nommé *<YourResourceGroupName>* à l’emplacement *eastus*.</span><span class="sxs-lookup"><span data-stu-id="2da9a-138">The following example creates a resource group named *<YourResourceGroupName>* in the *eastus* location.</span></span>

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="2da9a-139">Le groupe de ressources que vous venez de créer est utilisé tout au long de ce tutoriel.</span><span class="sxs-lookup"><span data-stu-id="2da9a-139">The resource group you just created is used throughout this tutorial.</span></span>

## <a name="create-an-azure-key-vault"></a><span data-ttu-id="2da9a-140">Créer un Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-140">Create an Azure Key Vault</span></span>

<span data-ttu-id="2da9a-141">Ensuite, vous créez un coffre de clés en utilisant le groupe de ressources créé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="2da9a-141">Next you create a Key Vault using the resource group created in the previous step.</span></span> <span data-ttu-id="2da9a-142">Bien que « ContosoKeyVault » soit utilisé comme le nom du coffre de clés dans cet article, vous devez utiliser un nom unique.</span><span class="sxs-lookup"><span data-stu-id="2da9a-142">Although “ContosoKeyVault” is used as the name for the Key Vault throughout this article, you have to use a unique name.</span></span> <span data-ttu-id="2da9a-143">Fournissez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2da9a-143">Provide the following information:</span></span>

* <span data-ttu-id="2da9a-144">Nom du coffre - **Sélectionnez un nom de coffre de clés ici**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-144">Vault name - **Select a Key Vault Name here**.</span></span>
* <span data-ttu-id="2da9a-145">Nom du groupe de ressources - **Sélectionnez un nom de groupe de ressources ici**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-145">Resource group name - **Select a Resource Group Name here**.</span></span>
* <span data-ttu-id="2da9a-146">Emplacement - **USA Est**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-146">The location - **East US**.</span></span>

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

<span data-ttu-id="2da9a-147">À ce stade, votre compte Azure est le seul autorisé à effectuer des opérations sur ce nouveau coffre.</span><span class="sxs-lookup"><span data-stu-id="2da9a-147">At this point, your Azure account is the only one authorized to perform any operations on this new vault.</span></span>

## <a name="add-a-secret-to-key-vault"></a><span data-ttu-id="2da9a-148">Ajouter un secret au coffre de clés</span><span class="sxs-lookup"><span data-stu-id="2da9a-148">Add a secret to key vault</span></span>

<span data-ttu-id="2da9a-149">Nous allons ajouter un secret pour montrer comment cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2da9a-149">We're adding a secret to help illustrate how this works.</span></span> <span data-ttu-id="2da9a-150">Vous pouvez stocker une chaîne de connexion SQL ou toute autre information que vous devez conserver en toute sécurité mais que vous devez rendre disponible à votre application.</span><span class="sxs-lookup"><span data-stu-id="2da9a-150">You could be storing a SQL connection string or any other information that you need to keep securely but make available to your application.</span></span> <span data-ttu-id="2da9a-151">Dans ce tutoriel, le mot de passe sera appelé **AppSecret** et stocke la valeur de **MySecret**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-151">In this tutorial, the password will be called **AppSecret** and will store the value of **MySecret** in it.</span></span>

<span data-ttu-id="2da9a-152">Tapez les commandes ci-dessous pour créer un secret dans Key Vault, appelé **AppSecret** et qui va stocker la valeur **MySecret** :</span><span class="sxs-lookup"><span data-stu-id="2da9a-152">Type the commands below to create a secret in Key Vault called **AppSecret** that will store the value **MySecret**:</span></span>

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

<span data-ttu-id="2da9a-153">Pour afficher sous forme de texte brut la valeur contenue dans le secret :</span><span class="sxs-lookup"><span data-stu-id="2da9a-153">To view the value contained in the secret as plain text:</span></span>

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

<span data-ttu-id="2da9a-154">Cette commande affiche les informations du secret, y compris l’URI.</span><span class="sxs-lookup"><span data-stu-id="2da9a-154">This command shows the secret information including the URI.</span></span> <span data-ttu-id="2da9a-155">Après ces étapes, vous devez avoir un URI pointant vers un secret dans Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2da9a-155">After completing these steps, you should have a URI to a secret in an Azure Key Vault.</span></span> <span data-ttu-id="2da9a-156">Notez ces informations.</span><span class="sxs-lookup"><span data-stu-id="2da9a-156">Write this information down.</span></span> <span data-ttu-id="2da9a-157">Vous en aurez besoin dans une étape ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-157">You need it in a later step.</span></span>

## <a name="clone-the-repo"></a><span data-ttu-id="2da9a-158">Cloner le référentiel</span><span class="sxs-lookup"><span data-stu-id="2da9a-158">Clone the Repo</span></span>

<span data-ttu-id="2da9a-159">Clonez le référentiel afin de créer une copie locale vous permettant de modifier la source en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2da9a-159">Clone the repo in order to make a local copy for you to edit the source by running the following command:</span></span>

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

<span data-ttu-id="2da9a-160">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="2da9a-160">::: zone pivot="nodejs"</span></span>

## <a name="install-dependencies"></a><span data-ttu-id="2da9a-161">Installer des dépendances</span><span class="sxs-lookup"><span data-stu-id="2da9a-161">Install dependencies</span></span>

<span data-ttu-id="2da9a-162">Ici, nous installons les dépendances.</span><span class="sxs-lookup"><span data-stu-id="2da9a-162">Here we install the dependencies.</span></span> <span data-ttu-id="2da9a-163">Exécutez les commandes suivantes cd key-vault-node-quickstart npm install</span><span class="sxs-lookup"><span data-stu-id="2da9a-163">Run the following commands cd key-vault-node-quickstart npm install</span></span>

<span data-ttu-id="2da9a-164">Ce projet a utilisé 2 modules de nœud :</span><span class="sxs-lookup"><span data-stu-id="2da9a-164">This project used 2 node modules:</span></span>

* [<span data-ttu-id="2da9a-165">ms-rest-azure</span><span class="sxs-lookup"><span data-stu-id="2da9a-165">ms-rest-azure</span></span>](https://www.npmjs.com/package/ms-rest-azure) 
* [<span data-ttu-id="2da9a-166">azure-keyvault</span><span class="sxs-lookup"><span data-stu-id="2da9a-166">azure-keyvault</span></span>](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="2da9a-167">Publier l’application web dans Azure</span><span class="sxs-lookup"><span data-stu-id="2da9a-167">Publish the web application to Azure</span></span>

<span data-ttu-id="2da9a-168">Voici les quelques étapes que nous devons faire</span><span class="sxs-lookup"><span data-stu-id="2da9a-168">Below are the few steps we need to do</span></span>

* <span data-ttu-id="2da9a-169">La 1ère étape consiste à créer un plan [Azure App Service](https://azure.microsoft.com/services/app-service/).</span><span class="sxs-lookup"><span data-stu-id="2da9a-169">The 1st step is to create a [Azure App Service](https://azure.microsoft.com/services/app-service/) Plan.</span></span> <span data-ttu-id="2da9a-170">Vous pouvez stocker plusieurs applications web dans ce plan.</span><span class="sxs-lookup"><span data-stu-id="2da9a-170">You can store multiple web apps in this plan.</span></span>

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* <span data-ttu-id="2da9a-171">Nous créons maintenant une application web.</span><span class="sxs-lookup"><span data-stu-id="2da9a-171">Next we create a web app.</span></span> <span data-ttu-id="2da9a-172">Dans l’exemple suivant, remplacez <app_name> par un nom d’application unique (les caractères autorisés sont a-z, 0-9 et -).</span><span class="sxs-lookup"><span data-stu-id="2da9a-172">In the following example, replace <app_name> with a globally unique app name (valid characters are a-z, 0-9, and -).</span></span> <span data-ttu-id="2da9a-173">Le runtime est défini sur NODE|6.9.</span><span class="sxs-lookup"><span data-stu-id="2da9a-173">The runtime is set to NODE|6.9.</span></span> <span data-ttu-id="2da9a-174">Pour afficher tous les runtimes pris en charge, exécutez az webapp list-runtimes</span><span class="sxs-lookup"><span data-stu-id="2da9a-174">To see all supported runtimes, run az webapp list-runtimes</span></span>

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    <span data-ttu-id="2da9a-175">Une fois l’application web créée, Azure CLI affiche une sortie similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="2da9a-175">When the web app has been created, the Azure CLI shows output similar to the following example:</span></span>

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
    <span data-ttu-id="2da9a-176">Accédez à votre application web nouvellement créée et vous devriez voir une application web qui fonctionne.</span><span class="sxs-lookup"><span data-stu-id="2da9a-176">Browse to your newly created web app and you should see a functioning web app.</span></span> <span data-ttu-id="2da9a-177">Remplacez <app_name> par un nom d’application unique.</span><span class="sxs-lookup"><span data-stu-id="2da9a-177">Replace <app_name> with a unique app name.</span></span>

    ```text
    http://<app name>.azurewebsites.net
    ```
    <span data-ttu-id="2da9a-178">La commande ci-dessus crée également une application prenant en charge Git qui vous permet de déployer vers Azure à partir de votre git local.</span><span class="sxs-lookup"><span data-stu-id="2da9a-178">The above command also creates a Git-enabled app which allows you to deploy to azure from your local git.</span></span> 
    <span data-ttu-id="2da9a-179">Le git local est configuré avec l’URL de « https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git »</span><span class="sxs-lookup"><span data-stu-id="2da9a-179">Local git is configured with url of 'https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git'</span></span>

* <span data-ttu-id="2da9a-180">Créer un utilisateur de déploiement Une fois la commande précédente terminée, vous pouvez ajouter un Azure à distance à votre référentiel Git local.</span><span class="sxs-lookup"><span data-stu-id="2da9a-180">Create a deployment user After the previous command is completed you can add add an Azure remote to your local Git repository.</span></span> <span data-ttu-id="2da9a-181">Remplacez <url> par l’URL du Git distant de la section Activer Git pour votre application.</span><span class="sxs-lookup"><span data-stu-id="2da9a-181">Replace <url> with the URL of the Git remote that you got from Enable Git for your app.</span></span>

    ```bash
    git remote add azure <url>
    ```
    
<span data-ttu-id="2da9a-182">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-182">::: zone-end</span></span>

<span data-ttu-id="2da9a-183">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="2da9a-183">::: zone pivot="dotnet"</span></span>
## <a name="open-and-edit-the-solution"></a><span data-ttu-id="2da9a-184">Ouvrir et modifier la solution</span><span class="sxs-lookup"><span data-stu-id="2da9a-184">Open and edit the solution</span></span>

<span data-ttu-id="2da9a-185">Modifiez le fichier program.cs pour exécuter l’exemple avec le nom de votre coffre de clés spécifique :</span><span class="sxs-lookup"><span data-stu-id="2da9a-185">Edit the program.cs file to run the sample with your specific key vault name:</span></span>

1. <span data-ttu-id="2da9a-186">Naviguez jusqu’au dossier key-vault-dotnet-core-quickstart.</span><span class="sxs-lookup"><span data-stu-id="2da9a-186">Browse to the folder key-vault-dotnet-core-quickstart.</span></span>
2. <span data-ttu-id="2da9a-187">Ouvrir le fichier de key-vault-dotnet-core-quickstart.sln dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="2da9a-187">Open the key-vault-dotnet-core-quickstart.sln file in Visual Studio 2017.</span></span>
3. <span data-ttu-id="2da9a-188">Ouvrez le fichier Program.cs et remplacez l’espace réservé *YourKeyVaultName* par le nom de votre coffre de clés créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="2da9a-188">Open the Program.cs file and update the placeholder *YourKeyVaultName* with the name of your key vault that you created earlier.</span></span>

<span data-ttu-id="2da9a-189">Cette solution utilise les bibliothèques NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) et [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).</span><span class="sxs-lookup"><span data-stu-id="2da9a-189">This solution uses [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) and [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet libraries.</span></span>

## <a name="run-the-app"></a><span data-ttu-id="2da9a-190">Exécuter l’application</span><span class="sxs-lookup"><span data-stu-id="2da9a-190">Run the app</span></span>

<span data-ttu-id="2da9a-191">Dans le menu principal de Visual Studio 2017, sélectionnez **Déboguer** > **Démarrer** sans débogage.</span><span class="sxs-lookup"><span data-stu-id="2da9a-191">From the main menu of Visual Studio 2017, select **Debug** > **Start** without debugging.</span></span> <span data-ttu-id="2da9a-192">Lorsque le navigateur s’affiche, accédez à la page **À propos**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-192">When the browser appears, go to the **About** page.</span></span> <span data-ttu-id="2da9a-193">La valeur d’**AppSecret** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2da9a-193">The value for **AppSecret** is displayed.</span></span>

## <a name="publish-the-web-application-to-azure"></a><span data-ttu-id="2da9a-194">Publier l’application web dans Azure</span><span class="sxs-lookup"><span data-stu-id="2da9a-194">Publish the web application to Azure</span></span>

<span data-ttu-id="2da9a-195">Publiez cette application dans Azure pour l’afficher en direct en tant qu’application web, et pour afficher la récupération de la valeur du secret :</span><span class="sxs-lookup"><span data-stu-id="2da9a-195">Publish this app to Azure to see it live as a web app, and to see that you can fetch the secret value:</span></span>

1. <span data-ttu-id="2da9a-196">Dans Visual Studio, sélectionnez le projet **key-vault-dotnet-core-quickstart**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-196">In Visual Studio, select the **key-vault-dotnet-core-quickstart** project.</span></span>
2. <span data-ttu-id="2da9a-197">Sélectionnez **Publier** > **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-197">Select **Publish** > **Start**.</span></span>
3. <span data-ttu-id="2da9a-198">Créer un nouvel **App Service**, puis sélectionnez **Publier**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-198">Create a new **App Service**, and then select **Publish**.</span></span>
4. <span data-ttu-id="2da9a-199">Modifiez le nom de l’application en **keyvaultdotnetcorequickstart**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-199">Change the app name to **keyvaultdotnetcorequickstart**.</span></span>
5. <span data-ttu-id="2da9a-200">Sélectionnez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="2da9a-200">Select **Create**.</span></span>

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
<span data-ttu-id="2da9a-201">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-201">::: zone-end</span></span>

## <a name="enable-managed-service-identities"></a><span data-ttu-id="2da9a-202">Activer les identités de service administrées</span><span class="sxs-lookup"><span data-stu-id="2da9a-202">Enable managed service identities</span></span>

<span data-ttu-id="2da9a-203">Azure Key Vault permet de stocker en toute sécurité des informations d’identification et d’autres clés et secrets, mais votre code doit s’authentifier sur Azure Key Vault pour les récupérer.</span><span class="sxs-lookup"><span data-stu-id="2da9a-203">Azure Key Vault provides a way to securely store credentials and other keys and secrets, but your code needs to authenticate to Azure Key Vault to retrieve them.</span></span> <span data-ttu-id="2da9a-204">Managed Service Identity simplifie la résolution de ce problème en donnant aux services Azure une identité automatiquement administrée dans Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2da9a-204">Managed Service Identity makes this easier by giving Azure services an automatically managed identity in Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="2da9a-205">Vous pouvez utiliser cette identité pour vous authentifier sur n’importe quel service prenant en charge l’authentification Azure AD, y compris Key Vault, sans avoir d’informations d’identification dans votre code.</span><span class="sxs-lookup"><span data-stu-id="2da9a-205">You can use this identity to authenticate to any service that supports Azure AD authentication, including Key Vault, without having any credentials in your code.</span></span>

1. <span data-ttu-id="2da9a-206">Revenez à l’interface Azure CLI.</span><span class="sxs-lookup"><span data-stu-id="2da9a-206">Return to the Azure CLI.</span></span>
2. <span data-ttu-id="2da9a-207">Exécutez la commande assign-identity pour créer l’identité de cette application :</span><span class="sxs-lookup"><span data-stu-id="2da9a-207">Run the assign-identity command to create the identity for this application:</span></span>

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
><span data-ttu-id="2da9a-208">L’exécution de cette commande dans cette procédure revient à accéder au portail et à régler **Managed Service Identity** sur **Activer** dans les propriétés de l’application web.</span><span class="sxs-lookup"><span data-stu-id="2da9a-208">The command in this procedure is the equivalent of going to the portal and switching **Managed service identity** to **On** in the web application properties.</span></span>

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a><span data-ttu-id="2da9a-209">Octroyer des autorisations à votre application pour lire des secrets dans Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-209">Assign permissions to your application to read secrets from Key Vault</span></span>

<span data-ttu-id="2da9a-210">Prenez note de la sortie quand vous publiez l’application dans Azure.</span><span class="sxs-lookup"><span data-stu-id="2da9a-210">Make a note of the output when you publish the application to Azure.</span></span> <span data-ttu-id="2da9a-211">Elle doit être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="2da9a-211">It should be of the format:</span></span>

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

<span data-ttu-id="2da9a-212">Ensuite, exécutez cette commande en utilisant le nom de votre coffre de clés et la valeur de **PrincipalId** :</span><span class="sxs-lookup"><span data-stu-id="2da9a-212">Then, run this command by using the name of your key vault and the value of **PrincipalId**:</span></span>

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

<span data-ttu-id="2da9a-213">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="2da9a-213">::: zone pivot="nodejs"</span></span>
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a><span data-ttu-id="2da9a-214">Déployer l’application Node sur Azure et récupérer la valeur du secret</span><span class="sxs-lookup"><span data-stu-id="2da9a-214">Deploy the Node App to Azure and retrieve the secret value</span></span>

<span data-ttu-id="2da9a-215">Maintenant que tout est configuré.</span><span class="sxs-lookup"><span data-stu-id="2da9a-215">Now that everything is set.</span></span> <span data-ttu-id="2da9a-216">Exécutez la commande suivante pour déployer l’application sur Azure</span><span class="sxs-lookup"><span data-stu-id="2da9a-216">Run the following command to deploy the app to Azure</span></span>

```bash
git push azure master
```

<span data-ttu-id="2da9a-217">Lorsque c’est fait et que vous parcourez https://<app_name>.azurewebsites.net, vous pouvez voir la valeur du secret.</span><span class="sxs-lookup"><span data-stu-id="2da9a-217">After this when you browse https://<app_name>.azurewebsites.net you can see the secret value.</span></span>
<span data-ttu-id="2da9a-218">Assurez-vous d’avoir remplacé le nom <YourKeyVaultName> par le nom de votre coffre</span><span class="sxs-lookup"><span data-stu-id="2da9a-218">Make sure that you replaced the name <YourKeyVaultName> with your vault name</span></span>

<span data-ttu-id="2da9a-219">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-219">::: zone-end</span></span>

<span data-ttu-id="2da9a-220">::: zone pivot="dotnet" Maintenant lorsque vous exécutez l’application, vous devriez voir la valeur de votre secret récupérée.</span><span class="sxs-lookup"><span data-stu-id="2da9a-220">::: zone pivot="dotnet" Now when you run the application, you should see your secret value retrieved.</span></span>
<span data-ttu-id="2da9a-221">::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-221">::: zone-end</span></span>

## <a name="next-steps"></a><span data-ttu-id="2da9a-222">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2da9a-222">Next steps</span></span>

<span data-ttu-id="2da9a-223">::: zone pivot="nodejs"</span><span class="sxs-lookup"><span data-stu-id="2da9a-223">::: zone pivot="nodejs"</span></span>
* [<span data-ttu-id="2da9a-224">Page d'accueil d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-224">Azure Key Vault Home Page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="2da9a-225">Documentation d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-225">Azure Key Vault Documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="2da9a-226">SDK Azure pour Node</span><span class="sxs-lookup"><span data-stu-id="2da9a-226">Azure SDK For Node</span></span>](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* <span data-ttu-id="2da9a-227">[Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-227">[Azure REST API Reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>

<span data-ttu-id="2da9a-228">::: zone pivot="dotnet"</span><span class="sxs-lookup"><span data-stu-id="2da9a-228">::: zone pivot="dotnet"</span></span>
* [<span data-ttu-id="2da9a-229">Page d'accueil d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-229">Azure Key Vault home page</span></span>](https://azure.microsoft.com/services/key-vault/)
* [<span data-ttu-id="2da9a-230">Documentation d’Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2da9a-230">Azure Key Vault documentation</span></span>](https://docs.microsoft.com/azure/key-vault/)
* [<span data-ttu-id="2da9a-231">SDK Azure pour .NET</span><span class="sxs-lookup"><span data-stu-id="2da9a-231">Azure SDK For .NET</span></span>](https://github.com/Azure/azure-sdk-for-net)
* <span data-ttu-id="2da9a-232">[Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span><span class="sxs-lookup"><span data-stu-id="2da9a-232">[Azure REST API reference](https://docs.microsoft.com/rest/api/keyvault/) ::: zone-end</span></span>
