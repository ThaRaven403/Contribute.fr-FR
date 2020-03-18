---
title: Complétion des langages de développement - Docs Authoring Pack
description: Découvrez comment la complétion des langages de développement aide les contributeurs de l’extension Visual Studio Code Docs Authoring Pack.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336793"
---
# <a name="dev-lang-completion"></a>Complétion des langages de développement

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

Les contributeurs ont besoin d’aide pour déterminer les identificateurs de langage valide (langages de développement) qui peuvent suivre les trois accents graves (ouvertures de délimitation de code) dans un fichier Markdown. Malheureusement, il n’existe pas de validation des langages de développement au moment de la génération. Il en résulte des représentations disparates d’un même langage au sein du même docset conceptuel.

Prenons C# à titre d’exemple. Les contributeurs ont utilisé `c#`, `C#`, `cs`, `csharp`, entre autres, comme représentations du langage de développement. Laquelle des représentations précédentes est correcte ?

La fonctionnalité *Dev lang completion* (Complétion des langages de développement) dissipe la confusion en affichant une liste des langages de développement connus. Lors de la sélection d’un nom de langage de développement dans IntelliSense :

* La délimitation de code est fermée.
* Le signe insertion est positionné dans la délimitation de code.

## <a name="preferences"></a>Préférences

Il n’est pas possible de désactiver cette fonctionnalité. Les paramètres suivants sont disponibles :

* [Afficher les langages de développement couramment utilisés](#display-commonly-used-dev-langs)
* [Afficher tous les langages de développement connus](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a>Afficher les langages de développement couramment utilisés

Seule une partie des langages de développement valides est utilisé dans un même docset. Pour améliorer l’expérience utilisateur :

1. Dans Visual Studio Code, ouvrez le docset dans le répertoire racine.
1. Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).
1. Cliquez sur le lien **Edit in settings.json** (Modifier dans settings.json) dans la section **Markdown: Docset Languages** (Markdown : Langage du docset).
1. Ajoutez la propriété `markdown.docsetLanguages` suivante au fichier *settings.json* :

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. Placez le signe insertion dans le tableau vide de la propriété, puis activez IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Espace</kbd>). Une liste de noms de langage de développement connus s’affiche.
1. Ajoutez des noms de langage de développement au tableau jusqu’à ce que vous soyez satisfait de la liste. Par exemple, la liste suivante présente quatre noms de langage de développement à l’utilisateur après la saisie de trois accents graves :

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. Enregistrez les modifications apportées au fichier *settings.json*.

> [!WARNING]
> Un tableau `markdown.docsetLanguages` vide provoque l’affichage de tous les langages de développement connus.

### <a name="display-all-known-dev-langs"></a>Afficher tous les langages de développement connus

Par défaut, tous les noms de langage de développement connus sont affichés dans IntelliSense. Ce paramètre remplace la propriété `markdown.docsetLanguages` décrite dans [Afficher les langages de développement couramment utilisés](#display-commonly-used-dev-langs).

Pour changer ce paramètre :

1. Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).
1. Activez/désactivez le paramètre dans la section **Markdown : All Available Languages** (Markdown : Tous les langages disponibles).

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité :

[![Complétion des langages de développement](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)
