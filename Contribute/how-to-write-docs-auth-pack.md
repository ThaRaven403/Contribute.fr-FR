---
title: Docs Authoring Pack pour VS Code
description: Cet article décrit le pack d’extensions VS Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: d0d61db2faf88598ecd2c800fb5fbe8df8ec44f5
ms.sourcegitcommit: 7b668124f25b8ad0442937a3ad05b19a47af5970
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack pour VS Code

Docs Authoring Pack est une collection d’extensions VS Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com. [Disponible dans le VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), le pack contient les extensions suivantes :

- **DocFx** : fournit un aperçu de Markdown spécifique à docs.microsoft.com. Pour plus d’informations, consultez [DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX).
- **markdownlint** : créé par David Anson, ce linter populaire vérifie que le contenu Markdown respecte les bonnes pratiques. Pour plus d’informations, consultez [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).
- **Docs Markdown** : fournit de l’aide sur la création de contenu Markdown pour docs.microsoft.com dans OPS (Open Publishing System), notamment la prise en charge de base de Markdown et la prise en charge de syntaxes Markdown personnalisées dans OPS. Le reste de cette rubrique décrit l’extension Docs Markdown.

## <a name="prerequisites-and-assumptions"></a>Prérequis et hypothèses

Pour insérer avec précision des liens relatifs, des images et autre contenu incorporé avec l’extension Docs Markdown, la portée de votre espace de travail VS Code doit être limitée à la racine de votre dépôt OPS cloné.

Certaines syntaxes Markdown prises en charge par l’extension, comme les alertes et les extraits, sont personnalisées pour OPS. Celles-ci ne s’affichent correctement que si vous les publiez par le biais d’OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Comment utiliser l’extension Docs Markdown

Pour accéder au menu Docs Markdown, tapez `ALT+M`. Vous pouvez cliquer sur la fonction voulue ou utiliser les flèches haut/bas pour la sélectionner, ou encore taper son nom pour lancer le filtrage. Quand la fonction que vous voulez utiliser est en surbrillance dans le menu, appuyez sur `ENTER`. Les éléments suivants sont disponibles :

|Fonction     |Commande             |Description           |
|-------------|--------------------|----------------------|
|Gras         |`formatBold`        |Met le texte en **gras**.|
|Italique       |`formatItalic`      |Met le texte en *italique*.|
|Code         |`formatCode`        |Si une ligne ou moins est sélectionnée, met le texte au format `inline code`.<br><br>Si plusieurs lignes sont sélectionnées, applique le format « bloc de code délimité », et vous permet éventuellement de sélectionner un langage de programmation pris en charge par OPS.|
|Alerte        |`insertAlert`       |Insère un élément Note, Important, Warning ou Tip.<br><br>Sélectionnez Alert (Alerte) dans le menu, puis sélectionnez le type d’alerte. Si vous avez déjà sélectionné du texte, il est entouré de la syntaxe d’alerte sélectionnée. Si aucun texte n’est sélectionné, une nouvelle alerte est ajoutée avec un texte d’espace réservé.|
|Liste numérotée|`insertNumberedList` |Insère une nouvelle liste numérotée.<br><br> Si plusieurs lignes sont sélectionnées, chaque ligne constitue un élément de liste. Notez que les listes numérotées apparaissent toutes dans Markdown avec des 1. Toutefois, elles s’affichent sur docs.microsoft.com avec des numéros séquentiels ou, pour les listes imbriquées, des lettres. Pour créer une liste numérotée imbriquée, appuyez sur Tab dans la liste parente.|
|Liste à puces|`insertBulletedList` |Insère une nouvelle liste à puces.|
|Table        |`insertTable`        |Insère une structure de table Markdown.<br><br>Après avoir sélectionné la commande table, spécifiez le nombre de colonnes et de lignes au format colonnes:lignes. Par exemple : 3:4. Dans un souci de lisibilité, notez que le nombre maximum de colonnes que vous pouvez spécifier avec cette extension est de 5.|
|Lien         |`selectLinkType`      |Insère un lien. Quand vous sélectionnez cette commande, le sous-menu suivant apparaît.<br><br>`External` : créez un lien vers une page web avec un URI. Doit inclure « http » ou « https ».<br>`Internal` : insérez un lien relatif à un autre fichier dans le même dépôt. Après avoir sélectionné cette option, tapez du texte dans la fenêtre de commande pour filtrer les fichiers par nom, puis sélectionnez le fichier souhaité. <br>`Bookmark in this file` : choisissez un élément dans une liste de titres du fichier actif pour insérer un signet correctement mis en forme.<br>`Bookmark in another file` : commencez par filtrer les fichiers par nom et sélectionnez le fichier vers lequel doit pointer le lien, puis choisissez le titre approprié dans le fichier sélectionné.|
|Image        |`insertImage`     |Tapez le texte de remplacement (obligatoire à des fins d’accessibilité) et sélectionnez-le, puis appelez cette commande pour filtrer la liste des fichiers image pris en charge dans le dépôt et sélectionnez celui que vous voulez. Si aucun texte de remplacement n’est sélectionné quand vous appelez cette commande, vous êtes invité à le faire avant de pouvoir choisir un fichier image.|
|Inclure      |`insertInclude`   |Recherchez un fichier à incorporer au fichier actif.|
|Extrait      |`insertSnippet`   |Recherchez un extrait de code dans le dépôt à incorporer au fichier actif.|
|Vidéo        |`insertVideo`     |Ajoutez une vidéo incorporée.|
|Aperçu      |`previewTopic`    |Prévisualisez la rubrique active dans une fenêtre côte à côte à l’aide de l’extension DocFX.  Si l’extension DocFX n’est pas installée ou qu’elle est installée mais désactivée, la rubrique ne s’affiche pas.


