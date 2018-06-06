---
title: Guide pratique pour utiliser Markdown pour écrire du contenu Docs
description: Cet article fournit des informations de base et de référence sur le langage Markdown utilisé pour écrire des articles docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 07/13/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 041398361aef90c44bdf3a0dad4aaa2d40a38289
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469943"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>Guide pratique pour utiliser Markdown pour écrire du contenu Docs

Les articles docs.microsoft.com sont écrits dans un langage de balisage léger appelé [Markdown](https://daringfireball.net/projects/markdown/), à la fois facile à lire et facile à apprendre. Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur.

Le contenu Docs étant stocké dans GitHub, il peut utiliser un sur-ensemble de Markdown appelé [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), qui offre des fonctionnalités supplémentaires pour les besoins en formatage courants. De plus, OPS (Open Publishing Services) implémente l’analyseur Markdown Markdig. Markdig est hautement compatible avec GFM (GitHub Flavored Markdown) et offre de nouvelles fonctions permettant d’utiliser des fonctionnalités propres à Docs.

* Markdig est un processeur Markdown rapide, performant, compatible CommonMark et extensible pour .NET.
* https://github.com/lunet-io/markdig
* Meilleure prise en charge de la communauté
* Meilleure prise en charge des standards

## <a name="markdown-basics"></a>Les bases de Markdown

### <a name="headings"></a>En-têtes

Pour créer un en-tête, vous utilisez un dièse (#), comme suit :

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>Texte en gras et italique

Pour formater le texte en **gras**, vous l’entourez de deux astérisques :

```markdown
    This text is **bold**.
```

Pour formater le texte en *italique*, vous l’entourez d’un seul astérisque :

```markdown
    This text is *italic*.
```

Pour formater le texte en ***gras et en italique***, vous l’entourez de trois astérisques :

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>Listes

#### <a name="unordered-list"></a>Liste non ordonnée

Pour formater une liste à puces/non ordonnée, vous pouvez utiliser des astérisques ou des tirets. Par exemple, le code Markdown suivant :

```markdown
- List item 1
- List item 2
- List item 3
```

s’affichera sous la forme :

- Élément de liste 1
- Élément de liste 2
- Élément de liste 3

Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants. Par exemple, le code Markdown suivant :

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

s’affichera sous la forme :

- Élément de liste 1
  - Élément de liste A
  - Élément de liste B
- Élément de liste 2

#### <a name="ordered-list"></a>Liste ordonnée

Pour formater une liste ordonnée/d'étapes, vous utilisez les numéros correspondants. Par exemple, le code Markdown suivant :

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

s’affichera sous la forme :

1. Première instruction
2. Deuxième instruction
3. Troisième instruction

Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants. Par exemple, le code Markdown suivant :

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

s’affichera sous la forme :

1. Première instruction
    1. Sous-instruction
    2. Sous-instruction
2. Deuxième instruction

### <a name="tables"></a>les tableaux

Les tableaux ne sont pas pris en charge par la spécification Markdown principale, mais ils sont pris en charge par GFM. Vous pouvez créer des tableaux avec la barre verticale (|) et le trait d’union (-). Les traits d’union servent à créer l’en-tête de chaque colonne, tandis que les barres verticales séparent chaque colonne. Ajoutez une ligne vide avant votre tableau pour qu’il s’affiche correctement.

Par exemple, le code Markdown suivant :

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

s’affichera sous la forme :

| Amusez-vous                  | avec                 | les tableaux          |
| :------------------- | -------------------: |:---------------:|
| colonne alignée à gauche  | colonne alignée à droite | colonne centrée |
| 100 $                 | 100 $                 | 100 $            |
| 10 $                  | 10 $                  | 10 $             |
| 1 $                   | 1 $                   | 1 $              |

Pour plus d'informations sur la création de tableaux, consultez :

- La [fonctionnalité de wrapping de tableaux](#table-wrapping) Markdig, qui peut vous aider à mettre en forme les tableaux larges
- [Organisation des informations avec des tableaux](https://help.github.com/articles/organizing-information-with-tables/), de GitHub
- L'application Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)
- [« Markdown Cheatsheet » d'Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [« Markdown Extra » de Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table)
- [Convertir les tableaux HTML en Markdown](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>Liens

La syntaxe Markdown pour un lien inline est composée d’une partie `[link text]`, qui est le texte du lien, suivie de la partie `(file-name.md)`, qui est l’URL ou le nom du fichier cible du lien :

 `[link text](file-name.md)`

Pour plus d’informations sur la liaison, consultez :

- Le [Guide de syntaxe Markdown](https://daringfireball.net/projects/markdown/syntax#link) pour plus de détails sur la prise en charge des liens de base avec Markdown.
- La section [Liens](how-to-write-links.md) de ce guide pour plus de détails sur la syntaxe de liaison supplémentaire fournie par Markdig.

### <a name="code-snippets"></a>Extraits de code

Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases. Pour plus d’informations, consultez :

- [Prise en charge native des blocs de code par Markdown](https://daringfireball.net/projects/markdown/syntax#precode)
- [Prise en charge du cloisonnement de code et du surlignage de la syntaxe par GFM](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

Les blocs de code cloisonnés sont un moyen facile de permettre le surlignage de la syntaxe de vos extraits de code. Le format général des blocs de code cloisonnés est la suivante :

    ```alias
    ...
    your code goes in here
    ...
    ```

L’alias après les trois caractères accent grave (`) initiaux définit le surlignage de syntaxe à utiliser. Vous trouverez ci-après une liste de langages de programmation couramment utilisés dans le contenu Docs et l’étiquette correspondante :

Ces langages prennent en charge les noms conviviaux, et pour la plupart d’entre eux, la mise en surbrillance de la syntaxe.

|Nom|Étiquette Markdown|
|-----|-------|
|.NET Console|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>Exemple : C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__Render__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>Exemple : SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__Render__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>Extensions Markdown personnalisées OPS

> [!NOTE]
> OPS (Open Publishing Services) implémente un analyseur Markdig pour Markdown, qui est hautement compatible avec GFM (GitHub Flavored Markdown). Markdig ajoute des fonctionnalités via des extensions Markdown. À ce titre, des articles sélectionnés du Guide de création OPS complet sont inclus dans ce guide pour référence. (Par exemple, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.)

Les articles Docs utilisent GFM pour la majeure partie de la mise en forme des articles, comme les paragraphes, les liens, les listes et les en-têtes. Pour une mise en forme plus riche, les articles peuvent utiliser des fonctionnalités Markdig comme :

- Blocs de notes
- Des includes
- Des sélecteurs
- Des vidéos intégrées
- Des exemples/extraits de code

Pour obtenir la liste complète, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.

### <a name="note-blocks"></a>Blocs de notes

Vous pouvez choisir parmi quatre types de blocs de notes pour attirer l’attention sur du contenu spécifique :

- REMARQUE
- AVERTISSEMENT
- CONSEIL
- IMPORTANT

En général, les blocs de notes doivent être utilisés avec parcimonie, car ils peuvent perturber la lecture. Même s’ils prennent également en charge les blocs de code, les images, les listes et les liens, essayez de vous limiter à des blocs de notes simples et directs.

### <a name="includes"></a>Includes

Quand vous avez du texte ou des fichiers image réutilisables qui doivent être inclus dans des fichiers d’article, vous pouvez utiliser une référence vers le fichier « include » via la fonctionnalité d’inclusion de fichier de Markdig. Cette fonctionnalité demande à OPS d’inclure le fichier dans votre fichier d’article lors de sa génération, ce qui en fait une partie de votre article publié. Trois types d’includes sont disponibles pour vous aider à réutiliser du contenu :

- Inline : pour réutiliser un extrait de texte commun au sein d’une autre phrase.
- Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.
- Image : il s’agit de la façon dont l’inclusion d’images standard est implémentée dans Docs.

Un include de type inline ou bloc est un simple fichier Markdown (.md). Il peut contenir tout code Markdown valide. Tous les fichiers Markdown include doivent être placés dans un [sous-répertoire `/includes` commun ](git-github-fundamentals.md#includes-subdirectory), à la racine du dépôt. Quand l’article est publié, le fichier inclus y est intégré de façon transparente.

Voici les conditions requises et éléments à prendre en compte pour les includes :

- Utilisez les includes lorsque vous souhaitez que le même texte s'affiche dans plusieurs articles.
- Utilisez des includes de blocs pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée. Ne l'utilisez pas pour des éléments plus petits qu'une phrase.
- Les includes ne s’afficheront pas dans la vue de votre article rendu par GitHub, car ils reposent sur des extensions Markdig. Ils ne sont rendus qu’après publication.
- Vérifiez que tout le texte dans un include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence l’include. Ignorer cette instruction crée une chaîne intraduisible dans l'article, ce qui nuit à l'expérience localisée.
- N'imbriquez pas d'includes dans d'autres includes. Les groupes ne sont pas pris en charge.
- Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>`/includes/media. Le répertoire multimédia ne doit pas contenir d'images à sa racine. Si l’include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire multimédia correspondant.
- Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include. Utilisez un fichier distinct avec un nom unique pour chaque include et article. Stockez le fichier multimédia dans le dossier multimédia associé à l’include.
- N'utilisez pas un include comme seul contenu d'un article.  Les includes sont censés compléter le contenu du reste de l'article.

### <a name="selectors"></a>Des sélecteurs

Utilisez des sélecteurs dans les articles techniques lorsque vous créez plusieurs versions d'un même article, pour répondre aux différences d'implémentation à travers les technologies et plateformes. Cela s'applique particulièrement au contenu pour plateformes mobiles pour développeurs. Il existe actuellement deux types différents de sélecteurs dans Markdig, un sélecteur unique et un multi-sélecteur.

Le même Markdown de sélecteur allant dans chaque article de la sélection, nous vous recommandons de placer le sélecteur pour votre article dans un include. Vous pouvez ensuite référencer ce dernier dans tous vos articles qui utilisent le même sélecteur.

### <a name="code-snippets"></a>Extraits de code

Markdig prend en charge l’inclusion avancée de code dans un article, via son extension d’extraits de code. Elle fournit un rendu avancé qui se base sur les fonctionnalités de GFM comme la sélection du langage de programmation et la coloration de la syntaxe, plus des fonctionnalités intéressantes comme :

- l’inclusion d’exemples/extraits de code centralisés depuis un dépôt externe ;
- une interface à onglets pour présenter différentes versions des exemples de code dans différents langages.

## <a name="gotchas-and-troubleshooting"></a>Pièges et résolution des problèmes

### <a name="alt-text"></a>Texte de remplacement

Le texte de remplacement qui contient des traits de soulignement ne s’affiche pas correctement. Par exemple, au lieu d’utiliser ceci :

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

Placez les traits de soulignement dans une séquence d’échappement comme ceci :

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>Apostrophes et guillemets

Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes. Vous devez les encoder ou les changer en apostrophes/guillemets de base. Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ€™s

Voici les encodages pour les versions courbes de ces signes de ponctuation :

- Guillemet gauche (ouvrant) : `&#8220;`
- Guillemet droit (fermant) : `&#8221;`
- Guillemet simple droit (fermant) ou apostrophe : `&#8217;`
- Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`

### <a name="angle-brackets"></a>Crochets pointus

Si vous utilisez des crochets pointus dans le texte (et non le code) de votre fichier, par exemple pour signaler un espace réservé, vous devez manuellement encoder les crochets pointus. Sinon, Markdown considère qu’il s’agit d’une balise HTML.

Par exemple, encodez `<script name>` en `&lt;script name&gt;`

## <a name="see-also"></a>Voir aussi

### <a name="markdown-resources"></a>Ressources Markdown

- [Introduction à Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Fiche récapitulative de Markdown pour Docs](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [Les bases du Markdown GitHub](https://help.github.com/articles/markdown-basics/)
