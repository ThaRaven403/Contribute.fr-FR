---
title: Informations de référence sur Markdown pour docs.microsoft.com
description: Découvrez la syntaxe et les fonctionnalités Markdown utilisées dans la plateforme Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: a5ff6c5122a08d2b611fd6b0344a6f5740d93928
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592561"
---
# <a name="markdown-reference"></a>Informations de référence sur Markdown

Markdown est un langage de balisage léger avec une syntaxe de mise en forme en texte brut. La plateforme Docs prend en charge la norme CommonMark pour Markdown, ainsi que certaines extensions Markdown personnalisées conçues pour fournir du contenu enrichi sur docs.microsoft.com. Cet article fournit des informations de référence par ordre alphabétique, qui facilitent l’utilisation de Markdown pour docs.microsoft.com.

Vous pouvez utiliser n’importe quel éditeur de texte pour créer du contenu Markdown. Comme éditeur facilitant l’insertion à la fois d’une syntaxe Markdown standard et d’extensions Docs personnalisées, nous recommandons [VS Code](https://code.visualstudio.com/) avec le [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installé.

Docs utilise le moteur Markdown Markdig. Vous pouvez tester le rendu de Markdown dans Markdig par rapport à d’autre moteurs sur [https://babelmark.github.io/](https://babelmark.github.io/).

## <a name="alerts-note-tip-important-caution-warning"></a>Alertes (Remarque, Conseil, Important, Attention, Avertissement)

Les alertes sont une extension Markdown Docs pour créer des citations qui s’affichent sur docs.microsoft.com avec des couleurs et des icônes indiquant la signification du contenu. Les types d’alerte suivants sont pris en charge :

```md
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

![montre comment les alertes de l’exemple précédent apparaissent sur la page Documentation publiée avec les différentes icônes et couleurs](media/alerts-rendering.png)

## <a name="code-snippets"></a>Extraits de code

Vous pouvez incorporer des extraits de code dans vos fichiers Markdown :

```md
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a>En-têtes

Docs prend en charge six niveaux de titres Markdown :

```md
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- Il doit y avoir un espace entre le signe `#` et le texte du titre.
- Chaque fichier Markdown doit avoir un, et un seul, titre H1.
- Le titre H1 doit être le premier contenu du fichier après le bloc de métadonnées YML.
- Les titres H2 apparaissent automatiquement dans le menu de navigation de droite du fichier publié. Ce n’est pas le cas des titres de niveau inférieur, donc privilégiez l’utilisation de titres H2 pour aider les lecteurs à parcourir votre contenu.
- Les titres HMTL, comme `<h1>`, ne sont pas recommandés. En effet, dans certains cas, ils entraînent l’affichage d’avertissements de génération.
- Vous pouvez créer un lien vers des titres spécifiques dans un fichier par le biais de [signets](#bookmark-links).

## <a name="html"></a>HTML

Bien que Markdown prenne en charge la syntaxe HTML inline, HTML n’est pas recommandé pour une publication sur Docs, car, sauf pour un ensemble limité de valeurs, il entraîne des avertissements ou des erreurs de génération.

## <a name="images"></a>Images

La syntaxe pour inclure une image est :

```md
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

Où `alt text` est une brève description de l’image et `<folder path>` un chemin relatif de l’image. Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants. Ce texte est également utile si le site contient un bogue qui empêche l’affichage de l’image.

Les images doivent être stockées dans un dossier `/media` au sein de votre documentation. Les types de fichiers suivants sont pris en charge par défaut pour les images :

- .jpg
- .png

Vous pouvez ajouter la prise en charge d’autres types d’image en les ajoutant comme ressources au fichier docfx.json<!--add link to reference when available--> de votre documentation.

## <a name="links"></a>Liens

Dans la plupart des cas, Docs utilise des liens Markdown standard vers d’autres fichiers et pages. Les types de liens sont décrits dans des sous-sections plus loin.

> [!TIP]
> Le Docs Authoring Pack pour VS Code peut aider à insérer correctement des signets et des liens relatifs sans avoir à deviner les chemins !

> [!IMPORTANT]
> N’incluez pas de codes de paramètres régionaux, comme en-us, dans vos liens vers des sites Microsoft. Les codes de paramètres régionaux codés en dur empêchent l’affichage du contenu traduit, ce qui procure une mauvaise expérience aux utilisateurs dans d’autres paramètres régionaux et engendre des coûts de traduction significatifs. Quand vous copiez une URL à partir d’un navigateur, le code de paramètres régionaux est inclus par défaut ; vous devez le supprimer manuellement quand vous créez votre lien. Par exemple, utilisez :
>
> `[Microsoft](https://www.microsoft.com)`
>
> Pas :
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a>Liens relatifs vers des fichiers de la même documentation

Un chemin relatif est le chemin du fichier cible par rapport au fichier actuel. Dans Docs, vous pouvez utiliser un chemin relatif pour créer un lien vers un autre fichier de la même documentation. La syntaxe d’un chemin relatif est la suivante :

```md
[link text](../../folder/filename.md)
```

Où `../` indique un niveau au-dessus dans la hiérarchie.

- Le chemin relatif est résolu pendant la génération, qui inclut la suppression de l’extension .md.
- Vous pouvez utiliser « ../ » pour créer un lien vers le fichier dans le dossier parent, mais ce fichier doit se trouver dans la même documentation. Vous ne pouvez pas utiliser « ../ » pour créer un lien vers un fichier d’une autre documentation.
- Docs prend également en charge une forme spéciale de chemin relatif qui commence par « ~ » (par exemple, ~/foo/bar.md). Cette syntaxe indique un fichier par rapport au dossier racine d’une documentation. Ce genre de chemin est aussi validé et résolu pendant la génération.

> [!IMPORTANT]
> Ajoutez l’extension de fichier dans le chemin relatif. La génération valide l’existence du fichier cible de ce chemin relatif. Si le chemin relatif n’inclut pas d’extension de fichier, il est probable qu’un avertissement de lien rompu apparaisse lors de la génération. Par exemple, utilisez :
>
> `[link text](../../folder/filename.md)`
>
> Pas :
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a>Liens relatifs de site vers d’autres fichiers sur Docs

```md
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

N’incluez pas l’extension de fichier (.md). Ce lien dirige vers le fichier Linux « overview » depuis l’extérieur de la documentation Azure « articles ».

### <a name="links-to-external-sites"></a>Liens vers des sites externes

```md
[Microsoft](https://www.microsoft.com)
```

Lien basé sur une URL vers une autre page web (doit inclure https://).

### <a name="bookmark-links"></a>Liens de signet

Lien de signet vers un titre d’un autre fichier du même dépôt Par exemple :

```md
[Managed Disks](../../linux/overview.md#managed-disks)
```

Lien de signet vers un titre du fichier actuel :

```md
[Managed Disks](#managed-disks)
```

Utilisez un signe dièse `#` suivi des mots du titre. Pour changer le texte du titre dans le texte du lien :
- Utiliser des caractères minuscules
- Supprimer la ponctuation
- Remplacer les espaces par des tirets

Par exemple, si le nom du titre est « Problèmes de sécurité 2.2 », le texte du lien du signet sera « #problèmes-de-sécurité-22 ».

### <a name="explicit-anchor-links"></a>Liens d’ancrage explicites

Les liens d’ancrage explicites utilisant la balise HTML `<a>` **ne sont pas obligatoires ou recommandés** sauf dans les pages d’arrivée et hub. Utilisez des signets comme indiqué plus haut dans les fichiers Markdown généraux. Pour les pages hub et d’arrivée, utilisez des ancrages comme suit :

`## <a id="AnchorText"> </a>Header text` ou `## <a name="AnchorText"> </a>Header text`

Pour créer un lien vers des ancrages explicites, utilisez la syntaxe suivante :

```md
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a>Liens XREF (référence croisée)

Pour créer un lien vers des pages de références d’API générées automatiquement dans la documentation actuelle ou dans d’autres documentations, utilisez des liens XREF avec l’ID unique (UID).

> [!NOTE]
> Pour référencer des pages de références d’API dans d’autres jeux de documentation, vous devez ajouter la configuration `xrefService` dans le fichier `docfx.json`.
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

L’UID équivaut au nom complet de la classe et du membre. Si vous ajoutez un * après l’UID, le lien représente alors la page de la surcharge et non pas une API spécifique. Par exemple, utilisez `List<T>.BinarySearch*` pour créer un lien vers la page Méthode BinarySearch au lieu de créer un lien vers une surcharge spécifique telle que `List<T>.BinarySearch(T, IComparer<T>)`.

Vous pouvez utiliser une des syntaxes suivantes :

- Lien automatique : `<xref:UID> or <xref:UID?displayProperty=nameWithType>`

  Le paramètre de requête `displayProperty` facultatif produit un texte de lien complet. Par défaut, le texte du lien montre seulement le nom du membre ou du type.

- Lien Markdown : `[link text](xref:UID)`
  
  À utiliser quand vous voulez personnaliser le texte du lien affiché.

Exemples :

- `<xref:System.String>` s’affiche sous la forme « String ».
- `<xref:System.String?displayProperty=nameWithType>` s’affiche sous la forme « System.String ».
- `[String class](xref:System.String)` s’affiche sous la forme « String class ».

Il n’existe actuellement aucun moyen facile de trouver les UID. <!-- ? -->La meilleure façon de trouver l’UID pour une API consiste à afficher la source de la page de l’API vers laquelle vous voulez créer un lien et à rechercher la valeur de ms.assetid. Les valeurs des surcharges individuelles ne figurent pas dans la source. Nous nous efforçons de mettre au point un meilleur système dans le futur.

Quand l’UID contient les caractères spéciaux \`, \# ou \*, la valeur de l’UID doit être encodée en HTML en tant que `%60`, `%23` et `%2A`, respectivement. Vous pouvez parfois trouver des parenthèses dans l’encodage, mais elles ne sont pas obligatoires.

Exemples :

- System.Threading.Tasks.Task\`1 devient `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor devient `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) devient `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a>Listes (numérotées, à puces, liste de contrôle)

### <a name="numbered-list"></a>Liste numérotée

Pour créer une liste numérotée, vous pouvez utiliser exclusivement des « 1 », qui sont restitués sous la forme d’une liste séquentielle au moment de la publication. Pour accroître la lisibilité du texte source, vous pouvez incrémenter vos listes.

N’utilisez pas de lettres dans les listes, y compris dans les listes imbriquées. Elles ne sont pas restituées correctement au moment de la publication sur Docs. Les listes imbriquées utilisant des nombres sont restituées avec des lettres minuscules au moment de la publication. Par exemple :

```md
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

Pour créer une liste à puces, utilisez `-` suivi d’un espace au début de chaque ligne :

```md
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

### <a name="checklist"></a>Liste de contrôle

Les listes de contrôle sont utilisables sur docs.microsoft.com (uniquement) par le biais d’une extension Markdown personnalisée :

```md
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

Cet exemple s’affiche sur docs.microsoft.com ainsi :

> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3

Utilisez des listes de contrôle au début ou à la fin d’un article pour récapituler le contenu que l’utilisateur va étudier ou a étudié. N’ajoutez pas de listes de contrôle aléatoires dans vos articles.
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a>Action d’étape suivante

Vous pouvez utiliser une extension personnalisée pour ajouter un bouton d’action d’étape suivante à des pages sur docs.microsoft.com (uniquement).

La syntaxe est la suivante :

```md
> [!div class="nextstepaction"]
> [button text](link to topic)
```

Par exemple :

```md
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

Ce code est restitué comme suit :

> [!div class="nextstepaction"]
> [Découvrir le style simple](style-quick-start.md)

Vous pouvez utiliser n’importe quel lien pris en charge dans une action d’étape suivante, y compris un lien Markdown vers une autre page web. Dans la plupart des cas, le lien d’action suivante est un lien relatif vers un autre fichier de la même documentation.

## <a name="section-definition"></a>Définition de section

<!-- more info about this would be helpful! -->
Vous aurez peut-être à définir une section. Cette syntaxe est principalement utilisée pour les tables de code.
Regardez l’exemple suivant :

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

Le texte Markdown de citation précédent s’affiche ainsi :
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a>Des sélecteurs

<!-- could be more clear! -->
Vous pouvez utiliser un sélecteur pour lier plusieurs pages d’un même article. Les lecteurs peuvent ainsi passer d’une page à l’autre.

> [!NOTE]
> Cette extension fonctionne différemment sur docs.microsoft.com et sur MSDN. <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a>Sélecteur unique

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

... s’affiche ainsi :

> [!div class="op_single_selector"]
> - [Windows universel](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a>Sélecteur multiple

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

... s’affiche ainsi :

> [!div class="op_multi_selector" title1="Plateforme" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universel C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universel C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

## <a name="tables"></a>les tableaux

Le moyen le plus simple de créer un tableau en Markdown est d’utiliser des barres verticales et des lignes. Pour créer un tableau standard avec un en-tête, faites suivre la première ligne d’une ligne en pointillés :

```md
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

Vous pouvez également créer un tableau sans en-tête. Par exemple, pour créer une liste à plusieurs colonnes :

```md
|   |   |
| - | - |
| This | table |
| has no | header |
```

Ce code est restitué comme suit :

|   |   |
| - | - |
| This | table |
| has no | header |

Vous pouvez aligner les colonnes à l’aide de signes deux-points :

```md
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

Ce code est restitué comme suit :

|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|

> [!TIP]
> L’extension Docs Authoring pour VS Code facilite l’ajout de tableaux Markdown simples !
>
> Vous pouvez également utiliser un [ générateur de tableau en ligne](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a>mx-tdBreakAll

> [!IMPORTANT]
> Cette classe fonctionne uniquement sur le site docs.microsoft.com.

Si vous créez un tableau en Markdown, le tableau peut s’étendre sur la barre de navigation de droite et devient alors illisible. Vous pouvez résoudre ce problème en permettant à l’affichage Docs de scinder le tableau. Pour cela, il vous suffit d’encapsuler le tableau avec la classe personnalisée `[!div class="mx-tdBreakAll"]`.

Voici un exemple de code Markdown d’un tableau, avec trois lignes encapsulées par un `div`, avec le nom de classe `mx-tdBreakAll`.

```md
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

### <a name="mx-tdcol2breakall"></a>mx-tdCol2BreakAll

> [!IMPORTANT]
> Cette classe fonctionne uniquement sur le site docs.microsoft.com.

Il arrive parfois que la deuxième colonne d’un tableau contienne de très longs mots. Pour qu’ils soient correctement scindés, vous pouvez appliquer la classe `mx-tdCol2BreakAll` à l’aide de la syntaxe du wrapper `div`, comme indiqué précédemment.

### <a name="html-tables"></a>Tableaux HTML

Les tableaux HTML ne sont pas recommandés dans docs.microsoft.com. Ils ne se présentent pas sous une forme conviviale dans le source, ce qui va à l’encontre d’un principe essentiel de Markdown.

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a>Vidéos

### <a name="embedding-videos-into-a-markdown-page"></a>Incorporation de vidéos dans une page Markdown

À l’heure actuelle, Docs peut prendre en charge les vidéos publiées sur :

- YouTube
- Canal 9
- Système « One Player » de Microsoft

Vous pouvez incorporer une vidéo avec la syntaxe suivante et permettre à Docs de l’afficher.

```md
> [!VIDEO <embedded_video_link>]
```

Exemple :

```md
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

... s’affiche ainsi :

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

Elle s’affiche ainsi sur les pages publiées :

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> L’URL de la vidéo CH9 doit commencer par `https` et se terminer par `/player`. Sinon, le code incorpore la page entière au lieu de la vidéo uniquement.

### <a name="uploading-new-videos"></a>Chargement de nouvelles vidéos

Toute nouvelle vidéo doit être chargée à l’aide du processus suivant :

1. Rejoignez le groupe **docs_video_users** sur IDWEB.
1. Accédez à https://aka.ms/VideoUploadRequest, puis indiquez les détails de votre vidéo. Munissez-vous des éléments suivants (dont aucun ne sera visible publiquement) :
    1. Titre de votre vidéo.
    1. Liste de produits/services avec lesquels votre vidéo a un lien.
    1. Page cible ou, à défaut, documentation qui hébergera votre vidéo.
    1. Lien vers le fichier MP4 de votre vidéo (si vous n’avez pas d’emplacement pour le fichier, vous pouvez le placer ici provisoirement : `\\scratch2\scratch\apex`). Les fichiers MP4 doivent être au format 720p ou supérieur.
    1. Description de la vidéo.
1. Soumettez (enregistrez) cet élément.
1. La vidéo est chargée dans un délai maximal de deux jours ouvrés. Le lien dont vous avez besoin pour l’incorporation est placé dans l’élément de travail et *vous sera rendu* prêt à l’emploi.
1. Une fois que vous avez récupéré le lien de la vidéo, fermez l’élément de travail.
1. Vous pouvez alors ajouter le lien de la vidéo à votre publication à l’aide de la syntaxe suivante :

   ```md
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
