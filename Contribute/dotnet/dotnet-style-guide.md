---
title: Modèle et aide-mémoire pour les articles .NET
description: Cet article contient un modèle pratique que vous pouvez utiliser pour créer des articles pour les dépôts de documentation .NET.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: a520112cd77f4c4807e7719c2c4dbd43a762f062
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2020
ms.locfileid: "80759558"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a>Modèle de métadonnées et de Markdown pour la documentation .NET

Ce modèle dotnet/docs contient des exemples de syntaxe Markdown ainsi que des conseils sur la configuration des métadonnées.

Lors de la création d’un fichier Markdown, vous devez copier le modèle inclus dans un nouveau fichier, renseigner les métadonnées come indiqué ci-dessous et définir l’en-tête H1 ci-dessus dans le titre de l’article.

## <a name="metadata"></a>Métadonnées

Le bloc de métadonnées requis se trouve dans l’exemple de bloc de métadonnées suivant :

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- Vous **devez** insérer un espace entre les deux-points (:) et la valeur d’un élément de métadonnées.
- Les deux-points dans une valeur (par exemple un titre) rompent l’analyseur de métadonnées. Dans ce cas, placez le titre entre des guillemets doubles (par exemple `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).
- **title** : apparaît dans les résultats des moteurs de recherche. Le titre ne doit pas être identique au titre de votre en-tête H1, et il doit contenir au plus 60 caractères.
- **description** : fournit un récapitulatif du contenu de l’article. Elle est généralement affichée dans la page des résultats de la recherche, mais elle n’entre pas en compte pour le classement des recherches. Elle doit avoir une longueur comprise entre 115 et 145 caractères, espaces compris.
- **author** : le champ author doit contenir le **nom d’utilisateur GitHub** de l’auteur.
- **ms.date** : date de la dernière mise à jour importante. Mettez-la à jour dans les articles existants si vous avez révisé et mis à jour l’ensemble de l’article. Les petites corrections, telles que les fautes de frappe ou similaires, ne nécessitent pas de mise à jour.

D’autres métadonnées sont attachées à chaque article, mais nous appliquons en général la plupart des valeurs de métadonnées au niveau du dossier, spécifié dans **docfx.json**.

## <a name="basic-markdown-gfm-and-special-characters"></a>Markdown de base, GFM et caractères spéciaux

Pour découvrir les principes de base de Markdown, de GFM (GitHub Flavored Markdown) et des extensions propres à OPS, consultez l’article [Informations de référence sur Markdown](../markdown-reference.md).

Markdown utilise des caractères spéciaux tels que \*, \` et \# pour la mise en forme. Si vous souhaitez inclure l’un de ces caractères dans votre contenu, vous devez effectuer l’une des deux opérations suivantes :

- Placer une barre oblique inverse avant le caractère spécial pour l’« échapper » (par exemple `\*` pour \*)
- Utiliser le [code d’entité HTML](http://www.ascii.cl/htmlcodes.htm) pour le caractère (par exemple `&#42;` pour &#42;)

## <a name="file-names"></a>Noms de fichiers

Les noms de fichiers suivent les règles ci-dessous :

* Ils ne doivent contenir que des lettres, des chiffres et des traits d’union.
* Ils ne doivent pas contenir d’espaces ni de caractères de ponctuation. Utilisez des traits d’union pour séparer les mots et les chiffres compris dans le nom de fichier.
* Utilisez des verbes d’action spécifiques, tels que « développer », « acheter », « créer », « dépanner », etc. Ils ne doivent pas comprendre de mots se terminant par « -ing ».
* Ils ne doivent pas comprendre de mots courts (« un », « et », « le », « en », « ou », etc.).
* Ils doivent être au format Markdown et avoir l’extension de fichier .md.
* Faites en sorte que les noms de fichiers soient le plus court possible. Ils font partie de l’URL de vos articles.

## <a name="headings"></a>En-têtes

Utilisez les majuscules comme pour les phrases. Mettez toujours une majuscule au premier mot d’un titre.

## <a name="text-styling"></a>Style de texte

*Italique* À utiliser pour les fichiers, dossiers, chemins (les éléments longs doivent figurer sur leur propre ligne), nouveaux termes.

**Gras** À utiliser pour les éléments d’interface utilisateur.

`Code` À utiliser pour le code inline, les mots clés de langage, les noms des packages NuGet, les commandes de la ligne de commande, les noms des colonnes et tables de base de données, et les URL qui ne doivent pas être cliquables.

## <a name="links"></a>Liens

Pour plus d’informations sur les ancrages, les liens internes, les liens vers d’autres documents, les ajouts de code et les liens externes, consultez l’article général sur les [Liens](../how-to-write-links.md).

L’équipe de documentation .NET applique les conventions suivantes :

- Dans la plupart des cas, nous utilisons des liens relatifs et déconseillons l’utilisation de `~/` dans les liens, car les liens relatifs sont résolus dans la source sur GitHub. Toutefois, chaque fois que nous établissons une liaison vers un fichier dans un dépôt dépendant, nous utilisons le caractère `~/` pour spécifier le chemin. Étant donné que les fichiers d’un dépôt dépendant sont à un emplacement différent dans GitHub, les liens relatifs ne seront pas résolus correctement, quelle que soit la manière dont ils sont écrits.
- Les spécifications des langages C# et Visual Basic sont comprises dans la documentation .NET en incluant la source à partir des dépôts de langage. Les sources Markdown sont gérées dans les dépôts [csharplang](https://github.com/dotnet/csharplang) et [vblang](https://github.com/dotnet/vblang).

Les liens vers les spécifications doivent pointer vers les répertoires sources dans lesquels ces spécifications sont stockées. Pour C#, il s’agit de **~/_csharplang/spec**, et pour VB, il s’agit de **~/_vblang/spec**, comme dans l’exemple suivant :

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a>Liens vers les API

Le système de build comprend certaines extensions qui nous permettent d’établir des liaisons vers des API .NET sans avoir à recourir à des liens externes. Vous devez utiliser l’une des syntaxes suivantes :

1. Lien automatique : `<xref:UID>` ou `<xref:UID?displayProperty=nameWithType>`

   Le paramètre de requête `displayProperty` produit un texte de lien complet. Par défaut, le texte du lien montre seulement le nom du membre ou du type.

2. Lien Markdown : `[link text](xref:UID)`

   À utiliser quand vous voulez personnaliser le texte du lien affiché.

Exemples :

- `<xref:System.String>` est rendu en tant que [String](https://docs.microsoft.com/dotnet/api/system.string)
- `<xref:System.String?displayProperty=nameWithType>` est rendu en tant que [System.String](https://docs.microsoft.com/dotnet/api/system.string)
- `[String class](xref:System.String)` est rendu en tant que [classe String](https://docs.microsoft.com/dotnet/api/system.string)

Pour plus d’informations sur l’utilisation de cette notation, consultez [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).

Certains UID contiennent les caractères spéciaux \`, \# ou \*. La valeur de l’UID doit être encodée en HTML en tant que `%60`, `%23` et `%2A`, respectivement. Vous pouvez parfois trouver des parenthèses dans l’encodage, mais elles ne sont pas obligatoires.

Exemples :

- System.Threading.Tasks.Task\`1 devient `System.Threading.Tasks.Task%601`
- System.Exception.\#ctor devient `System.Exception.%23ctor`
- System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) devient `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`

Vous pouvez obtenir les UID des types, une liste des surcharges de membres ou un membre surchargé spécifique à partir de`https://xref.docs.microsoft.com/autocomplete`. La chaîne de requête `?text=*\<type-member-name>*` identifie le type ou le membre dont vous souhaitez voir les UID. Par exemple, `https://xref.docs.microsoft.com/autocomplete?text=string.format` récupère les surcharges [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format). L’outil recherche le paramètre de requête `text` fourni dans n’importe quelle partie de l’UID. Par exemple, vous pouvez rechercher le nom du membre (ToString), le nom du membre partiel (ToStri), le type et le le nom du membre (Double.ToString), et ainsi de suite.

Si vous ajoutez un \* (ou un `%2A`) après l’UID, le lien représente alors la page de la surcharge et non une API spécifique. Par exemple, vous pouvez utiliser cela quand vous voulez créer un lien vers la page de la méthode [List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) de façon générique, au lieu d’une surcharge spécifique, comme [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_). Vous pouvez aussi utiliser \* pour établir une liaison vers une page de membre quand le membre n’est pas surchargé. Cela vous évite d’avoir à inclure la liste des paramètres dans l’UID.

Pour établir une liaison à une surcharge de méthode spécifique, vous devez inclure le nom de type qualifié complet de chacun des paramètres de la méthode. Par exemple, \<xref:System.DateTime.ToString> établit une liaison à la méthode sans paramètre [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), tandis que \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> établit une liaison à la méthode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).

Pour établir une liaison à un type générique, tel que [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), vous utilisez le caractère \` (`%60`) suivi du nombre de paramètres de type générique. Par exemple, `<xref:System.Nullable%601>` établit une liaison au type [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), tandis que `<xref:System.Func%602>` établit une liaison au délégué [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).

## <a name="code"></a>Code

Le meilleur moyen d’inclure du code consiste à inclure des extraits à partir d’un exemple opérationnel. Créez votre exemple en suivant les instructions fournies dans l’article [Contribution à .NET](dotnet-contribute.md#contributing-to-samples). Les règles de base pour l’inclusion de code figurent dans les instructions générales concernant le [code](../code-in-docs.md).

Vous pouvez inclure le code à l’aide de la syntaxe suivante :

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* `-<language>` (*facultatif* mais *recommandé*)
  * Langage de l’extrait de code référencé.

* `<name>` (*facultatif*)
  * Nom de l’extrait de code. Il n’a aucun impact sur la sortie HTML, mais vous pouvez l’utiliser pour améliorer la lisibilité de votre source Markdown.

* `<pathToFile>` (*obligatoire*)
  * Chemin relatif dans le système de fichiers qui indique le fichier d’extrait de code à référencer. Il peut être compliqué du fait des différents dépôts qui composent le jeu de documentation .NET. Les exemples .NET se trouvent dans le dépôt dotnet/samples. Tous les chemins des extraits commenceraient par `~/samples`, le reste du chemin étant constitué du chemin vers la source à partir de la racine de ce dépôt.

* `<queryoption>` (*facultatif*)
  * Utilisé pour spécifier la manière dont le code doit être récupéré à partir du fichier :
    * `#` :  `#{tagname}` (nom de balise) *ou* `#L{startlinenumber}-L{endlinenumber}` (plage de lignes).
    Nous déconseillons l’utilisation de numéros de lignes, car ils sont très fragiles. Il est préférable de référencer les exemples de code par nom de balise. Utilisez des noms de balises significatifs. (De nombreux extraits de code ont été migrés à partir d’une plateforme antérieure, et les balise ont des noms tels que `Snippet1`, `Snippet2` et ainsi de suite. Cette pratique est beaucoup plus difficile à maintenir.)
    * `range` : `?range=1,3-5` plage de lignes. Cet exemple inclut les lignes 1, 3, 4 et 5.

Nous recommandons d’utiliser l’option de nom de balise dans la mesure du possible. Le nom de balise est le nom d’une région ou d’un commentaire de code au format `Snippettagname` présent dans le code source. L’exemple suivant montre comment faire référence au nom de balise `BasicThrow` :

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

Le chemin relatif à la source dans le dépôt **dotnet/samples** suit le chemin `~/samples`.

Et vous pouvez voir comment les balises de l’extrait sont structurées dans [ce fichier source](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs). Pour plus d’informations sur la représentation des balises de noms dans les fichiers sources d’extrait de code selon les langages, consultez les [Instructions DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

L’exemple suivant montre du code inclus dans les trois langages .NET :

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]
```

Le fait d’inclure des extraits tirés de programmes complets permet de s’assurer que tout le code transite par notre système d’intégration continue. Toutefois, si vous souhaitez afficher quelque chose qui provoque des erreurs de compilation ou d’exécution, vous pouvez utiliser des blocs de code inline.

## <a name="images"></a>Images

### <a name="static-image-or-animated-gif"></a>Image statique ou GIF animé

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a>Image liée

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a>Vidéos

Actuellement, vous pouvez incorporer des vidéos Channel 9 et YouTube avec la syntaxe suivante :

### <a name="channel-9"></a>Canal 9

```markdown
> [!VIDEO <channel9_video_link>]
```

Pour obtenir l’URL correcte de la vidéo, sélectionnez l’onglet **Incorporer** sous la trame vidéo et copiez l’URL à partir de l’élément `<iframe>`. Par exemple :

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a>YouTube

Pour obtenir l’URL correcte de la vidéo, cliquez avec le bouton droit sur la vidéo, sélectionnez **Copier le code incorporé** et copiez l’URL à partir de l’élément `<iframe>`.

```markdown
> [!VIDEO <youtube_video_link>]
```

Par exemple :

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a>Extensions docs.microsoft

docs.microsoft fournit quelques extensions supplémentaires de GitHub Flavored Markdown.

### <a name="checked-lists"></a>Listes de cases à cocher

Un style personnalisé est disponible pour les listes. Vous pouvez afficher des listes avec des coches vertes.

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

Ce code est restitué comme suit :

> [!div class="checklist"]
> * Guide pratique pour créer une application .NET Core
> * Guide pratique pour ajouter une référence au package Microsoft.XmlSerializer.Generator
> * Guide pratique pour modifier votre fichier MyApp.csproj afin d’ajouter des dépendances
> * Guide pratique pour ajouter une classe et un XmlSerializer
> * Guide pratique pour générer et exécuter l’application

Vous pouvez obtenir un exemple de listes vérifiées en action dans la [documentation .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).

### <a name="buttons"></a>Boutons

Liens de boutons :

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

Ce code est restitué comme suit :

> [!div class="button"]
> [liens de boutons](dotnet-contribute.md)

Vous pouvez obtenir un exemple de boutons en action dans la [documentation Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).

### <a name="step-by-steps"></a>Pas à pas

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

Vous pouvez obtenir un exemple de pas à pas en action dans le [Guide C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).
