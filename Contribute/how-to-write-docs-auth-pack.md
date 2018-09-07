---
title: Docs Authoring Pack pour VS Code
description: Cet article décrit le pack d’extensions VS Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.openlocfilehash: b9fedce0a73c5c4212ffd0893c745fab56677c8c
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308913"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack pour VS Code

Docs Authoring Pack est une collection d’extensions VS Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com. [Disponible dans le VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), le pack contient les extensions suivantes :

- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) : créé par David Anson, ce linter populaire vérifie que le contenu Markdown respecte les bonnes pratiques.
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) : outil de vérification orthographique entièrement hors ligne de Street Side Software.
- [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview) : utilise la feuilles de style en cascade docs.microsoft.com pour un aperçu Markdown plus précis, notamment Markdown personnalisé.
- [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) : fournit de l’aide sur la création de contenu Markdown pour docs.microsoft.com dans OPS (Open Publishing System), notamment la prise en charge de base de Markdown et la prise en charge de syntaxes Markdown personnalisées dans OPS. Le reste de cette rubrique décrit l’extension Docs Markdown.
- [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates) : permet aux utilisateurs d’appliquer du contenu squelette Markdown aux nouveaux fichiers.

## <a name="prerequisites-and-assumptions"></a>Prérequis et hypothèses

Pour insérer avec précision des liens relatifs, des images et autre contenu incorporé avec l’extension Docs Markdown, la portée de votre espace de travail VS Code doit être limitée à la racine de votre dépôt Open Publishing System (OPS) cloné.

Certaines syntaxes Markdown prises en charge par l’extension, comme les alertes et les extraits, sont personnalisées pour OPS. Celles-ci ne s’affichent correctement que si vous les publiez par le biais d’OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Comment utiliser l’extension Docs Markdown

Pour accéder au menu Docs Markdown, tapez `ALT+M`. Vous pouvez cliquer sur la fonction voulue ou utiliser les flèches haut/bas pour la sélectionner, ou encore taper son nom pour lancer le filtrage. Quand la fonction que vous voulez utiliser est en surbrillance dans le menu, appuyez sur `ENTER`. Les éléments suivants sont disponibles :

