---
title: Docs Authoring Pack pour Visual Studio Code
description: Cet article décrit le pack d’extensions Visual Studio Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336396"
---
# <a name="docs-authoring-pack-for-vs-code"></a>Docs Authoring Pack pour VS Code

Docs Authoring Pack est une collection d’extensions VS Code visant à faciliter la création de contenu Markdown pour docs.microsoft.com. [Disponible dans le VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack), le pack contient les extensions suivantes :

> [!div class="checklist"]
> * [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) : Fournit de l’aide sur la création de contenu Markdown pour docs.microsoft.com (Docs), notamment la prise en charge de base de Markdown et la prise en charge de syntaxes Markdown personnalisées dans Docs, telles que les alertes, les extraits de code et le texte non localisable. Comprend également de l’aide de base sur la création de contenu YAML, par exemple l’insertion d’entrées de table des matières.
> * [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) : Un linter Markdown créé par David Anson pour vérifier que votre Markdown est valide.
> * [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) : Un outil de vérification orthographique entièrement hors connexion par Street Side Software.
> * [Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview) : Utilise la feuille de style en cascade de docs.microsoft.com pour un aperçu Markdown plus précis, notamment le Markdown personnalisé.
> * [Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates) : Permet aux utilisateurs de créer une structure de modules Learn et d’appliquer du contenu de squelette Markdown à de nouveaux fichiers.
> * [Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml) : Fournit la validation de schéma Docs YAML et la complétion.
> * [Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images) : Fournit la compression et le redimensionnement des images pour les dossiers et les fichiers individuels afin d’aider les auteurs de docs.microsoft.com.

## <a name="prerequisites-and-assumptions"></a>Prérequis et hypothèses

