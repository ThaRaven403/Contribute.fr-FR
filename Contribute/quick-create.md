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
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805737"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>Démarrage rapide : définir et récupérer un secret depuis Azure Key Vault à l’aide d’Azure Key Vault

Ce démarrage rapide vous montre comment stocker un secret dans Key Vault et le récupérer à l’aide d’une application web. Pour afficher la valeur du secret, vous devrez exécuter cette procédure sur Azure. Le guide de démarrage rapide utilise des identités de service administrées (MSI) et Node.js.

> [!div class="checklist"]
> * Création d’un coffre de clés.
> * Stockage d’un secret dans le coffre de clés.
> * Récupération d’un secret à partir de Key Vault.
> * Création d’une application web Azure.
> * [Activation d’identités de service administrées (MSI)](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview).
> * Octroi des autorisations requises à l’application web pour lire des données venant de Key Vault.

Avant de procéder, assurez-vous d’être familiarisé avec les [concepts de base](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts).

> [!NOTE]
> Pour comprendre pourquoi le tutoriel ci-dessous est la meilleure pratique, il est nécessaire de comprendre certains concepts. Key Vault est un référentiel central pour stocker les secrets par programmation. Mais pour cela, les applications / utilisateurs doivent d’abord s’authentifier sur Key Vault, et donc présenter un secret. Pour suivre les meilleures pratiques de sécurité, ce premier secret doit faire l’objet d’une rotation périodique. Mais avec [Managed Service Identity](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview), les applications qui s’exécutent dans Azure bénéficient d’une identité administrée automatiquement par Azure. Cela permet de résoudre le **problème d’introduction de secrets** où les utilisateurs / applications peuvent suivre les meilleures pratiques et n’ont pas à se soucier de la rotation du premier secret