|Fonction     |Description           |
|-------------|----------------------|
|Aperçu      |Prévisualisez la rubrique active dans une fenêtre côte à côte à l’aide de l’extension Docs Preview. Cette option n’est disponible que si Docs Preview est installé.|
|Gras         |Met le texte en **gras**.|
|Italique       |Met le texte en *italique*.|
|Code         |Si une ligne ou moins est sélectionnée, met le texte au format `inline code`.<br><br>Si plusieurs lignes sont sélectionnées, applique le format « bloc de code délimité », et vous permet éventuellement de sélectionner un langage de programmation pris en charge par OPS.|
|Alerte        |Insère un élément Note, Important, Warning ou Tip.<br><br>Sélectionnez Alert (Alerte) dans le menu, puis sélectionnez le type d’alerte. Si vous avez déjà sélectionné du texte, il est entouré de la syntaxe d’alerte sélectionnée. Si aucun texte n’est sélectionné, une nouvelle alerte est ajoutée avec un texte d’espace réservé.|
|Liste numérotée|Insère une nouvelle liste numérotée.<br><br> Si plusieurs lignes sont sélectionnées, chaque ligne constitue un élément de liste. Notez que les listes numérotées apparaissent toutes dans Markdown avec des 1. Toutefois, elles s’affichent sur docs.microsoft.com avec des numéros séquentiels ou, pour les listes imbriquées, des lettres. Pour créer une liste numérotée imbriquée, appuyez sur Tab dans la liste parente.|
|Liste à puces|Insère une nouvelle liste à puces.|
|Table        |Insère une structure de table Markdown.<br><br>Après avoir sélectionné la commande table, spécifiez le nombre de colonnes et de lignes au format colonnes:lignes. Par exemple : 3:4. Dans un souci de lisibilité, notez que le nombre maximum de colonnes que vous pouvez spécifier avec cette extension est de 5.|
|Lien vers un fichier dans le référentiel|Insère un lien relatif à un autre fichier dans le référentiel actuel. Après avoir sélectionné cette option, tapez du texte dans la fenêtre de commande pour filtrer les fichiers par nom, puis sélectionnez le fichier souhaité. Si vous aviez précédemment sélectionné du texte, il devient le texte du lien. Sinon, le titre H1 du fichier cible est utilisé comme texte du lien.|
|Lien vers une page web    |Insère un lien vers une page web. Une fois cette option sélectionnée, collez ou tapez l’URI dans la fenêtre de commande. `https://` est obligatoire. Si vous aviez précédemment sélectionné du texte, il devient le texte du lien. Sinon, l’URI sera utilisé comme texte du lien.|
|Lien vers un titre     |Assure le lien vers un signet dans le fichier actuel ou un autre fichier du référentiel.<br>`Bookmark in this file` : choisissez un élément dans une liste de titres du fichier actif pour insérer un signet correctement mis en forme.<br>`Bookmark in another file` : commencez par filtrer les fichiers par nom et sélectionnez le fichier vers lequel doit pointer le lien, puis choisissez le titre approprié dans le fichier sélectionné.|
|Image        |Tapez le texte de remplacement (obligatoire à des fins d’accessibilité) et sélectionnez-le, puis appelez cette commande pour filtrer la liste des fichiers image pris en charge dans le dépôt et sélectionnez celui que vous voulez. Si aucun texte de remplacement n’est sélectionné quand vous appelez cette commande, vous êtes invité à le faire avant de pouvoir choisir un fichier image.|
|Inclure      |Recherchez un fichier à incorporer au fichier actif.|
|Extrait      |Recherchez un extrait de code dans le dépôt à incorporer au fichier actif.|
|Vidéo        |Ajoutez une vidéo incorporée.|
|Modèle     |Créez un fichier et appliquez un modèle Markdown. Pour plus d’informations, consultez [Modèles](#how-to-use-docs-templates) ci-dessous.|

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

## <a name="how-to-show-the-legacy-toolbar"></a>Comment afficher la barre d’outils héritée

Les utilisateurs de la préversion de l’extension remarqueront que la barre d’outils de création n’apparaît plus en bas de la fenêtre VS Code quand l’extension Docs Markdown est installée. En effet, la barre d’outils prenait beaucoup de place sur la barre d’état de VS Code et ne suivait pas les bonnes pratiques en matière d’expérience utilisateur pour les extensions. Elle est donc dépréciée dans la nouvelle extension. Vous pouvez tout de même afficher la barre d’outils en mettant à jour votre fichier VS Code settings.json comme suit :

1. Dans VS Code, accédez à Fichier -> Préférences -> Paramètres (`CTRL+Comma`).
1. Sélectionnez Paramètres utilisateur pour changer les paramètres de tous les espaces de travail VS Code ou Paramètres de l’espace de travail pour les changer uniquement dans l’espace de travail actif.
1. Dans le volet Paramètres par défaut, recherchez Docs Authoring Extension Configuration, puis sélectionnez l’icône représentant un crayon à côté du paramètre souhaité. Vous êtes ensuite invité à sélectionner `true` ou `false`. Une fois votre sélection effectuée, VS Code ajoute automatiquement la valeur au fichier settings.json, et vous êtes invité à recharger la fenêtre pour que les changements entrent en vigueur.

## <a name="how-to-use-docs-templates"></a>Utilisation des modèles Docs

L’extension Docs Article Templates permet à ceux qui écrivent en VS Code d’extraire un modèle Markdown à partir d’un magasin centralisé et de l’appliquer à un fichier. Les modèles peuvent permettre de s’assurer que les métadonnées requises sont incluses dans les articles, que les normes relatives au contenu sont respectées, etc. Les modèles sont gérés en tant que fichiers Markdown dans un référentiel GitHub public.

### <a name="to-apply-a-template-in-vs-code"></a>Pour appliquer un modèle dans VS Code

1. Si l’extension Docs Markdown n’est pas installée, appuyez sur F1 pour ouvrir la palette de commandes, commencez à taper « template » pour filtrer les résultats, puis cliquez sur `Docs: Template`. Si l’extension Docs Markdown est installée, vous pouvez utiliser la palette de commandes ou vous pouvez cliquer sur `Alt+M` pour afficher le menu Docs Markdown QuickPick, puis sélectionnez `Template` dans la liste.
1. Sélectionnez le modèle requis dans la liste qui s’affiche.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Pour ajouter votre ID GitHub et/ou votre alias Microsoft à vos paramètres VS Code

L’extension Templates prend en charge trois champs de métadonnées dynamiques : author, ms.author et ms.date. Cela signifie que si le créateur d’un modèle utilise ces champs dans l’en-tête des métadonnées d’un modèle Markdown, ces champs seront renseignés automatiquement dans votre fichier lorsque vous appliquez le modèle, comme suit :

|Métadonnées  |Valeur|
|----------|---------------|
|author    |Votre ID GitHub, si spécifié dans le fichier des paramètres VS Code.|
|ms.author |Votre alias Microsoft, si spécifié dans le fichier des paramètres VS Code. Si vous n’êtes pas un employé de Microsoft, ne renseignez pas ce champ.|
|ms.date   |La date actuelle au format pris en charge par Docs, MM/JJ/AAAA. Notez que la date n’est pas automatiquement mise à jour si vous modifiez le fichier ultérieurement. Vous devez la mettre à jour manuellement pour indiquer la date de l’article.|

### <a name="to-set-author-github-id-andor-msauthor-microsoft-alias"></a>Pour définir author (ID GitHub) et/ou ms.author (alias Microsoft)

1. Dans VS Code, accédez à Fichier -> Préférences -> Paramètres (`CTRL+Comma`).
1. Sélectionnez Paramètres utilisateur pour changer les paramètres de tous les espaces de travail VS Code ou Paramètres de l’espace de travail pour les changer uniquement dans l’espace de travail actif.
1. Dans le volet Paramètres par défaut à gauche, recherchez Docs Article Templates Extension Configuration, cliquez sur l’icône crayon en regard du paramètre requis, puis cliquez sur Remplacer dans les paramètres.
1. Le volet Paramètres utilisateur s’ouvre à côté et contient une nouvelle entrée en bas.
1. Ajoutez votre ID GitHub ou votre alias e-mail Microsoft, le cas échéant, et enregistrez le fichier.
1. Vous devrez peut-être fermer et redémarrer VS Code pour que les modifications prennent effet.
1. À présent, lorsque vous appliquez un modèle qui utilise des champs dynamiques, votre ID GitHub et/ou votre alias Microsoft sera automatiquement renseigné dans l’en-tête des métadonnées.
