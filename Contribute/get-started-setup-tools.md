---
title: Installer des outils de création de contenu
description: Cet article vous aide à télécharger et installer les outils clients dont vous avez besoin pour Git et pour l’édition de fichiers Markdown.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: jasonwhowell
ms.author: jasonh
ms.date: 04/30/2018
ms.openlocfilehash: 24d47c4e094c318be75a27dbaaec11d8ead94452
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288555"
---
# <a name="install-content-authoring-tools"></a>Installer des outils de création de contenu

Cet article décrit les étapes à suivre pour installer de manière interactive des outils clients Git et Visual Studio Code.
> [!div class="checklist"]
> * Installer [Git](https://git-scm.com/)
> * Installer [Visual Studio Code](https://code.visualstudio.com/)
> * Installer [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

>[!IMPORTANT]
> Si vous n’effectuez que des changements mineurs sur un article, vous n’avez *pas* besoin d’effectuer les étapes de cet article et vous pouvez passer directement au [workflow des changements rapides](index.md#quick-edits-to-existing-documents).
>
> Les principaux contributeurs sont encouragés à suivre ces étapes, qui permettent d’utiliser le [workflow de modifications majeures/à long terme](how-to-write-workflows-major.md). Même si vous disposez d’autorisations en écriture sur le référentiel principal, *nous vous conseillons vivement (et ce guide part de cette hypothèse) de dupliquer (fork) et de cloner le référentiel*, de façon à ce que vous ayez les autorisations en lecture/écriture nécessaires pour stocker les modifications que vous proposez dans votre fourche.

## <a name="install-git-client-tools"></a>Installer les outils client Git 

 Installez la dernière version des [outils client Git de Software Freedom Conservancy](https://git-scm.com/download/) pour votre plateforme. 

* [Git pour Windows](https://git-scm.com/download/win). Cette installation comprend le système de gestion de versions de Git et Git Bash, l’application en ligne de commande qui vous permettra d’interagir avec votre référentiel Git local.
* Git pour Mac est fourni dans le cadre des Outils en ligne de commande Xcode. Exécutez simplement `git` depuis la ligne de commande. Vous serez invité à installer les outils en ligne de commande si nécessaire. Vous pouvez aussi télécharger [Git pour Mac](https://git-scm.com/download/mac) à partir de Software Freedom Conservancy.
* [Git pour Linux et Unix](https://git-scm.com/download/linux)

Si vous préférez une interface graphique utilisateur (GUI) à une interface de ligne de commande (CLI), consultez la [page des clients GUI disponibles sur Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop](https://desktop.github.com/) ou [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) pour afficher des options répandues.

Suivez les instructions du client choisi pour l’installation et la configuration.

Dans le prochain article, vous allez [Configurer un référentiel Git local](get-started-setup-local.md).

   Des ressources Git supplémentaires sont disponibles ici : [Terminologie Git](https://help.github.com/articles/github-glossary) | [Notions de base de Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Découvrir Git et GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>Comprendre les éditeurs Markdown

Markdown est un langage de balisage léger à la fois facile à lire et facile à apprendre. Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur. Pour écrire des articles en Markdown, nous vous conseillons de commencer par télécharger et installer un éditeur Markdown.  [Visual Studio Code](https://code.visualstudio.com/) est l’outil de prédilection pour modifier des fichiers Markdown sous Microsoft. [Atom](https://atom.io) est un autre outil d’édition courant.

Le texte Markdown est enregistré dans des fichiers portant l’extension .md.

Vous trouverez davantage de détails sur l’écriture avec Markdown, notamment les bases de Markdown et les fonctionnalités prises en charge par les extensions Markdown personnalisées OPS (Open Publishing Services), dans les articles [Guide pratique pour utiliser Markdown pour écrire du contenu Docs](how-to-write-use-markdown.md) et [Informations de référence sur Markdown pour OPS](markdown-reference.md).

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), également connu sous le nom de VS Code, est un éditeur léger qui fonctionne sous Windows, Linux et Mac. Il comprend l’intégration Git et la prise en charge des extensions.

Téléchargez et installez [VS Code](https://code.visualstudio.com/). La page d’accueil de VS Code devrait détecter correctement votre système d’exploitation.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Pour lancer VS Code et ouvrir le dossier actif, exécutez la commande `code .` en ligne de commande ou dans un interpréteur de commandes Bash. Si le dossier actif fait partie d’un dépôt Git local, l’intégration de GitHub apparaît automatiquement dans Visual Studio Code.

## <a name="docs-authoring-pack"></a>Docs Authoring Pack
Installer Docs Authoring Pack pour Visual Studio Code. Cet ensemble d’extensions inclut une assistance de création de base pour l’écriture de Markdown et une fonctionnalité d’aperçu. Vous pouvez ainsi voir à quoi ressemble le Markdown dans le style du site docs.microsoft.com.

   Visitez cette [page de place de marché](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) et sélectionnez **Installer**, ou cherchez `docsmsft.docs-authoring-pack` dans votre liste d’extensions à l’intérieur de la fenêtre VS Code. 

   Pour accéder à Docs Authoring Pack, appuyez sur alt + M dans VS Code. La barre d’outils est masquée par défaut, mais peut être affichée. Modifiez les paramètres de VS Code (contrôle + virgule) et le paramètre d’ajout d’utilisateurs `"markdown.showToolbar": true` pour afficher la barre d’outils.

   Pour en savoir plus, consultez la page [Docs Authoring Pack](how-to-write-docs-auth-pack.md).


## <a name="next-steps"></a>Étapes suivantes

Vous pouvez maintenant [Configurer un référentiel Git local](get-started-setup-local.md).
