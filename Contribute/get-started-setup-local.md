---
title: Configurer le dépôt Git localement
description: Cet article vous aider à créer un dépôt Git local et à contribuer à la documentation. Il explique notamment le processus de clonage et de duplication (fork).
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: f702d0d29ee7dc9c69cb26b79bf6283d91b6b6bc
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469759"
---
# <a name="set-up-git-repository-locally-for-documentation"></a>Configurer un référentiel Git localement pour la documentation

Cet article décrit les étapes à suivre pour configurer un référentiel Git sur un ordinateur local, dans l’intention de contribuer à la documentation de Microsoft. Les contributeurs peuvent utiliser un référentiel cloné localement pour ajouter de nouveaux articles, apporter des modifications importantes à des articles existants ou modifier des illustrations.

Effectuez une fois pour toutes ces activités de configuration afin de commencer à contribuer :
> [!div class="checklist"]
> * Identifiez un référentiel adéquat.
> * Dupliquez (fork) le référentiel sur votre compte GitHub.
> * Choisissez un dossier local pour les fichiers clonés.
> * Clonez le référentiel sur votre ordinateur local.
> * Configurez la valeur à distance en amont.

> [!IMPORTANT]
> Si vous n’effectuez que des changements mineurs sur un article, vous n’avez *pas* besoin d’effectuer les étapes décrites dans cet article. Vous pouvez passer directement aux [workflow pour les changements rapides](index.md#quick-edits-to-existing-documents).
>

## <a name="overview"></a>Vue d'ensemble

Pour contribuer au site de documentation de Microsoft, vous pouvez créer et modifier des fichiers Markdown localement en clonant le dépôt de documentation correspondant. Microsoft vous impose de dupliquer (fork) le référentiel adéquat dans votre propre compte GitHub, de façon à ce que vous y disposiez des autorisations de lecture/écriture nécessaires pour stocker les modifications que vous proposez. Vous utiliserez ensuite des demandes de tirage (pull requests) pour fusionner les modifications dans le référentiel central partagé en lecture seule.

![Triangle GitHub](./media/git-and-github-initial-setup.png)

Si vous découvrez GitHub, regardez la vidéo ci-dessous pour un aperçu conceptuel du processus de duplication et de clonage :

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a>Déterminer le référentiel

La documentation hébergée sur [docs.microsoft.com](https://docs.microsoft.com) réside dans plusieurs référentiels différents à l’adresse [github.com](https://www.github.com).

1. Si vous ne savez pas exactement quel référentiel utiliser, accédez à l’article sur docs.microsoft.com avec votre navigateur web. Sélectionnez le lien **Modifier** (icône en forme de crayon) en haut à droite de l’article.

   ![Cliquez sur Modifier pour déterminer l’emplacement du fichier et du référentiel.](media/index/edit-article.png)

2. Ce lien vous conduit à l’emplacement github.com du fichier Markdown correspondant dans le dépôt approprié. Notez l’URL pour afficher le nom du référentiel.

   ![Notez l’URL pour déterminer l’emplacement du référentiel.](media/public-repo.png)

   Par exemple, ces référentiels courants sont ouverts aux contributions publiques :
   - Documentation Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)
   - Documentation SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)
   - Documentation Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)
   - Documentation .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)
   - [Documentation du SDK Azure pour .NEThttps://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)

## <a name="fork-the-repository"></a>Dupliquer (fork) le référentiel
À l’aide du dépôt approprié, créez une duplication (fork) du dépôt dans votre propre compte GitHub à l’aide du site web GitHub.

Une duplication personnelle est nécessaire, car tous les dépôts de documentation principaux fournissent un accès en lecture seule, ce qui signifie que vous ne pouvez pas changer directement le contenu des dépôts. Pour effectuer des changements, vous devez envoyer une [demande de tirage](git-github-fundamentals.md#pull-requests) (pull request) au dépôt principal. Pour faciliter ce processus, vous avez d’abord besoin de votre propre copie du dépôt auquel vous avez accès en écriture. Une *duplication* GitHub sert à cela.

1. Naviguez vers la page GitHub du dépôt principal et cliquez sur le bouton **Fork** (Duplication) dans la partie supérieure droite.

   ![Exemple de profil GitHub](./media/contribute-get-started-setup-local/fork.png)

2. Si vous y êtes invité, sélectionnez la vignette de votre compte GitHub comme destination de création de la duplication. Il en résulte la création d’une copie du dépôt dans votre compte GitHub, appelée duplication.

## <a name="choose-a-local-folder"></a>Choisir un dossier local
Créez un dossier local pour y placer une copie locale du dépôt. Certains dépôts sont volumineux. Par exemple, azure-docs peut atteindre 5 Go. Choisissez un emplacement avec de l’espace disque disponible.

1. Choisissez un nom de dossier facile à mémoriser et à taper. Par exemple, utilisez un dossier racine `C:\docs\` ou créez un dossier dans le répertoire de votre profil utilisateur `~/Documents/docs/`.

   > [!IMPORTANT]
   > Évitez de choisir un chemin de dossier local imbriqué dans un autre emplacement de dossier de dépôt git. Même s’il est possible de stocker les dossiers git clonés les uns à côté des autres, l’imbrication de dossiers git entre eux provoque des erreurs de suivi des fichiers.

2. Lancez Git Bash.

   ![Lancer Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   L’emplacement par défaut dans lequel Git Bash démarre est généralement le répertoire de base (~) ou `/c/users/<Windows-user-account>/` sur le système d’exploitation Windows.

   Pour déterminer le répertoire actif, tapez `pwd` à l’invite $. 

3. Utilisez cd pour changer de répertoire et passer au dossier que vous avez créé pour héberger le dépôt localement. Notez que Git Bash respecte la convention Linux qui consiste à utiliser des barres obliques pour les chemins de dossier (et non des barres obliques inversées).

   Par exemple, `cd /c/docs/ ` ou `cd ~/Documents/docs/`.

## <a name="create-a-local-clone"></a>Créer un clone local

À l’aide de Git Bash, préparez l’exécution de la commande **clone** pour tirer (pull) une copie d’un dépôt (votre duplication) vers votre appareil sur le répertoire actif. 

### <a name="authenticate-by-using-git-credential-manager"></a>S’authentifier avec Git Credential Manager
Si vous avez installé la dernière version de Git pour Windows et accepté l’installation par défaut, Git Credential Manager est activé par défaut. Git Credential Manager simplifie grandement l’authentification, car vous n’avez pas besoin de retenir votre jeton d’accès personnel quand vous rétablissez les connexions authentifiées et remotes avec GitHub.

1. Exécutez la commande **clone** en indiquant le nom du dépôt. Le clonage télécharge (clone) le dépôt dupliqué sur votre ordinateur local. 

    > [!Tip]
    > Vous pouvez obtenir l’URL GitHub de votre duplication pour la commande de clonage avec le bouton **Cloner ou télécharger** dans l’interface utilisateur de GitHub :
    >
    > ![Cloner ou télécharger](./media/contribute-get-started-setup-local/clone-or-download.png)

    Veillez à spécifier le chemin vers *votre duplication* lors du clonage et non celui du dépôt principal à partir duquel vous avez créé la duplication. Sinon, vous ne pouvez pas apporter de changements. Votre duplication est référencée par le biais de votre compte utilisateur GitHub personnel. Par exemple : `github.com/<github-username>/<repo>`.

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    Votre commande clone doit ressembler à ceci :

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. À l’invite, entrez vos informations d’identification GitHub.

    ![Connexion à GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. À l’invite, entrez votre code d’authentification à 2 facteurs.

    ![Authentification à 2 facteurs GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > Vos informations d’identification seront enregistrées et utilisées pour authentifier les demandes futures pour GitHub. Vous avez seulement besoin de faire cette authentification une fois par ordinateur. 

4. La commande clone s’exécute et télécharge une copie des fichiers de dépôt de votre duplication vers un nouveau dossier sur le disque local. Un nouveau dossier est créé dans le dossier actif. Cette opération peut prendre quelques minutes en fonction de la taille du dépôt. Vous pouvez explorer le dossier pour voir la structure une fois l’opération terminée.

## <a name="configure-remote-upstream"></a>Configurer remote upstream
Après avoir cloné le dépôt, configurez une connexion distante en lecture seule au dépôt principal nommé **upstream**. Utilisez l’URL upstream pour synchroniser votre dépôt local avec les derniers changements apportés par d’autres utilisateurs. Utilisez la commande **git remote** pour définir la valeur de configuration. Utilisez la commande **fetch** pour actualiser les informations de branche du dépôt upstream.

1. Si vous utilisez **Git Credential Manager**, utilisez les commandes suivantes. Remplacez les espaces réservés \<repo\> et \<organization\>.
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. Examinez les valeurs configurées et confirmez que les URL sont correctes. Vérifiez que les URL **origin** pointent vers votre duplication personnelle. Vérifiez que les URL **upstream** pointent vers le dépôt principal, par exemple MicrosoftDocs ou Azure. 
   ```bash
   git remote -v 
   ```

   Voici un exemple de sortie remote. Un compte git fictif nommé MyGitAccount est configuré avec un jeton d’accès personnel pour accéder au dépôt azure-docs :
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. Si vous avez fait une erreur, vous pouvez supprimer la valeur remote. Pour supprimer la valeur upstream, exécutez la commande `git remote remove upstream`.

## <a name="next-steps"></a>Étapes suivantes
- Pour en savoir plus sur l’ajout et la mise à jour de contenu, passez à [Flux de travail de contribution à GitHub](how-to-write-workflows-major.md).