---
title: Informations de référence sur Markdown pour docs.microsoft.com
description: Découvrez la syntaxe et les fonctionnalités Markdown utilisées dans la plateforme Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 03/31/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: f0aed4ebb57ee1ce34f55d9085bab718fd4511cb
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624726"
---
# <a name="docs-markdown-reference"></a>Informations de référence sur Docs Markdown

Cet article fournit des informations de référence par ordre alphabétique, qui facilitent l’écriture de Markdown pour docs.microsoft.com (Docs).

[Markdown](https://daringfireball.net/projects/markdown/) est un langage de balisage léger avec une syntaxe de mise en forme en texte brut. Docs prend en charge le Markdown conforme à [CommonMark](https://commonmark.org/) analysé via le moteur d’analyse [Markdig](https://github.com/lunet-io/markdig). Docs prend également en charge les extensions Markdown personnalisées qui fournissent du contenu plus riche sur le site Docs.

Vous pouvez utiliser n’importe quel éditeur de texte pour écrire du Markdown, mais nous vous recommandons [Visual Studio Code](https://code.visualstudio.com/) avec le [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack). Le Docs Authoring Pack fournit des outils d’édition et des fonctionnalités d’aperçu qui vous permettent de voir à quoi ressemblent vos articles une fois affichés sur Docs.

## <a name="alerts-note-tip-important-caution-warning"></a>Alertes (Remarque, Conseil, Important, Attention, Avertissement)

Les alertes sont une extension Markdown pour créer des citations qui s’affichent sur docs.microsoft.com avec des couleurs et des icônes indiquant la signification du contenu. Les types d’alerte suivants sont pris en charge :

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

Ces alertes ressemblent à ceci sur docs.microsoft.com :

> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.

### <a name="angle-brackets"></a>Crochets pointus

Si vous utilisez des crochets pointus dans le texte de votre fichier, par exemple pour signaler un espace réservé, vous devez manuellement encoder les crochets pointus. Sinon, Markdown considère qu’il s’agit d’une balise HTML.

Par exemple, encodez `<script name>` en `&lt;script name&gt;` ou `\<script name>`.

Les crochets pointus n’ont pas besoin d’être placés dans une séquence d’échappement dans du texte mis en forme en tant que code inline ou dans des blocs de code.

## <a name="apostrophes-and-quotation-marks"></a>Apostrophes et guillemets

Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes. Vous devez les encoder ou les changer en apostrophes/guillemets de base. Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ&euro;&trade;s

Voici les encodages pour les versions courbes de ces signes de ponctuation :

- Guillemet gauche (ouvrant) : `&#8220;`
- Guillemet droit (fermant) : `&#8221;`
- Guillemet simple droit (fermant) ou apostrophe : `&#8217;`
- Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`

## <a name="blockquotes"></a>Éléments blockquote

Pour créer un élément blockquote, vous utilisez le caractère `>` :

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

L’exemple précédent s’affiche comme suit :

> Il s’agit d’un bloc de citation. Il est généralement affiché en retrait et avec une couleur d’arrière-plan différente.

## <a name="bold-and-italic-text"></a>Texte en gras et italique

Pour mettre en forme le texte en **gras**, entourez-le de deux astérisques :

```markdown
This text is **bold**.
```

Pour mettre en forme le texte en *italique*, entourez-le d’un seul astérisque :

```markdown
This text is *italic*.
```

Pour mettre en forme le texte en ***gras et en italique***, entourez-le de trois astérisques :

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a>Extraits de code

Docs Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases. Pour plus d’informations, consultez [Guide pratique pour ajouter du code à la documentation](code-in-docs.md).

## <a name="columns"></a>Colonnes

L’extension Markdown pour les **colonnes** donne aux auteurs de documentation la possibilité d’ajouter des dispositions de contenu basées sur des colonnes qui sont plus flexibles et plus puissantes que les tableaux Markdown de base, qui sont adaptés uniquement aux données véritablement tabulaires. Vous pouvez ajouter jusqu’à quatre colonnes et utiliser l’attribut facultatif `span` pour fusionner deux colonnes ou plus.

La syntaxe des colonnes est la suivante :

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

Les colonnes doivent contenir uniquement du Markdown de base, y compris des images. Les en-têtes, tableaux, onglets et autres structures complexes ne doivent pas être inclus. Une ligne ne peut pas avoir de contenu en dehors de la colonne.

Par exemple, le Markdown suivant crée une colonne qui s’étend sur deux largeurs de colonne et une colonne standard (pas de `span`) :

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

Ce code est restitué comme suit :

:::row:::
   :::column span="2":::
      **Il s’agit d’une colonne à double étendue qui contient beaucoup de texte.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **Il s’agit d’une colonne à étendue unique avec une image.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a>En-têtes

Docs prend en charge six niveaux de titres Markdown :

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Il doit y avoir un espace entre le signe `#` et le texte du titre.
- Chaque fichier Markdown doit avoir un, et un seul, titre H1.
- Le titre H1 doit être le premier contenu du fichier après le bloc de métadonnées YML.
- Les titres H2 apparaissent automatiquement dans le menu de navigation de droite du fichier publié. Les titres de niveau inférieur n’apparaissant pas, privilégiez l’utilisation de titres H2 pour aider les lecteurs à parcourir votre contenu.
- Les titres HTML, comme `<h1>`, ne sont pas recommandés. En effet, dans certains cas, ils entraînent l’affichage d’avertissements de génération.
- Vous pouvez créer un lien vers des titres spécifiques dans un fichier par le biais de [liens de signet](how-to-write-links.md#explicit-anchor-links).

## <a name="html"></a>HTML

Bien que Markdown prenne en charge la syntaxe HTML inline, HTML n’est pas recommandé pour une publication sur Docs, car, sauf pour un ensemble limité de valeurs, il entraîne des avertissements ou des erreurs de génération.

## <a name="images"></a>Images

Les types de fichiers suivants sont pris en charge par défaut pour les images :

- .jpg
- .png

### <a name="standard-conceptual-images-default-markdown"></a>Images conceptuelles standard (Markdown par défaut)

La syntaxe Markdown de base pour incorporer une image est la suivante :

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Où `<alt text>` est une brève description de l’image et `<folder path>` un chemin relatif de l’image. Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants. Ce texte est également utile si le site contient un bogue qui empêche l’affichage de l’image.

Les traits de soulignement dans le texte de remplacement ne sont pas affichés correctement à moins de les placer dans une séquence d’échappement en les faisant précéder d’une barre oblique inverse (`\_`). Toutefois, ne copiez pas de noms de fichiers à utiliser comme texte de remplacement. Par exemple, au lieu de ceci :

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Écrivez ceci :

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a>Images conceptuelles standard (Docs Markdown)

L’extension `:::image:::` personnalisée Docs prend en charge les images standard, les images complexes et les icônes.

Pour les images standard, la syntaxe Markdown plus ancienne continue de fonctionner, mais la nouvelle extension est recommandée, car elle prend en charge des fonctionnalités plus puissantes, telles que la spécification d’une étendue de localisation différente de la rubrique parente. D’autres fonctionnalités avancées, telles que la sélection dans la galerie d’images partagées au lieu de la spécification d’une image locale, seront disponibles à l’avenir. La nouvelle syntaxe est la suivante :

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

Si `type="content"` (par défaut), `source` et `alt-text` sont requis.

### <a name="complex-images-with-long-descriptions"></a>Images complexes avec des descriptions longues

Vous pouvez également utiliser cette extension pour ajouter une image avec une description longue qui est lue par les lecteurs d’écran, mais qui n’est pas affichée visuellement sur la page publiée. Les descriptions longues sont une exigence d’accessibilité pour les images complexes, telles que les graphiques. La syntaxe est la suivante :

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

Si `type="complex"`, `source`, `alt-text`, une description longue et la balise `:::image-end:::` sont tous obligatoires.

### <a name="specifying-loc-scope"></a>Spécification de loc-scope

Parfois, l’étendue de localisation d’une image est différente de celle de l’article ou du module qui la contient. Cela peut entraîner une mauvaise expérience globale, par exemple, si une capture d’écran d’un produit est accidentellement localisée dans une langue dans laquelle le produit n’est pas disponible. Pour éviter cela, vous pouvez spécifier l’attribut `loc-scope` facultatif dans les images de types `content` et `complex`.

### <a name="icons"></a>Icônes

L’extension d’image prend en charge les icônes, qui sont des images décoratives et qui ne doivent pas comporter de texte de remplacement. La syntaxe des icônes est la suivante :

```Markdown
:::image type="icon" source="<folderPath>":::
```

Si `type="icon"`, seul `source` doit être spécifié.

## <a name="included-markdown-files"></a>Fichiers Markdown inclus

Quand des fichiers Markdown doivent être répétés dans plusieurs articles, vous pouvez utiliser un fichier include. La fonctionnalité d’includes indique à Docs de remplacer la référence par le contenu du fichier include au moment de la génération. Vous pouvez utiliser des includes de la façon suivante :

- Inline : pour réutiliser un extrait de texte commun au sein d’une phrase.
- Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.

Un fichier include de type inline ou bloc est un fichier Markdown (.md). Il peut contenir tout code Markdown valide. Les fichiers include se trouvent généralement dans un sous-répertoire *includes* commun, à la racine du dépôt. Quand l’article est publié, le fichier inclus y est intégré de façon transparente.

### <a name="includes-syntax"></a>Syntaxe des includes

Un include sous forme de bloc occupe une ligne à part :

```markdown
[!INCLUDE [<title>](<filepath>)]
```

Un include inline se trouve à l’intérieur d’une ligne :

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

Où `<title>` est le nom du fichier et `<filepath>` le chemin relatif du fichier. `INCLUDE` doit être en majuscule et un espace doit figurer avant `<title>`.

Voici les conditions requises et éléments à prendre en compte pour les fichiers include :

- Utilisez des includes de blocs pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée. Ne l'utilisez pas pour des éléments plus petits qu'une phrase.
- Les includes ne s’afficheront pas dans la vue de votre article rendu par GitHub, car ils reposent sur des extensions Docs. Ils ne sont rendus qu’après publication.
- Vérifiez que tout le texte dans un fichier include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence l’include. Le fait d’ignorer cette instruction crée une chaîne intraduisible dans l’article.
- N’incorporez pas de fichiers include dans d’autres fichiers include.
- Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>` */includes/media*. Le répertoire *media* ne doit pas contenir d’images à sa racine. Si l’include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire *media* correspondant.
- Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include. Utilisez un fichier distinct avec un nom unique pour chaque include et article. Stockez le fichier multimédia dans le dossier multimédia associé à l’include.
- N'utilisez pas un include comme seul contenu d'un article.  Les includes sont censés compléter le contenu du reste de l'article.

## <a name="links"></a>Liens

Pour plus d’informations sur la syntaxe des liens, consultez [Utiliser des liens dans la documentation](how-to-write-links.md).

## <a name="lists-numbered-bulleted-checklist"></a>Listes (numérotées, à puces, liste de contrôle)

### <a name="numbered-list"></a>Liste numérotée

Pour créer une liste numérotée, vous pouvez utiliser uniquement des 1. Les nombres sont affichés dans l’ordre croissant sous la forme d’une liste séquentielle au moment de la publication. Pour accroître la lisibilité du texte source, vous pouvez incrémenter vos listes manuellement.

N’utilisez pas de lettres dans les listes, y compris dans les listes imbriquées. Elles ne sont pas restituées correctement au moment de la publication sur Docs. Les listes imbriquées utilisant des nombres sont restituées avec des lettres minuscules au moment de la publication. Par exemple :

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

Ce code est restitué comme suit :

1. This is
1. a parent numbered list
   1. and this is
   1. a parent numbered list
1. (fin)

### <a name="bulleted-list"></a>Liste à puces

Pour créer une liste à puces, utilisez `-` ou `*` suivi d’un espace au début de chaque ligne :

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

Ce code est restitué comme suit :

- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!

Quelle que soit la syntaxe que vous utilisez, `-` ou `*`, utilisez-la de manière cohérente dans un article.

### <a name="checklist"></a>Liste de contrôle

Les listes de contrôle sont utilisables sur Docs par le biais d’une extension Markdown personnalisée :

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Cet exemple s’affiche sur Docs ainsi :

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Utilisez des listes de contrôle au début ou à la fin d’un article pour récapituler le contenu que l’utilisateur va étudier ou a étudié. N’ajoutez pas de listes de contrôle aléatoires dans vos articles.

## <a name="next-step-action"></a>Action d’étape suivante

Vous pouvez utiliser une extension personnalisée pour ajouter un bouton d’action d’étape suivante à des pages Docs.

La syntaxe est la suivante :

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Par exemple :

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

Ce code est restitué comme suit :

> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)

Vous pouvez utiliser n’importe quel lien pris en charge dans une action d’étape suivante, y compris un lien Markdown vers une autre page web. Dans la plupart des cas, le lien d’action suivante est un lien relatif vers un autre fichier de le même docset.

## <a name="non-localized-strings"></a>Chaînes non localisées

Vous pouvez utiliser l’extension Markdown `no-loc` personnalisée pour identifier les chaînes de contenu que le processus de localisation doit ignorer.

Toutes les chaînes appelées sont sensibles à la casse ; autrement dit, une chaîne doit correspondre exactement pour être ignorée au moment de la localisation.

Pour marquer une chaîne individuelle comme non localisable, utilisez la syntaxe suivante :

```markdown
:::no-loc text="String":::
```

Par exemple, dans le code suivant, seule l’instance unique de `Document` est ignorée au cours du processus de localisation :

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> Utilisez `\` pour placer les caractères spéciaux dans une séquence d’échappement:
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

Vous pouvez également utiliser des métadonnées dans l’en-tête YAML pour marquer toutes les instances d’une chaîne dans le fichier Markdown actuel comme non localisables :

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> Les métadonnées no-loc ne sont pas prises en charge en tant que métadonnées globales dans le fichier *docfx.json*. Le pipeline de localisation ne lit pas le fichier *docfx.json*. Ainsi, les métadonnées no-loc doivent être ajoutées à chaque fichier source individuel.

Dans l’exemple suivant, à la fois dans la métadonnée `title` et dans l’en-tête Markdown, le mot `Document` est ignoré au cours du processus de localisation.

Dans la métadonnée `description` et le contenu principal de Markdown, le mot `document` est localisé, car il ne commence pas par un `D` majuscule.

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a>Des sélecteurs

Les sélecteurs sont des éléments d’interface utilisateur qui permettent à l’utilisateur de basculer entre plusieurs versions du même article. Ils sont utilisés dans certains docsets pour résoudre les différences d’implémentation entre les technologies et les plateformes. Les sélecteurs s’appliquent particulièrement au contenu pour plateformes mobiles pour développeurs.

Le même Markdown de sélecteur allant dans chaque fichier d’article qui utilise le sélecteur, nous vous recommandons de placer le sélecteur pour votre article dans un fichier include. Vous pouvez ensuite référencer ce dernier dans tous vos fichiers d’article qui utilisent le même sélecteur.

Il existe deux types de sélecteurs : sélecteur unique et sélecteur multiple.

### <a name="single-selector"></a>Sélecteur unique

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

... s’affiche ainsi :

> [!div class="op_single_selector"]
> - [Windows universel](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a>Sélecteur multiple

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

... s’affiche ainsi :

> [!div class="op_multi_selector" title1="Plateforme" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universel C# | .NET)](how-to-write-links.md)
> - [(Windows universel C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a>Indice et exposant

Vous devez uniquement utiliser un indice ou un exposant quand cela est nécessaire pour une précision technique, par exemple lors de l’écriture de formules mathématiques. Ne les utilisez pas pour les styles non standard, tels que les notes de bas de page.

Pour exprimer du contenu sous forme d’indice ou d’exposant, utilisez HTML :

```html
Hello <sub>This is subscript!</sub>
```

Ce code est restitué comme suit :

Hello <sub>This is subscript!</sub>

```html
Goodbye <sup>This is superscript!</sup>
```

Ce code est restitué comme suit :

Goodbye <sup>This is superscript!</sup>

## <a name="tables"></a>Les tableaux

Le moyen le plus simple de créer un tableau en Markdown est d’utiliser des barres verticales et des lignes. Pour créer un tableau standard avec un en-tête, faites suivre la première ligne d’une ligne en pointillés :

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

Ce code est restitué comme suit :

|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!||

Vous pouvez aligner les colonnes à l’aide de signes deux-points :

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

Ce code est restitué comme suit :

| Fun                  | With                 | Les tableaux          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

> [!TIP]
> L’extension Docs Authoring pour VS Code facilite l’ajout de tableaux Markdown simples !
>
> Vous pouvez également utiliser un [ générateur de tableau en ligne](http://www.tablesgenerator.com/markdown_tables).

### <a name="line-breaks-within-words-in-any-table-cell"></a>Sauts de ligne dans les mots d’une cellule de tableau

Les mots longs dans un tableau Markdown peuvent amener ce dernier à s’étendre sur la barre de navigation de droite au point de devenir illisible. Vous pouvez résoudre cela en autorisant le rendu Docs à insérer automatiquement des sauts de ligne dans les mots, si nécessaire. Pour cela, il vous suffit d’encapsuler le tableau avec la classe personnalisée `[!div class="mx-tdBreakAll"]`.

Voici un exemple de code Markdown d’un tableau, avec trois lignes encapsulées par un `div`, avec le nom de classe `mx-tdBreakAll`.

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

Cela s’affiche ainsi :

> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a>Sauts de ligne dans les mots au sein des cellules de la deuxième colonne d’un tableau

Vous souhaiterez peut-être insérer automatiquement des sauts de ligne dans les mots de la deuxième colonne d’un tableau uniquement. Pour limiter les arrêts à la deuxième colonne, appliquez la classe `mx-tdCol2BreakAll` à l’aide de la syntaxe de wrapper `div`, comme indiqué plus haut.

### <a name="data-matrix-tables"></a>Tables de matrices de données

Une table de matrice de données contient une en-tête et une première colonne pondérée. Une matrice avec une cellule vide est créée en haut à gauche. Docs contient Markdown personnalisé pour les tables de la matrice de données :

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

Chaque entrée de la première colonne doit avoir le style gras (`**bold**`) ; sinon, les tables ne sont pas accessibles pour les lecteurs d’écran ou ne sont pas valides pour Docs.

### <a name="html-tables"></a>Tableaux HTML

Les tableaux HTML ne sont pas recommandés dans docs.microsoft.com. Ils ne se présentent pas sous une forme conviviale dans le source, ce qui va à l’encontre d’un principe essentiel de Markdown.
