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
ms.openlocfilehash: 0ca942e557640db1ba36d3f5b1064656ed3dea8d
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="install-content-authoring-tools"></a>Installer des outils de création de contenu

Cet article décrit les étapes à suivre pour installer de manière interactive des outils clients Git et Visual Studio Code.
> [!div class="checklist"]
> * Installer [Git pour Windows](https://git-scm.com/download/win)
> * Installer [Visual Studio Code](https://code.visualstudio.com/)

>[!IMPORTANT]
> Si vous n’effectuez que des changements mineurs sur un article, vous n’avez *pas* besoin d’effectuer les étapes de cet article et vous pouvez passer directement au [workflow des changements rapides](index.md#quick-edits-to-existing-documents).
>
> Les principaux contributeurs sont encouragés à suivre ces étapes, qui permettent d’utiliser le [workflow des changements majeurs/à long terme](how-to-write-workflows-major.md). Même si vous disposez d’autorisations en écriture sur le dépôt principal, *nous vous conseillons vivement (et ce guide part de cette hypothèse) de dupliquer (fork) et de cloner le dépôt*, de façon à ce que vous ayez les autorisations en lecture/écriture nécessaires pour stocker les changements que vous proposez dans votre duplication.

## <a name="install-git-client-tools-on-windows"></a>Installer les outils client Git sous Windows

 Installez la dernière version des [outils client Git de Software Freedom Conservancy](https://git-scm.com/download/). L’installation comprend le système de gestion de versions de Git et Git Bash, l’application en ligne de commande qui vous permet d’interagir avec votre dépôt Git local.

Si vous préférez une interface graphique utilisateur (GUI) à une interface de ligne de commande (CLI), consultez la [page des clients GUI disponibles sur Software Freedom Conservancy](https://git-scm.com/downloads/guis), [GitHub Desktop](https://desktop.github.com/) ou [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) pour afficher des options répandues.

Suivez les instructions du client choisi pour l’installation et la configuration.

Dans le prochain article, vous allez [Configurer un dépôt Git local](get-started-setup-local.md).

   Voici des liens vers des ressources Git supplémentaires : [Terminologie Git](https://help.github.com/articles/github-glossary) | [Bases de Git](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Découvrir Git et GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/).

## <a name="understand-markdown-editors"></a>Comprendre les éditeurs Markdown

Markdown est un langage de balisage léger à la fois facile à lire et facile à apprendre. Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur. Pour écrire des articles en Markdown, nous vous conseillons de commencer par télécharger et installer un éditeur Markdown.  [Visual Studio Code](https://code.visualstudio.com/) est l’outil de prédilection pour modifier des fichiers Markdown sous Microsoft. [Atom](https://atom.io) est un autre outil d’édition courant.

Le texte Markdown est enregistré dans des fichiers portant l’extension .md.

Vous trouverez davantage de détails sur l’écriture avec Markdown, notamment les bases de Markdown et les fonctionnalités prises en charge par les extensions Markdown personnalisées OPS, plus loin dans l’article [Guide pratique pour utiliser Markdown](how-to-write-use-markdown.md).

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/), également connu sous le nom de VS Code, est un éditeur léger qui fonctionne sous Windows, Linux et Mac. Il comprend l’intégration Git et la prise en charge des extensions.

Téléchargez et installez [VS Code](https://code.visualstudio.com/). La page d’accueil de VS Code devrait détecter correctement votre système d’exploitation.

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> Pour lancer VS Code et ouvrir le dossier actif, exécutez la commande `code .` en ligne de commande ou dans un interpréteur de commandes Bash. Si le dossier actif fait partie d’un dépôt Git local, l’intégration de GitHub apparaît automatiquement dans Visual Studio Code.

## <a name="next-steps"></a>Étapes suivantes

Vous pouvez maintenant [Configurer un dépôt Git local](get-started-setup-local.md).