## <a name="how-to-assign-keyboard-shortcuts"></a>Comment définir des raccourcis clavier

1. Appuyez sur `CTRL+K`, puis sur `CTRL+S` pour ouvrir la liste des raccourcis clavier.
1. Recherchez la commande pour laquelle vous souhaitez créer une combinaison de touches personnalisée, par exemple `formatBold`.
1. Cliquez sur le signe plus qui apparaît près du nom de la commande quand vous pointez sur la ligne.
1. À l’apparition d’une nouvelle zone d’entrée, tapez le raccourci clavier à associer à cette commande particulière. Par exemple, pour utiliser le raccourci courant de mise en gras, tapez `ctrl+b`.
1. Il est conseillé d’insérer une clause `when` dans votre combinaison de touches pour que celle-ci soit uniquement disponible dans les fichiers Markdown. Pour ce faire, ouvrez *keybindings.json* et insérez la ligne suivante sous le nom de la commande (veillez à ajouter une virgule entre les lignes) :
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Au final, votre combinaison de touches personnalisée doit ressembler à ceci dans keybindings.json :

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. Enregistrez keybindings.json.

Pour plus informations, consultez [Combinaison de touches](https://code.visualstudio.com/docs/getstarted/keybindings) dans la documentation VS Code.

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Comment afficher la barre d’outils « Gauntlet » héritée

Les utilisateurs de l’ancienne extension (nom de code « Gauntlet ») remarqueront que la barre d’outils de création n’apparaît plus en bas de la fenêtre VS Code quand l’extension Docs Markdown est installée. En effet, la barre d’outils prenait beaucoup de place sur la barre d’état de VS Code et ne suivait pas les bonnes pratiques en matière d’expérience utilisateur pour les extensions. Elle est donc dépréciée dans la nouvelle extension. Vous pouvez tout de même afficher la barre d’outils en mettant à jour votre fichier VS Code settings.json comme suit :

1. Dans VS Code, accédez à Fichier -> Préférences -> Paramètres (`CTRL+Comma`).
1. Sélectionnez Paramètres utilisateur pour changer les paramètres de tous les espaces de travail VS Code ou Paramètres de l’espace de travail pour les changer uniquement dans l’espace de travail actif.
1. Dans le volet Paramètres par défaut, recherchez Docs Authoring Extension Configuration, puis sélectionnez l’icône représentant un crayon à côté du paramètre souhaité. Vous êtes ensuite invité à sélectionner `true` ou `false`. Une fois votre sélection effectuée, VS Code ajoute automatiquement la valeur au fichier settings.json, et vous êtes invité à recharger la fenêtre pour que les changements entrent en vigueur.

## <a name="known-issues"></a>Problèmes connus

- Aperçu DocFX : sur MacOS et Linux, l’aperçu DocFX ne lance pas correctement l’aperçu (l’aperçu de VS Code Markdown est choisi par défaut pour ces plateformes).
- Aperçu DocFX :sur toutes les plateformes, certaines syntaxes, notamment les liens xref (références croisées) vers les API, ne s’affichent pas correctement dans l’aperçu, laissant dans certains cas des vides dans le contenu.
- Signets externes : sur Linux, la liste des fichiers est affichée, mais aucun titre ne peut être sélectionné.
- Inclut : sur Linux, la liste des fichiers est affichée, mais aucun lien n’est ajouté après la sélection.