Pour insérer des liens relatifs, des images et autre contenu incorporé avec l’extension Docs Markdown, la portée de votre espace de travail VS Code doit être limitée à la racine de votre dépôt Open Publishing System (OPS) cloné. Par exemple, si vous avez cloné le dépôt docs sur `C:\git\SomeDocsRepo\`, ouvrez ce dossier ou un sous-dossier dans VS Code : Menu **Fichier** > **Ouvrir le dossier** ou `code C:\git\SomeDocsRepo\` à partir de la ligne de commande.

Certaines syntaxes Markdown prises en charge par l’extension, comme les alertes et les extraits, sont personnalisées pour OPS. Celles-ci ne s’affichent correctement que si vous les publiez par le biais d’OPS.

## <a name="how-to-use-the-docs-markdown-extension"></a>Comment utiliser l’extension Docs Markdown

Pour accéder au menu **Docs Markdown**, tapez <kbd>Alt+M</kbd>. Vous pouvez cliquer ou utiliser les flèches vers le haut et vers le bas pour sélectionner la commande souhaitée. Vous pouvez également taper pour démarrer le filtrage, puis appuyer sur <kbd>Entrée</kbd> quand la fonction souhaitée est mise en surbrillance dans le menu.

Pour obtenir la liste des commandes à jour, consultez le fichier [Lisez-moi Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown).

## <a name="how-to-generate-a-master-redirect-file"></a>Comment générer un fichier de redirection maître

L’extension Docs Markdown comprend un script permettant de générer ou de mettre à jour un fichier de redirection maître pour un dépôt, en fonction de la métadonnée `redirect_url` dans des fichiers individuels. Ce script recherche `redirect_url` dans chaque fichier Markdown du dépôt, ajoute les métadonnées de redirection au fichier de redirection maître ( *.openpublishing.redirection.json*) pour le dépôt et déplace les fichiers redirigés vers un dossier à l’extérieur du dépôt. Pour exécuter le script :

1. Sélectionnez <kbd>F1</kbd> pour ouvrir la palette de commandes VS Code.
2. Commencez à taper « Docs: Generate... »
3. Sélectionnez la commande `Docs: Generate master redirection file`.
4. Une fois l’exécution du script terminée, les résultats de la redirection s’affichent dans le volet de sortie VS Code, et les fichiers Markdown supprimés sont ajoutés au dossier Docs Authoring\redirects sous votre chemin par défaut.
5. Passez en revue les résultats. S’ils sont conformes à vos attentes, envoyez une demande de tirage (pull request) pour mettre à jour le dépôt.

## <a name="how-to-assign-keyboard-shortcuts"></a>Comment définir des raccourcis clavier

1. Tapez <kbd>Ctrl+K</kbd> puis <kbd>Ctrl+S</kbd> pour ouvrir la **liste des raccourcis clavier**.
1. Recherchez la commande pour laquelle vous souhaitez créer une combinaison de touches personnalisée, par exemple `formatBold`.
1. Cliquez sur le signe plus qui apparaît près du nom de la commande quand vous pointez sur la ligne.
1. À l’apparition d’une nouvelle zone d’entrée, tapez le raccourci clavier à associer à cette commande particulière. Par exemple, pour utiliser le raccourci courant de mise en gras, tapez <kbd>Ctrl+G</kbd>.
1. Il est conseillé d’insérer une clause `when` dans votre combinaison de touches pour que celle-ci soit uniquement disponible dans les fichiers Markdown. Pour ce faire, ouvrez *keybindings.json* et insérez la ligne suivante sous le nom de la commande (veillez à ajouter une virgule entre les lignes) :

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    Au final, votre combinaison de touches personnalisée doit ressembler à ceci dans *keybindings.json* :

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > Placez vos combinaisons de touches dans ce fichier pour remplacer les valeurs par défaut.

1. Enregistrez *keybindings.json*.

Pour plus d’informations sur les combinaisons de touches, consultez la [documentation VS Code](https://code.visualstudio.com/docs/getstarted/keybindings).

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>Comment afficher la barre d’outils « Gauntlet » héritée

Les utilisateurs de l’ancienne extension (nom de code « Gauntlet ») remarqueront que la barre d’outils de création n’apparaît plus en bas de la fenêtre VS Code quand l’extension Docs Markdown est installée. En effet, la barre d’outils prenait une place importante sur la barre d’état de VS Code et ne suivait pas les bonnes pratiques en matière d’expérience utilisateur pour les extensions. Elle est donc dépréciée dans la nouvelle extension. Vous pouvez tout de même afficher la barre d’outils en mettant à jour votre fichier VS Code settings.json comme suit :

1. Dans VS Code, accédez à **Fichier** > **Préférences** > **Paramètres** ou sélectionnez <kbd>Ctrl+,</kbd>.
1. Sélectionnez **Paramètres utilisateur** pour changer les paramètres de tous les espaces de travail VS Code ou **Paramètres de l’espace de travail** pour les changer uniquement dans l’espace de travail actif.
1. Sélectionnez **Extensions** > **Docs Markdown Extension Configuration** (Configuration de l’extension Docs Markdown), puis sélectionnez **Show the legacy toolbar in the bottom status bar** (Afficher la barre d’outils héritée dans la barre d’état inférieure).

   ![Afficher le paramètre de barre d’outils héritée dans VS Code](docs-authoring/media/show-gauntlet-bar.png)

Une fois votre sélection effectuée, VS Code met à jour le fichier *settings.json*. Vous êtes ensuite invité à recharger la fenêtre pour que les modifications prennent effet.

Les commandes plus récentes ajoutées à l’extension ne sont pas disponibles à partir de la barre d’outils.

## <a name="how-to-use-docs-templates"></a>Utilisation des modèles Docs

L’extension Docs Article Templates permet à ceux qui écrivent en VS Code d’extraire un modèle Markdown à partir d’un magasin centralisé et de l’appliquer à un fichier. Les modèles peuvent permettre de s’assurer que les métadonnées requises sont incluses dans les articles, que les normes relatives au contenu sont respectées, etc. Les modèles sont gérés en tant que fichiers Markdown dans un référentiel GitHub public.

### <a name="to-apply-a-template-in-vs-code"></a>Pour appliquer un modèle dans VS Code

1. Vérifiez que l’extension Docs Article Templates est installée et activée.
1. Si l’extension Docs Markdown n’est pas installée, cliquez sur <kbd>F1</kbd> pour ouvrir la palette de commandes, commencez à taper « template » pour filtrer les résultats, puis cliquez sur `Docs: Template`. Si l’extension Docs Markdown est installée, vous pouvez utiliser la palette de commandes ou vous pouvez cliquer sur <kbd>Alt+M</kbd> pour afficher le menu Docs Markdown QuickPick, puis sélectionnez `Template` dans la liste.
1. Sélectionnez le modèle requis dans la liste qui s’affiche.

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a>Pour ajouter votre ID GitHub et/ou votre alias Microsoft à vos paramètres VS Code

L’extension Templates prend en charge trois champs de métadonnées dynamiques : author, ms.author et ms.date. Cela signifie que si le créateur d’un modèle utilise ces champs dans l’en-tête des métadonnées d’un modèle Markdown, ces champs seront renseignés automatiquement dans votre fichier lorsque vous appliquez le modèle, comme suit :

| Champ de métadonnées | Valeur |
|--|--|
| `author` | Votre alias GitHub, si spécifié dans le fichier des paramètres VS Code. |
| `ms.author` | Votre alias Microsoft, si spécifié dans le fichier des paramètres VS Code. Si vous n’êtes pas un employé de Microsoft, ne renseignez pas ce champ. |
| `ms.date` | La date actuelle au format pris en charge par Docs, `MM/DD/YYYY`. La date n’est pas automatiquement mise à jour si vous mettez à jour le fichier par la suite : vous devez la mettre à jour manuellement. Ce champ est utilisé pour indiquer « l’actualisation de l’article ». |

### <a name="to-set-author-andor-msauthor"></a>Pour définir author et/ou ms.author

1. Dans VS Code, accédez à **Fichier** > **Préférences** > **Paramètres** ou sélectionnez <kbd>Ctrl+,</kbd>.
1. Sélectionnez **Paramètres utilisateur** pour changer les paramètres de tous les espaces de travail VS Code ou **Paramètres de l’espace de travail** pour les changer uniquement dans l’espace de travail actif.
1. Dans le volet Paramètres par défaut à gauche, recherchez **Docs Article Templates Extension Configuration**, cliquez sur l’icône crayon en regard du paramètre requis, puis cliquez sur Remplacer dans les paramètres.
1. Le volet **Paramètres utilisateur** s’ouvre à côté et contient une nouvelle entrée en bas.
1. Ajoutez votre ID GitHub ou votre alias e-mail Microsoft, le cas échéant, et enregistrez le fichier.
1. Vous devrez peut-être fermer et redémarrer VS Code pour que les modifications prennent effet.
1. À présent, lorsque vous appliquez un modèle qui utilise des champs dynamiques, votre ID GitHub et/ou votre alias Microsoft sera automatiquement renseigné dans l’en-tête des métadonnées.

### <a name="to-make-a-new-template-available-in-vs-code"></a>Pour rendre un nouveau modèle disponible dans VS Code

1. Ébauchez votre modèle en tant que fichier Markdown.
1. Envoyez une demande de tirage (pull request) au dossier templates du dépôt [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates).

L’équipe docs.microsoft.com passe en revue votre modèle et fusionne la demande de tirage si elle répond aux règles de style docs.microsoft.com. Une fois fusionné, le modèle est disponible pour tous les utilisateurs de l’extension Docs Article Templates.

## <a name="demo-several-features"></a>Démonstration de plusieurs fonctionnalités

Voici une brève vidéo qui illustre les fonctionnalités suivantes du Docs Authoring Pack :

* **Fichiers YAML**
  * Prise en charge de « Docs : Lien vers un fichier dans le dépôt »
* **Fichiers Markdown**
  * Option de menu contextuel permettant de mettre à jour la valeur de la métadonnée « ms.date »
  * Prise en charge de l’autocomplétion du code pour les identificateurs de langage de délimitation de code
  * Avertissements d’identificateur de langage de délimitation de code non reconnu / prise en charge de la correction automatique
  * Trier la sélection par ordre croissant (de A à Z)
  * Trier la sélection par ordre décroissant (Z à A)

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a>Attentes autour des contributions

L’extension Docs Authoring Pack est open source et toute personne disposant d’un compte GitHub peut l’utiliser à des fins de contribution. Une équipe Microsoft interne dédiée travaille activement sur ce projet. Cette équipe supervise les problèmes et les demandes de tirage (pull requests). Le contrat de niveau de service (SLA) et le délai attendu de la révision d’une demande de tirage (pull request) sont d’une semaine. Les procédures de l’équipe font l’objet d’efforts d’automatisation visant à améliorer ce délai dans le temps.

## <a name="next-steps"></a>Étapes suivantes

Explorez les diverses fonctionnalités disponibles dans l’extension Visual Studio Code Docs Authoring Pack.

* [Complétion des langages de développement](docs-authoring/dev-lang-completion.md)
* [Compression d’image](docs-authoring/image-compression.md)
* [Mises à jour des métadonnées](docs-authoring/metadata-updates.md)
* [Modifier la mise en forme des tableaux](docs-authoring/reformat-table.md)
* [Remplacement des guillemets courbes](docs-authoring/smart-quote-replacement.md)
* [Trier les redirections](docs-authoring/sort-redirects.md)
* [Trier la sélection](docs-authoring/sort-selection.md)