## <a name="prerequisites"></a>Composants requis

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* [Visual Studio 2017 version 15.7.3 ou version ultérieure](https://www.microsoft.com/net/download/windows) avec les charges de travail suivantes :
  * Développement web et ASP.NET
  * Développement multiplateforme .NET Core
* [SDK .NET Core 2.1 ou version ultérieure](https://www.microsoft.com/net/download/windows)
::: zone-end
* Git ([télécharger](https://git-scm.com/downloads)).
* Un abonnement Azure. Si vous n’avez pas d’abonnement Azure, créez un [compte gratuit](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) avant de commencer.
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) version 2.0.4 ou ultérieure. Disponible pour Windows, Mac et Linux.

## <a name="login-to-azure"></a>Connexion à Azure

Pour vous connecter à Azure à l’aide de l’interface CLI, vous pouvez taper la commande suivante :

```azurecli
az login
```

## <a name="create-resource-group"></a>Créer un groupe de ressources

Créez un groupe de ressources avec la commande [groupe az create](/cli/azure/group#az-group-create). Un groupe de ressources Azure est un conteneur logique dans lequel des ressources Azure sont déployées et administrées.

Sélectionnez un nom de groupe de ressources et renseignez l’espace réservé.
L’exemple suivant crée un groupe de ressources nommé *<YourResourceGroupName>* à l’emplacement *eastus*.

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

Le groupe de ressources que vous venez de créer est utilisé tout au long de ce tutoriel.

## <a name="create-an-azure-key-vault"></a>Créer un Azure Key Vault

Ensuite, vous créez un coffre de clés en utilisant le groupe de ressources créé à l’étape précédente. Bien que « ContosoKeyVault » soit utilisé comme le nom du coffre de clés dans cet article, vous devez utiliser un nom unique. Fournissez les informations suivantes :

* Nom du coffre - **Sélectionnez un nom de coffre de clés ici**.
* Nom du groupe de ressources - **Sélectionnez un nom de groupe de ressources ici**.
* Emplacement - **USA Est**.

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

À ce stade, votre compte Azure est le seul autorisé à effectuer des opérations sur ce nouveau coffre.

## <a name="add-a-secret-to-key-vault"></a>Ajouter un secret au coffre de clés

Nous allons ajouter un secret pour montrer comment cela fonctionne. Vous pouvez stocker une chaîne de connexion SQL ou toute autre information que vous devez conserver en toute sécurité mais que vous devez rendre disponible à votre application. Dans ce tutoriel, le mot de passe sera appelé **AppSecret** et stocke la valeur de **MySecret**.

Tapez les commandes ci-dessous pour créer un secret dans Key Vault, appelé **AppSecret** et qui va stocker la valeur **MySecret** :

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

Pour afficher sous forme de texte brut la valeur contenue dans le secret :

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

Cette commande affiche les informations du secret, y compris l’URI. Après ces étapes, vous devez avoir un URI pointant vers un secret dans Azure Key Vault. Notez ces informations. Vous en aurez besoin dans une étape ultérieure.

## <a name="clone-the-repo"></a>Cloner le référentiel

Clonez le référentiel afin de créer une copie locale vous permettant de modifier la source en exécutant la commande suivante :

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>Installer des dépendances

Ici, nous installons les dépendances. Exécutez les commandes suivantes :

    cd key-vault-node-quickstart
    npm install

Ce projet a utilisé 2 modules de nœud :

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Publier l’application web dans Azure

Voici les quelques étapes que nous devons suivre pour publier l’application sur Azure.

* La 1ère étape consiste à créer un plan [Azure App Service](https://azure.microsoft.com/services/app-service/). Vous pouvez stocker plusieurs applications web dans ce plan.

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* Nous créons maintenant une application web. Dans l’exemple suivant, remplacez <app_name> par un nom d’application unique (les caractères autorisés sont a-z, 0-9 et -). Le runtime est défini sur NODE|6.9. Pour voir tous les runtimes, exécutez `az webapp list-runtimes`.

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Une fois l’application web créée, Azure CLI affiche une sortie similaire à l’exemple suivant :

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
    Accédez à votre application web nouvellement créée et vous devriez voir une application web qui fonctionne. Remplacez <app_name> par un nom d’application unique.

    ```text
    http://<app name>.azurewebsites.net
    ```
    La commande ci-dessus crée également une application prenant en charge Git qui vous permet de déployer vers Azure à partir de votre git local. 
    Le git local est configuré avec l’URL de « https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git »

* Créer un utilisateur de déploiement Une fois la commande précédente terminée, vous pouvez ajouter un Azure à distance à votre dépôt Git local. Remplacez <url> par l’URL du Git distant de la section Activer Git pour votre application.

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>Ouvrir et modifier la solution

Modifiez le fichier program.cs pour exécuter l’exemple avec le nom de votre coffre de clés spécifique :

1. Naviguez jusqu’au dossier key-vault-dotnet-core-quickstart.
2. Ouvrir le fichier de key-vault-dotnet-core-quickstart.sln dans Visual Studio 2017.
3. Ouvrez le fichier Program.cs et remplacez l’espace réservé *YourKeyVaultName* par le nom de votre coffre de clés créé précédemment.

Cette solution utilise les bibliothèques NuGet [AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) et [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault).

## <a name="run-the-app"></a>Exécuter l’application

Dans le menu principal de Visual Studio 2017, sélectionnez **Déboguer** > **Démarrer** sans débogage. Lorsque le navigateur s’affiche, accédez à la page **À propos**. La valeur d’**AppSecret** s’affiche.

## <a name="publish-the-web-application-to-azure"></a>Publier l’application web dans Azure

Publiez cette application dans Azure pour l’afficher en direct en tant qu’application web, et pour afficher la récupération de la valeur du secret :

1. Dans Visual Studio, sélectionnez le projet **key-vault-dotnet-core-quickstart**.
2. Sélectionnez **Publier** > **Démarrer**.
3. Créer un nouvel **App Service**, puis sélectionnez **Publier**.
4. Modifiez le nom de l’application en **keyvaultdotnetcorequickstart**.
5. Sélectionnez **Créer**.

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>Activer les identités de service administrées

Azure Key Vault permet de stocker en toute sécurité des informations d’identification et d’autres clés et secrets, mais votre code doit s’authentifier sur Azure Key Vault pour les récupérer. Managed Service Identity simplifie la résolution de ce problème en donnant aux services Azure une identité automatiquement administrée dans Azure Active Directory (Azure AD). Vous pouvez utiliser cette identité pour vous authentifier sur n’importe quel service prenant en charge l’authentification Azure AD, y compris Key Vault, sans avoir d’informations d’identification dans votre code.

1. Revenez à l’interface Azure CLI.
2. Exécutez la commande assign-identity pour créer l’identité de cette application :

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>L’exécution de cette commande dans cette procédure revient à accéder au portail et à régler **Managed Service Identity** sur **Activer** dans les propriétés de l’application web.

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>Octroyer des autorisations à votre application pour lire des secrets dans Key Vault

Prenez note de la sortie quand vous publiez l’application dans Azure. Elle doit être au format suivant :

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

Ensuite, exécutez cette commande en utilisant le nom de votre coffre de clés et la valeur de **PrincipalId** :

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Déployer l’application Node sur Azure et récupérer la valeur du secret

Maintenant que tout est configuré. Exécutez la commande suivante pour déployer l’application sur Azure

```bash
git push azure master
```

Lorsque c’est fait et que vous parcourez https://<app_name>.azurewebsites.net, vous pouvez voir la valeur du secret.
Assurez-vous d’avoir remplacé le nom <YourKeyVaultName> par le nom de votre coffre

::: zone-end

::: zone pivot="dotnet"
Maintenant, quand vous exécutez l’application, vous devriez voir la valeur du secret récupérée.
::: zone-end

## <a name="next-steps"></a>Étapes suivantes

::: zone pivot="nodejs"
* [Page d'accueil d’Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentation d’Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [SDK Azure pour Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Page d'accueil d’Azure Key Vault](https://azure.microsoft.com/services/key-vault/)
* [Documentation d’Azure Key Vault](https://docs.microsoft.com/azure/key-vault/)
* [SDK Azure pour .NET](https://github.com/Azure/azure-sdk-for-net)
* [Informations de référence sur l’API REST Azure](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
