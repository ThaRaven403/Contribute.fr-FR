---
title: Configurer le dépôt Git localement
description: Cet article vous aider à créer un dépôt Git local et à contribuer à la documentation. Il explique notamment le processus de clonage et de duplication (fork).
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 01/18/2018
ms.openlocfilehash: e73c60c439285f901c5c83e538f8971d795bd6c4
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288591"
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="e847a-103">Configurer un référentiel Git localement pour la documentation</span><span class="sxs-lookup"><span data-stu-id="e847a-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="e847a-104">Cet article décrit les étapes à suivre pour configurer un référentiel Git sur un ordinateur local, dans l’intention de contribuer à la documentation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e847a-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="e847a-105">Les contributeurs peuvent utiliser un référentiel cloné localement pour ajouter de nouveaux articles, apporter des modifications importantes à des articles existants ou modifier des illustrations.</span><span class="sxs-lookup"><span data-stu-id="e847a-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="e847a-106">Effectuez une fois pour toutes ces activités de configuration afin de commencer à contribuer :</span><span class="sxs-lookup"><span data-stu-id="e847a-106">You run these one-time setup activities to start contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="e847a-107">Identifiez un référentiel adéquat.</span><span class="sxs-lookup"><span data-stu-id="e847a-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="e847a-108">Dupliquez (fork) le référentiel sur votre compte GitHub.</span><span class="sxs-lookup"><span data-stu-id="e847a-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="e847a-109">Choisissez un dossier local pour les fichiers clonés.</span><span class="sxs-lookup"><span data-stu-id="e847a-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="e847a-110">Clonez le référentiel sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e847a-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="e847a-111">Configurez la valeur à distance en amont.</span><span class="sxs-lookup"><span data-stu-id="e847a-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e847a-112">Si vous n’effectuez que des changements mineurs sur un article, vous n’avez *pas* besoin d’effectuer les étapes décrites dans cet article.</span><span class="sxs-lookup"><span data-stu-id="e847a-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="e847a-113">Vous pouvez passer directement aux [workflow pour les changements rapides](index.md#quick-edits-to-existing-documents).</span><span class="sxs-lookup"><span data-stu-id="e847a-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="e847a-114">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="e847a-114">Overview</span></span>

<span data-ttu-id="e847a-115">Pour contribuer au site de documentation de Microsoft, vous pouvez créer et modifier des fichiers Markdown localement en clonant le dépôt de documentation correspondant.</span><span class="sxs-lookup"><span data-stu-id="e847a-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="e847a-116">Microsoft vous impose de dupliquer (fork) le dépôt adéquat dans votre propre compte GitHub, de façon à ce que vous y disposiez des autorisations de lecture/écriture nécessaires pour stocker les modifications que vous proposez.</span><span class="sxs-lookup"><span data-stu-id="e847a-116">Microsoft requires you to fork the appropriate repository into your own GitHub account so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="e847a-117">Vous utiliserez ensuite des demandes de tirage (pull requests) pour fusionner les modifications dans le référentiel central partagé en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e847a-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![Triangle GitHub](./media/git-and-github-initial-setup.png)

<span data-ttu-id="e847a-119">Si vous découvrez GitHub, regardez la vidéo ci-dessous pour un aperçu conceptuel du processus de duplication et de clonage :</span><span class="sxs-lookup"><span data-stu-id="e847a-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="e847a-120">Déterminer le référentiel</span><span class="sxs-lookup"><span data-stu-id="e847a-120">Determine the repository</span></span>

<span data-ttu-id="e847a-121">La documentation hébergée sur [docs.microsoft.com](https://docs.microsoft.com) réside dans plusieurs référentiels différents à l’adresse [github.com](https://www.github.com).</span><span class="sxs-lookup"><span data-stu-id="e847a-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="e847a-122">Si vous ne savez pas exactement quel dépôt utiliser, accédez à l’article sur [docs.microsoft.com](https://docs.microsoft.com) avec votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="e847a-122">If you are unsure of which repository to use, then visit the article on [docs.microsoft.com](https://docs.microsoft.com) using your web browser.</span></span> <span data-ttu-id="e847a-123">Sélectionnez le lien **Modifier** (icône en forme de crayon) en haut à droite de l’article.</span><span class="sxs-lookup"><span data-stu-id="e847a-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![Cliquez sur Modifier pour déterminer l’emplacement du fichier et du référentiel.](media/index/edit-article.png)

2. <span data-ttu-id="e847a-125">Ce lien vous conduit à l’emplacement github.com du fichier Markdown correspondant dans le dépôt approprié.</span><span class="sxs-lookup"><span data-stu-id="e847a-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="e847a-126">Notez l’URL pour afficher le nom du référentiel.</span><span class="sxs-lookup"><span data-stu-id="e847a-126">Note the URL to view the repository name.</span></span>

   ![Notez l’URL pour déterminer l’emplacement du référentiel.](media/public-repo.png)

   <span data-ttu-id="e847a-128">Par exemple, ces référentiels courants sont ouverts aux contributions publiques :</span><span class="sxs-lookup"><span data-stu-id="e847a-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="e847a-129">Documentation Azure [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="e847a-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="e847a-130">Documentation SQL Server [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="e847a-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="e847a-131">Documentation Visual Studio [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="e847a-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="e847a-132">Documentation .NET [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="e847a-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="e847a-133">[Documentation du SDK Azure pour .NET https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="e847a-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>
   - <span data-ttu-id="e847a-134">Documentation ConfigMgr [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span><span class="sxs-lookup"><span data-stu-id="e847a-134">ConfigMgr documentation [https://github.com/MicrosoftDocs/SCCMdocs](https://github.com/MicrosoftDocs/SCCMdocs/)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="e847a-135">Dupliquer (fork) le référentiel</span><span class="sxs-lookup"><span data-stu-id="e847a-135">Fork the repository</span></span>
<span data-ttu-id="e847a-136">À l’aide du dépôt approprié, créez une duplication (fork) du dépôt dans votre propre compte GitHub à l’aide du site web GitHub.</span><span class="sxs-lookup"><span data-stu-id="e847a-136">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="e847a-137">Une duplication personnelle est requise dans la mesure où tous les dépôts de la documentation principale fournissent un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e847a-137">A personal fork is required since all main documentation repositories provide read-only access.</span></span> <span data-ttu-id="e847a-138">Pour effectuer des changements, vous devez envoyer une [demande de tirage](git-github-fundamentals.md#pull-requests) (pull request) au dépôt principal.</span><span class="sxs-lookup"><span data-stu-id="e847a-138">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="e847a-139">Pour faciliter ce processus, vous avez d’abord besoin de votre propre copie du dépôt auquel vous avez accès en écriture.</span><span class="sxs-lookup"><span data-stu-id="e847a-139">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="e847a-140">Une *duplication* GitHub sert à cela.</span><span class="sxs-lookup"><span data-stu-id="e847a-140">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="e847a-141">Naviguez vers la page GitHub du dépôt principal et cliquez sur le bouton **Fork** (Duplication) dans la partie supérieure droite.</span><span class="sxs-lookup"><span data-stu-id="e847a-141">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![Exemple de profil GitHub](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="e847a-143">Si vous y êtes invité, sélectionnez la vignette de votre compte GitHub comme destination de création de la duplication.</span><span class="sxs-lookup"><span data-stu-id="e847a-143">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="e847a-144">Il en résulte la création d’une copie du dépôt dans votre compte GitHub, appelée duplication.</span><span class="sxs-lookup"><span data-stu-id="e847a-144">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="e847a-145">Choisir un dossier local</span><span class="sxs-lookup"><span data-stu-id="e847a-145">Choose a local folder</span></span>
<span data-ttu-id="e847a-146">Créez un dossier local pour y placer une copie locale du dépôt.</span><span class="sxs-lookup"><span data-stu-id="e847a-146">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="e847a-147">Certains dépôts sont volumineux. Par exemple, azure-docs peut atteindre 5 Go.</span><span class="sxs-lookup"><span data-stu-id="e847a-147">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="e847a-148">Choisissez un emplacement avec de l’espace disque disponible.</span><span class="sxs-lookup"><span data-stu-id="e847a-148">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="e847a-149">Choisissez un nom de dossier facile à mémoriser et à taper.</span><span class="sxs-lookup"><span data-stu-id="e847a-149">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="e847a-150">Par exemple, utilisez un dossier racine `C:\docs\` ou créez un dossier dans le répertoire de votre profil utilisateur `~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="e847a-150">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="e847a-151">Évitez de choisir un chemin de dossier local imbriqué dans un autre emplacement de dossier de dépôt git.</span><span class="sxs-lookup"><span data-stu-id="e847a-151">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="e847a-152">Même s’il est possible de stocker les dossiers git clonés les uns à côté des autres, l’imbrication de dossiers git entre eux provoque des erreurs de suivi des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e847a-152">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="e847a-153">Lancez Git Bash.</span><span class="sxs-lookup"><span data-stu-id="e847a-153">Launch Git Bash</span></span>

   ![Lancer Git Bash](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="e847a-155">L’emplacement par défaut dans lequel Git Bash démarre est généralement le répertoire de base (~) ou `/c/users/<Windows-user-account>/` sur le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="e847a-155">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="e847a-156">Pour déterminer le répertoire actif, tapez `pwd` à l’invite $.</span><span class="sxs-lookup"><span data-stu-id="e847a-156">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="e847a-157">Utilisez cd pour changer de répertoire et passer au dossier que vous avez créé pour héberger le dépôt localement.</span><span class="sxs-lookup"><span data-stu-id="e847a-157">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="e847a-158">Notez que Git Bash respecte la convention Linux qui consiste à utiliser des barres obliques pour les chemins de dossier (et non des barres obliques inversées).</span><span class="sxs-lookup"><span data-stu-id="e847a-158">Note that Git Bash uses the Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="e847a-159">Par exemple, `cd /c/docs/ ` ou `cd ~/Documents/docs/`.</span><span class="sxs-lookup"><span data-stu-id="e847a-159">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="e847a-160">Créer un clone local</span><span class="sxs-lookup"><span data-stu-id="e847a-160">Create a local clone</span></span>

<span data-ttu-id="e847a-161">À l’aide de Git Bash, préparez l’exécution de la commande **clone** pour tirer (pull) une copie d’un dépôt (votre duplication) vers votre appareil sur le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="e847a-161">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="e847a-162">S’authentifier avec Git Credential Manager</span><span class="sxs-lookup"><span data-stu-id="e847a-162">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="e847a-163">Si vous avez installé la dernière version de Git pour Windows et accepté l’installation par défaut, Git Credential Manager est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="e847a-163">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="e847a-164">Git Credential Manager simplifie grandement l’authentification, car vous n’avez pas besoin de retenir votre jeton d’accès personnel quand vous rétablissez les connexions authentifiées et remotes avec GitHub.</span><span class="sxs-lookup"><span data-stu-id="e847a-164">Git Credential Manager makes authentication much easier because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="e847a-165">Exécutez la commande **clone** en indiquant le nom du dépôt.</span><span class="sxs-lookup"><span data-stu-id="e847a-165">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="e847a-166">Le clonage télécharge (clone) le dépôt dupliqué sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e847a-166">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="e847a-167">Vous pouvez obtenir l’URL GitHub de votre duplication pour la commande de clonage avec le bouton **Cloner ou télécharger** dans l’interface utilisateur de GitHub :</span><span class="sxs-lookup"><span data-stu-id="e847a-167">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![Cloner ou télécharger](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="e847a-169">Veillez à spécifier le chemin vers *votre duplication* lors du clonage et non celui du dépôt principal à partir duquel vous avez créé la duplication.</span><span class="sxs-lookup"><span data-stu-id="e847a-169">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="e847a-170">Sinon, vous ne pouvez pas apporter de changements.</span><span class="sxs-lookup"><span data-stu-id="e847a-170">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="e847a-171">Votre duplication est référencée par le biais de votre compte utilisateur GitHub personnel. Par exemple : `github.com/<github-username>/<repo>`.</span><span class="sxs-lookup"><span data-stu-id="e847a-171">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="e847a-172">Votre commande clone doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="e847a-172">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="e847a-173">À l’invite, entrez vos informations d’identification GitHub.</span><span class="sxs-lookup"><span data-stu-id="e847a-173">When you're prompted, enter your GitHub credentials.</span></span>

    ![Connexion à GitHub](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="e847a-175">À l’invite, entrez votre code d’authentification à 2 facteurs.</span><span class="sxs-lookup"><span data-stu-id="e847a-175">When you're prompted, enter your two-factor authentication code.</span></span>

    ![Authentification à 2 facteurs GitHub](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="e847a-177">Vos informations d’identification seront enregistrées et utilisées pour authentifier les demandes futures pour GitHub.</span><span class="sxs-lookup"><span data-stu-id="e847a-177">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="e847a-178">Vous avez seulement besoin de faire cette authentification une fois par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e847a-178">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="e847a-179">La commande clone s’exécute et télécharge une copie des fichiers de dépôt de votre duplication vers un nouveau dossier sur le disque local.</span><span class="sxs-lookup"><span data-stu-id="e847a-179">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="e847a-180">Un nouveau dossier est créé dans le dossier actif.</span><span class="sxs-lookup"><span data-stu-id="e847a-180">A new folder is made within the current folder.</span></span> <span data-ttu-id="e847a-181">Cette opération peut prendre quelques minutes en fonction de la taille du dépôt.</span><span class="sxs-lookup"><span data-stu-id="e847a-181">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="e847a-182">Vous pouvez explorer le dossier pour voir la structure une fois l’opération terminée.</span><span class="sxs-lookup"><span data-stu-id="e847a-182">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="e847a-183">Configurer remote upstream</span><span class="sxs-lookup"><span data-stu-id="e847a-183">Configure remote upstream</span></span>
<span data-ttu-id="e847a-184">Après avoir cloné le dépôt, configurez une connexion distante en lecture seule au dépôt principal nommé **upstream**.</span><span class="sxs-lookup"><span data-stu-id="e847a-184">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="e847a-185">Utilisez l’URL upstream pour synchroniser votre dépôt local avec les derniers changements apportés par d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e847a-185">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="e847a-186">Utilisez la commande **git remote** pour définir la valeur de configuration.</span><span class="sxs-lookup"><span data-stu-id="e847a-186">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="e847a-187">Utilisez la commande **fetch** pour actualiser les informations de branche du dépôt upstream.</span><span class="sxs-lookup"><span data-stu-id="e847a-187">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="e847a-188">Si vous utilisez **Git Credential Manager**, utilisez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e847a-188">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="e847a-189">Remplacez les espaces réservés \<repo\> et \<organization\>.</span><span class="sxs-lookup"><span data-stu-id="e847a-189">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="e847a-190">Examinez les valeurs configurées et confirmez que les URL sont correctes.</span><span class="sxs-lookup"><span data-stu-id="e847a-190">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="e847a-191">Vérifiez que les URL **origin** pointent vers votre duplication personnelle.</span><span class="sxs-lookup"><span data-stu-id="e847a-191">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="e847a-192">Vérifiez que les URL **upstream** pointent vers le dépôt principal, par exemple MicrosoftDocs ou Azure.</span><span class="sxs-lookup"><span data-stu-id="e847a-192">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="e847a-193">Voici un exemple de sortie remote.</span><span class="sxs-lookup"><span data-stu-id="e847a-193">Example remote output is shown.</span></span> <span data-ttu-id="e847a-194">Un compte git fictif nommé MyGitAccount est configuré avec un jeton d’accès personnel pour accéder au dépôt azure-docs :</span><span class="sxs-lookup"><span data-stu-id="e847a-194">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="e847a-195">Si vous avez fait une erreur, vous pouvez supprimer la valeur remote.</span><span class="sxs-lookup"><span data-stu-id="e847a-195">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="e847a-196">Pour supprimer la valeur upstream, exécutez la commande `git remote remove upstream`.</span><span class="sxs-lookup"><span data-stu-id="e847a-196">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e847a-197">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e847a-197">Next steps</span></span>
- <span data-ttu-id="e847a-198">Pour en savoir plus sur l’ajout et la mise à jour de contenu, passez à [Flux de travail de contribution à GitHub](how-to-write-workflows-major.md).</span><span class="sxs-lookup"><span data-stu-id="e847a-198">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>
