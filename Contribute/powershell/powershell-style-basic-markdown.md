---
title: Modèle et aide-mémoire pour les articles PowerShell
description: Cet article contient un modèle pratique que vous pouvez utiliser pour créer des articles pour les dépôts de documentation PowerShell.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: e7ee9295794adfde78a2d500f0de3309dd3c821a
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290354"
---
# <a name="markdown-style-guide-for-powershell-docs"></a>Guide de style Markdown pour PowerShell-Docs

Cet article fournit des conseils de style spécifiques au contenu PowerShell-Docs.

Pour d’autres conseils sur le style d’écriture, consultez le [Guide de style Microsoft](https://docs.microsoft.com/style-guide/welcome/).

## <a name="metadata"></a>Métadonnées

Ce modèle contient des exemples de syntaxe Markdown ainsi que des conseils sur la définition des métadonnées.
Lors de la création d’un fichier Markdown, vous devez copier le modèle inclus dans un nouveau fichier, renseigner les métadonnées come indiqué ci-dessous et définir l’en-tête H1 ci-dessus dans le titre de l’article.

Le bloc de métadonnées requis se trouve dans l’exemple de bloc de métadonnées suivant :

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Vous **devez** insérer un espace entre les deux-points (:) et la valeur d’un élément de métadonnées.
- Les deux-points dans une valeur (par exemple un titre) rompent l’analyseur de métadonnées. Dans ce cas, placez le titre entre des guillemets doubles (par exemple `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **author** : le champ author doit contenir le **nom d’utilisateur GitHub** de l’auteur.
- **description** : fournit un récapitulatif du contenu de l’article. Elle est généralement affichée dans la page des résultats de la recherche, mais elle n’entre pas en compte pour le classement des recherches. Elle doit avoir une longueur comprise entre 115 et 145 caractères, espaces compris.
- **ms.date** : date de la dernière mise à jour importante. Mettez-la à jour dans les articles existants si vous avez révisé et mis à jour l’ensemble de l’article. Les petites corrections, comme les fautes de frappe ou similaires, ne nécessitent pas de mise à jour.
- **title** : apparaît dans les résultats des moteurs de recherche. Le titre ne doit pas être identique au titre de votre en-tête H1, et il doit contenir au plus 60 caractères.

D’autres métadonnées sont attachées à chaque article, mais nous appliquons en général la plupart des valeurs de métadonnées au niveau du dossier, spécifié dans **docfx.json**.

## <a name="product-terminology"></a>Terminologie du produit

Il existe plusieurs variantes de PowerShell. Ce tableau définit certains des différents termes utilisés pour parler de PowerShell.

- **PowerShell** : il s’agit du terme par défaut. PowerShell est le produit que nous livrons. Le terme PowerShell peut être utilisé pour décrire n’importe quelle édition du produit.
- **PowerShell Core** : PowerShell basé sur le CLR (Common Language Runtime) .NET Core (CoreCLR) pour toutes les plateformes prises en charge.
- **Windows PowerShell** : PowerShell basé sur le CLR (Common Language Runtime) .NET Framework. Windows PowerShell est fourni uniquement sur Windows et nécessite le CLR .NET Framework complet.

En général, les références à « Windows PowerShell » dans la documentation peuvent être remplacées par « PowerShell ».
« Windows PowerShell » ne doit **pas** être changé quand il est question de la technologie spécifique à Windows.

## <a name="basic-markdown-gfm-and-special-characters"></a>Markdown de base, GFM et caractères spéciaux

Pour découvrir les principes de base de Markdown, de GFM (GitHub Flavored Markdown) et des extensions propres à OPS, consultez les articles généraux sur [Markdown](../how-to-write-use-markdown.md) et la [référence Markdown](../markdown-reference.md).

Markdown utilise des caractères spéciaux tels que \*, \` et \# pour la mise en forme. Si vous souhaitez inclure l’un de ces caractères dans votre contenu, vous devez effectuer l’une des deux opérations suivantes :

- Placer une barre oblique inverse avant le caractère spécial pour l’« échapper » (par exemple `\*` pour \*)
- Utiliser le [code d’entité HTML](http://www.ascii.cl/htmlcodes.htm) pour le caractère (par exemple `&#42;` pour &#42;)
- Les fichiers Markdown doivent utiliser du texte ASCII brut ou l’encodage UTF-8. Évitez cependant d’utiliser des caractères UTF-8 multioctets. Utilisez à la place une entité HTML. Par exemple, pour les symboles de copyright, utilisez `&copy;`.
  Il est rendu sous la forme &copy;.

## <a name="hyperlinks"></a>Liens hypertexte

- Évitez d’utiliser des URL nues. Les liens doivent utiliser la syntaxe Markdown `[friendlyname](url-or-path)`
- Les liens doivent avoir un nom convivial, généralement le titre de la rubrique liée
- Tous les éléments de la section « Liens connexes » dans le bas doivent être liés par un lien hypertexte.
- Utilisez des liens relatifs pour lier à un autre contenu hébergé sur **docs.microsoft.com**.
- N’utilisez pas d’accents graves, du gras ou un autre balisage à l’intérieur des crochets d’un lien hypertexte.

Pour plus d’informations sur les liens, consultez [Utilisation de liens dans la documentation](../how-to-write-links.md).

## <a name="filenames"></a>Noms de fichiers

Les noms de fichiers suivent les règles ci-dessous :

- Ils contiennent seulement des lettres, des chiffres et des traits d’union.
- Ils ne doivent pas contenir d’espaces ni de caractères de ponctuation. Utilisez des traits d’union pour séparer les mots et les chiffres compris dans le nom de fichier.
- Utilisez des verbes d’action spécifiques, tels que « développer », « acheter », « créer », « dépanner », etc. Ils ne doivent pas comprendre de mots se terminant par « -ing ».
- Ils ne doivent pas comprendre de mots courts (« un », « et », « le », « en », « ou », etc.).
- Ils doivent être au format Markdown et avoir l’extension de fichier .md.
- Faites en sorte que les noms de fichiers soient le plus court possible. Ils font partie de l’URL de vos articles.

## <a name="blank-lines-spaces-and-tabs"></a>Lignes vides, espaces et tabulations

Supprimez les lignes vides en double. Les lignes vides multiples s’affichent sous la forme d’une seule ligne vide en HTML : il est donc inutile de les utiliser.

Les lignes vides indiquent aussi la fin d’un bloc dans Markdown. Il ne doit y avoir qu’un seul espace entre les blocs Markdown de différents types (par exemple entre un paragraphe et une liste ou un en-tête).

> [!NOTE]
> L’espacement a une signification dans Markdown. Utilisez toujours des espaces à la place de tabulations en dur. Supprimez les espaces en trop à la fin des lignes.

## <a name="titles-and-headings"></a>Titres et en-têtes

Utilisez uniquement des [en-têtes ATX][atx] (de style #, et non pas des en-têtes de style `=` ou `-`).

- Utilisez la casse classique des phrases : seuls les noms propres et la première lettre d’un titre ou d’un en-tête prennent une majuscule
- Il doit y avoir un seul espace entre le `#` et la première lettre du titre
- Les titres doivent être précédés et suivis d’une seule ligne vide
- Un seul titre H1 par document
- Les niveaux d’en-tête doivent être incrémentés d’une unité : ne passez pas un niveau
- N’utilisez pas d’accents graves, de gras ou un autre balisage dans les en-têtes

> [!CAUTION]
> Le schéma appliqué par [PlatyPS][platyPS] pour les informations de référence des applets de commande nécessite des en-têtes H2 et H3 spécifiques. L’ajout ou la suppression d’en-têtes peut entraîner un arrêt de la build. Pour plus d’informations, consultez le [Guide de style des informations de référence des applets de commande](powershell-style-reference.md).

## <a name="limit-line-length-to-100-characters"></a>Limitez la longueur des lignes à 100 caractères

Cela simplifie la sortie des différences et de l’historique des lignes de commande.

Cette règle n’a pas été appliquée pour la majeure partie du contenu existant dans PowerShell-Docs, mais nous l’appliquons au fil du temps. N’hésitez pas à nous aider. L’extension [reflow][reflow] de Visual Studio Code (VSCode) facilite la remise en forme des paragraphes avec cette limite.

## <a name="lists"></a>Listes

Si votre liste contient plusieurs phrases ou paragraphes, envisagez d’utiliser un en-tête de sous-niveau au lieu d’une liste.

Les listes doivent être précédées et suivies d’une seule ligne vide.

### <a name="unordered-lists"></a>Listes non triées

Ne terminez pas les éléments d’une liste par un point, sauf s’ils contiennent plusieurs phrases. Utilisez le caractère de trait d’union (`-`) pour les puces des éléments d’une liste. Cela évite la confusion avec un balisage en gras ou en italique qui utilise l’astérisque [`*`]. Pour inclure un paragraphe ou d’autres éléments sous un élément à puce, insérez un saut de ligne et alignez l’indentation sur le premier caractère après la puce.

Par exemple :

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

Voici une liste qui contient des sous-éléments sous un élément à puce.

- Premier élément à puce

  Phrase expliquant la première puce.

  - Élément à sous-puce

    Phrase expliquant la sous-puce.

- Deuxième élément à puce
- Troisième élément à puce

### <a name="ordered-lists"></a>Listes triées

Pour inclure un paragraphe ou d’autres éléments sous un élément numéroté, alignez l’indentation sur le premier caractère après le numéro de l’élément.

```markdown
1. For the first element, insert a single space after the 1. Long sentences should be
   wrapped to the next line and must line up with the first character after the numbered
   list marker.

   To include a second element (like this one), insert a line break after the first
   and align indentations. The indentation of the second element must line up with
   the first character after the numbered list marker. For single digit items, like
   this one, you indent to column 4. For double digits items, for example item number
   10, you indent to column 5.

1. The next numbered item starts here.
```

Pour obtenir ce résultat :

> 1. Pour le premier élément, insérez un espace après 1. Les phrases longues doivent être renvoyées à la ligne suivante et être alignées sur le premier caractère après le marqueur de liste numérotée.
>
>    Pour inclure un deuxième élément (comme celui-ci), insérez un saut de ligne après le premier élément et alignez les indentations. L’indentation du deuxième élément doit être alignée sur le premier caractère après le marqueur de liste numérotée. Pour les éléments à un seul chiffre, comme celui-ci, vous indentez à la colonne 4. Pour les éléments à deux chiffres, par exemple le numéro d’élément 10, vous indentez à la colonne 5.
>
> 1. L’élément numéroté suivant commence ici.

Tous les éléments d’une liste numérotée doivent utiliser le nombre `1.` au lieu de l’incrémenter pour chaque élément.
Le rendu de Markdown incrémente automatiquement la valeur. Cela facilite la réorganisation des éléments et standardise l’indentation du contenu subordonné.

## <a name="formatting-command-syntax-elements"></a>Mise en forme des éléments de la syntaxe des commandes

- Les noms des applets de commande PowerShell ont une [casse Pascal][pascal-case]. Les verbes sont séparés des noms par un trait d’union. Utilisez toujours le nom complet en casse Pascal pour les applets de commande et les paramètres. Évitez d’utiliser des alias, sauf si vous parlez spécifiquement d’un alias.

- Dans un paragraphe, les mots clés du langage, les noms des applets de commande et les références de variable doivent être entourés de caractères d’accent grave (`` ` ``). Les noms des propriétés, des paramètres et des classes doivent être en **gras**.

  Par exemple :

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- Quand vous faites référence à un paramètre par son nom, le nom doit être en **gras**. Lors de l’illustration de l’utilisation d’un paramètre avec le préfixe de trait d’union, le paramètre doit être entouré d’accents graves. Par exemple :

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- Quand vous faites référence à des commandes externes (des fichiers exécutables, des scripts, etc.), le nom de la commande doit être en gras, tout en minuscules (ou avec une majuscule s’il est au début d’une phrase) et inclure l’extension de fichier appropriée. Par exemple :

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- Quand vous montrez un exemple d’utilisation d’une commande externe, l’exemple doit être entouré d’accents graves.
  En cas de conflit de noms avec un alias, vous devez inclure l’extension de fichier dans l’exemple de commande. Par exemple :

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- Lors de l’écriture d’un article conceptuel (par opposition au contenu des informations de référence), la première occurrence du nom d’une applet de commande doit avoir un lien hypertexte vers la documentation de l’applet de commande. N’utilisez pas d’accents graves, du gras ou un autre balisage à l’intérieur des crochets d’un lien hypertexte.

  Par exemple :

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  Pour plus d’informations, consultez la section [Liens hypertexte](#hyperlinks) du Guide de style.

## <a name="images"></a>Images

La syntaxe pour inclure une image est :

```Syntax
![[alt text]](<folderPath>)
```

Exemple :

```markdown
![Introduction](./media/overview/Introduction.png)
```

Où `alt text` est une brève description de l’image et `<folder path>` un chemin relatif de l’image. Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants. Ce texte est également utile dans le cas où un bogue du site empêche l’affichage de l’image.

Les images doivent être stockées dans un dossier `media/<article-name>` dans le dossier contenant votre article. Les images ne doivent pas être partagées entre des articles. Créez un dossier qui correspond au nom de fichier de votre article sous le dossier `media`. Copiez les images pour cet article dans ce nouveau dossier. Si une image est utilisée par plusieurs articles, chaque dossier d’images doit avoir une copie de ce fichier d’image. Cette pratique permet d’éviter que la modification d’une image dans un article affecte un autre article.

Dans certains cas, vous voulez partager des images, comme des logos et des icônes, entre plusieurs articles. Ces images sont stockées dans le dossier `/media/shared` à la racine du dépôt.

Les types de fichiers d’image suivants sont pris en charge : *.png", *.gif", *.jpeg", *.jpg", *.svg

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
