---
title: Installer des outils de création de contenu
description: Cet article vous aide à télécharger et installer les outils clients dont vous avez besoin pour Git et pour l’édition de fichiers Markdown.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="ff2f0-103">Installer des outils de création de contenu</span><span class="sxs-lookup"><span data-stu-id="ff2f0-103">Install content authoring tools</span></span>

<span data-ttu-id="ff2f0-104">Cet article décrit les étapes à suivre pour installer de manière interactive des outils clients Git et Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="ff2f0-105">Installer [Git pour Windows](https://git-scm.com/download/win)</span><span class="sxs-lookup"><span data-stu-id="ff2f0-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="ff2f0-106">Installer [Visual Studio Code](https://code.visualstudio.com/)</span><span class="sxs-lookup"><span data-stu-id="ff2f0-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="ff2f0-107">Si vous n’effectuez que des changements mineurs sur un article, vous n’avez *pas* besoin d’effectuer les étapes de cet article et vous pouvez passer directement au [flux de travail pour les changements mineurs/peu fréquents](light-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-107">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [minor/infrequent changes workflow](light-workflow.md).</span></span>
>
> <span data-ttu-id="ff2f0-108">Les principaux contributeurs sont encouragés à suivre ces étapes, qui permettent d’utiliser le [workflow de modifications majeures/à long terme](full-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-108">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](full-workflow.md).</span></span> <span data-ttu-id="ff2f0-109">Même si vous disposez d’autorisations en écriture sur le référentiel principal, *nous vous conseillons vivement (et ce guide part de cette hypothèse) de dupliquer (fork) et de cloner le référentiel*, de façon à ce que vous ayez les autorisations en lecture/écriture nécessaires pour stocker les modifications que vous proposez dans votre fourche.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-109">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="ff2f0-110">Installer les outils client Git sous Windows</span><span class="sxs-lookup"><span data-stu-id="ff2f0-110">Install Git client tools on Windows</span></span>

 <span data-ttu-id="ff2f0-111">Installez la dernière version des [outils client Git de Software Freedom Conservancy](https://git-scm.com/download/).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-111">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="ff2f0-112">L’installation comprend le système de gestion de versions de Git et Git Bash, l’application en ligne de commande qui vous permettra d’interagir avec votre référentiel Git local.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-112">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="ff2f0-113">Si vous préférez une interface graphique utilisateur (GUI) à une interface de ligne de commande (CLI), consultez la [page des clients GUI disponibles sur Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop](https://desktop.github.com/) ou [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) pour afficher des options répandues.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-113">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="ff2f0-114">Suivez les instructions du client choisi pour l’installation et la configuration.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-114">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="ff2f0-115">Dans le prochain article, vous allez [Configurer un référentiel Git local](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-115">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="ff2f0-116">Voici des liens vers des ressources Git supplémentaires : [Terminologie Git](https://help.github.com/articles/github-glossary) | [Bases de Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Découvrir Git et GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-116">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="ff2f0-117">Comprendre les éditeurs Markdown</span><span class="sxs-lookup"><span data-stu-id="ff2f0-117">Understand Markdown editors</span></span>

<span data-ttu-id="ff2f0-118">Markdown est un langage de balisage léger à la fois facile à lire et facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-118">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="ff2f0-119">Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-119">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="ff2f0-120">Pour écrire des articles en Markdown, nous vous conseillons de commencer par télécharger et installer un éditeur Markdown.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-120">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="ff2f0-121">[Visual Studio Code](https://code.visualstudio.com/) est l’outil de prédilection pour modifier des fichiers Markdown sous Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-121">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="ff2f0-122">[Atom](https://atom.io) est un autre outil d’édition courant.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-122">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="ff2f0-123">Le texte Markdown est enregistré dans des fichiers portant l’extension .md.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-123">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="ff2f0-124">Vous trouverez davantage de détails sur l’écriture avec Markdown, notamment les bases de Markdown et les fonctionnalités prises en charge par les extensions Markdown personnalisées OPS, plus loin dans l’article [Guide pratique pour utiliser Markdown](how-to-write-use-markdown.md).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-124">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="ff2f0-125">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ff2f0-125">Visual Studio Code</span></span>

<span data-ttu-id="ff2f0-126">[Visual Studio Code](https://code.visualstudio.com/), également connu sous le nom de VS Code, est un éditeur léger qui fonctionne sous Windows, Linux et Mac.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-126">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="ff2f0-127">Il comprend l’intégration Git et la prise en charge des extensions.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-127">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="ff2f0-128">Téléchargez et installez [VS Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-128">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="ff2f0-129">La page d’accueil de VS Code devrait détecter correctement votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-129">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="ff2f0-130">Windows</span><span class="sxs-lookup"><span data-stu-id="ff2f0-130">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="ff2f0-131">Mac</span><span class="sxs-lookup"><span data-stu-id="ff2f0-131">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="ff2f0-132">Linux</span><span class="sxs-lookup"><span data-stu-id="ff2f0-132">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="ff2f0-133">Pour lancer VS Code et ouvrir le dossier actif, exécutez la commande `code .` en ligne de commande ou dans un interpréteur de commandes Bash.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-133">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="ff2f0-134">Si le dossier actif fait partie d’un référentiel Git local, l’intégration de GitHub apparaît automatiquement dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="ff2f0-134">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ff2f0-135">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ff2f0-135">Next steps</span></span>

<span data-ttu-id="ff2f0-136">Vous pouvez maintenant [Configurer un référentiel Git local](get-started-setup-local.md).</span><span class="sxs-lookup"><span data-stu-id="ff2f0-136">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
