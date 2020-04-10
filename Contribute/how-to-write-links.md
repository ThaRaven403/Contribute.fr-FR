---
title: Guide pratique pour utiliser des liens dans la documentation
description: Cet article vous aide à créer des liens vers du contenu situé sur docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 03/31/2020
ms.openlocfilehash: ca29d4b9e81f8af3b680367b210bd1734860687d
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/03/2020
ms.locfileid: "80624803"
---
# <a name="use-links-in-documentation"></a>Utiliser des liens dans la documentation

Cet article décrit comment utiliser des liens hypertexte à partir de pages hébergées sur docs.microsoft.com. Vous pouvez facilement ajouter des liens dans la syntaxe Markdown en tenant compte de quelques conventions. Les liens pointent vers du contenu situé dans la même page, dans d’autres pages voisines ou vers des sites et des URL externes.

Le back-end du site docs.microsoft.com utilise OPS (Open Publishing Services) qui prend en charge Markdown conforme avec [CommonMark][] analysé via le moteur [Markdig][]. Ce type Markdown est essentiellement compatible avec [GitHub Flavored Markdown (GFM)][GFM], car la plupart des documents sont stockés dans GitHub et peuvent être modifiés à cet endroit. Des fonctionnalités sont ajoutées via des extensions Markdown.

> [!IMPORTANT]
> Tous les liens doivent être sécurisés (`https` et `http`) lorsque la cible le permet (dans la grande majorité des cas).

## <a name="link-text"></a>Texte du lien

Les mots que vous incluez dans le texte doivent être conviviaux. En d’autres termes, il doit s’agir de mots simples ou du titre de la page vers laquelle vous établissez le lien.

> [!IMPORTANT]
> N’utilisez pas de texte de type « cliquez ici ». Ce n’est pas bon pour l’optimisation du référencement d’un site auprès d’un moteur de recherche et cela ne décrit pas correctement la cible.

**Correct :**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

**Incorrect :**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Liens d'un article à un autre

Deux types de liens hypertexte sont pris en charge par le système de publication : les **URL** et les **liens vers des fichiers**.

Un lien URL peut être un chemin d’URL relatif à la racine de docs.microsoft.com ou une URL absolue qui inclut la syntaxe complète de l’URL (par exemple, `https://github.com/MicrosoftDocs/PowerShell-Docs`).

- Utilisez un lien URL pour établir un lien vers du contenu situé en dehors du _docset_ actif ou entre des articles de référence et conceptuels générés automatiquement dans le docset.
- Le moyen le plus simple de créer un lien relatif consiste à copier l’URL à partir de votre navigateur, puis à supprimer `https://docs.microsoft.com/en-us` de la valeur que vous collez dans le code Markdown.
   - N’incluez pas de paramètres régionaux dans les URL pour les propriétés Microsoft (par exemple, supprimez « /en-US » de l’URL).

Un lien vers un fichier permet de lier un article à un autre dans le docset.

- Tous les chemins à des fichiers utilisent des barres obliques (`/`), et non des barres obliques inverses.
- Un article a un lien vers un autre article du même répertoire :

  `[link text](article-name.md)`

- Un article a un lien vers un article du répertoire parent du répertoire actif :

  `[link text](../article-name.md)`

- Un article a un lien vers un article d’un sous-répertoire du répertoire actif :

  `[link text](directory/article-name.md)`

- Un article a un lien vers un article d’un sous-répertoire du répertoire parent du répertoire actif :

  `[link text](../directory/article-name.md)`

> [!NOTE]
> Aucun des exemples précédents n’utilise de `~/` dans le lien. Pour créer un lien vers un chemin absolu qui commence à la racine du dépôt, commencez le lien avec `/`. L’ajout d’un `~/` produit des liens non valides quand vous accédez aux dépôts sources sur GitHub. En commençant par une `/`, le problème est résolu.

### <a name="structure-of-links-on-docsmicrosoftcom"></a>Structure des liens sur docs.microsoft.com

Le contenu publié sur docs.microsoft.com repose sur la structure d’URL suivante :

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

Exemples :

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- `<locale>` - Identifie la langue de l’article (par exemple : en-us ou fr-fr)
- `<product-service>` - Nom du produit ou du service (par exemple : powershell, dotnet ou azure)
- `[<feature-service>]` (facultatif) - Nom de la fonctionnalité ou du sous-service du produit (par exemple : csharp ou load-balancer)
- `[<subfolder>]` (facultatif) - Nom d’un sous-dossier dans une fonctionnalité
- `<topic>` - Nom du fichier de l’article pour la rubrique (par exemple : load-balancer-overview ou overview)
- `[?view=\<view-name>]` (facultatif) - Nom de la vue utilisée par le sélecteur de version pour du contenu disponible dans plusieurs versions (par exemple : azps-3.5.0)

> [!TIP]
> Dans la plupart des cas, les articles d’un même _docset_ ont le même fragment d’URL `<product-service>`. Par exemple :
> - Même docset
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - Docset différent
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a>Liens de signet

Pour établir un lien vers un titre marqué d’un signet dans le fichier *actif*, utilisez un symbole de hachage suivi des mots du titre en minuscules. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets :

```markdown
[Managed Disks](#managed-disks)
```

Pour établir un lien vers un titre marqué d’un signet dans un autre article, utilisez le lien relatif à un fichier ou relatif à un site plus un symbole dièse, suivi des mots du titre. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets :

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

Vous pouvez également copier le lien vers le signet à partir de l’URL. Pour trouver l’URL, pointez votre souris sur la ligne du titre sur docs.microsoft.com. Vous devriez voir une icône de lien :

![Icône de lien dans le titre de l’article](media/how-to-write-links/bookmark-link.png)

Cliquez sur l’icône de lien, puis copiez le texte de l’ancre du signet à partir de l’URL (c’est-à-dire la partie située après le hachage).

> [!NOTE]
> L’extension Docs contient également des outils pour vous aider à créer des liens.

### <a name="explicit-anchor-links"></a>Liens d’ancrage explicites

L’ajout de liens vers des ancres explicites utilisant la balise HTML `<a>` n’est ni obligatoire ni recommandé, sauf dans les pages hub et d’arrivée. Utilisez plutôt les signets générés automatiquement, comme décrit dans [Liens de signet](#bookmark-links). Pour les pages hub et d’arrivée, déclarez les ancres comme ceci :

```markdown
## <a id="anchortext" />Header text
```

ou

```markdown
## <a name="anchortext" />Header text
```

Ajoutez ce qui suit pour établir un lien vers l’ancre :

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> Le texte de l’ancre doit toujours être en minuscules et ne doit pas contenir d’espaces.

## <a name="xref-cross-reference-links"></a>Liens XRef (référence croisée)

Les liens XRef sont la méthode recommandée pour établir des liens vers des API, car ils sont validés au moment de la génération. Pour créer un lien vers des pages de références d’API générées automatiquement dans le docset actif ou dans d’autres docsets, utilisez des liens XRef avec l’ID unique ([UID](#determine-the-uid)) du type ou membre.

> [!TIP]
> Vous pouvez utiliser l’[extension Docs Markdown pour VS Code][docsextension] (fournie avec le Docs Authoring Pack) pour insérer des liens XRref .NET qui sont exposés dans le [navigateur d’API .NET][].

Vérifiez que l’API vers laquelle doit pointer votre lien se trouve sur [docs.microsoft.com][docs]. Pour cela, tapez tout ou partie de son nom complet dans la zone de recherche du [navigateur d’API .NET][] ou de [Windows UWP][]. Si aucun résultat n’est retourné, le type n’est pas encore sur docs.microsoft.com.

Vous pouvez utiliser une des syntaxes suivantes :

- Liens automatiques :

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   Par défaut, le texte du lien montre seulement le nom du membre ou du type. Le paramètre de requête `displayProperty=nameWithType` facultatif produit un texte de lien complet, à savoir **namespace.type** pour les types et **type.member** pour les membres de type, notamment les membres de type énumération.

- Liens de style Markdown :

   ```markdown
   [link text](xref:UID)
   ```

   Utilisez des liens de style Markdown pour XRef quand vous souhaitez personnaliser le texte du lien affiché.

Exemples :

- **\<xref:System.String>** apparaît sous la forme <xref:System.String>.

- **\<xref:System.String?displayProperty=nameWithType>** apparaît sous la forme <xref:System.String?displayProperty=nameWithType>.

- **\[String class](xref:System.String)** apparaît sous la forme [String class](xref:System.String).

Le paramètre de requête `displayProperty=fullName` fonctionne de la même façon que `displayProperty=nameWithType` pour les classes. Autrement dit, le texte du lien devient **namespace.classname**. Toutefois, pour les membres, le texte du lien apparaît sous la forme **namespace.classname.membername**, ce qui peut être indésirable.

> [!NOTE]
> Les UID respectent la casse. Par exemple, `<xref:System.Object>` est résolu correctement, mais pas `<xref:system.object>`.

### <a name="xref-build-warnings-and-incremental-builds"></a>Avertissements de build XRef et builds incrémentielles

Une build incrémentielle génère uniquement les fichiers qui ont changé ou ceux qui ont été affectés par un changement. Si vous recevez un avertissement de build à propos d’un lien XREF non valide alors que le lien est valide, cela peut être dû au fait que la build est incrémentielle. Le fichier à l’origine de l’avertissement n’a pas changé. Il n’a donc pas été généré et des avertissements antérieurs ont été relus. L’avertissement disparaît quand le fichier change ou si vous déclenchez une build complète (vous pouvez démarrer une build complète sur ops.microsoft.com). C’est un inconvénient pour les builds incrémentielles, car DocFX ne peut pas détecter de mise à jour de données à l’intérieur du service XREF.

### <a name="determine-the-uid"></a>Déterminer l’UID

L’UID est généralement le nom complet de la classe ou du membre. Il existe au moins deux façons de déterminer l’UID :

- Cliquez avec le bouton droit sur la page [Docs][docs] pour un type ou un membre, sélectionnez **Afficher la source**, puis copiez la valeur **content** pour **ms.assetid** :

  ![ms.assetid dans la source de la page web](media/how-to-write-links/ms-assetid.png)

- Utilisez le [site autocomplete][] en ajoutant une partie ou la totalité du nom du type à l’URL. Par exemple, si vous entrez `https://xref.docs.microsoft.com/autocomplete?text=Writeline` dans la barre d’adresses de votre navigateur, vous pouvez voir l’ensemble des types et des méthodes contenant **WriteLine** dans leur nom ainsi que leur UID.

#### <a name="verify-the-uid"></a>Vérifier l’UID

Pour vérifier si votre UID est correct, remplacez **System.String** dans l’URL suivante par votre UID, puis collez-la dans la barre d’adresses d’un navigateur :

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> L’UID dans l’URL respecte la casse. Si vous vérifiez une UID de surcharge de méthode, n’incluez pas d’espace entre les types de paramètres.

Si vous obtenez un message semblable au suivant, votre UID est correct :

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

Si la page affiche uniquement `[]`, votre UID est incorrect.

### <a name="percent-encoding-of-urls"></a>Encodage en pourcent des URL

Les caractères spéciaux de l’UID doivent être encodés au format HTML comme ceci :

| Caractère | Encodage HTML |
| --------- | ------------- |
| `` ` ``   | %60           |
| `#`       | %23           |
| `*`       | %2A           |

Consultez la liste complète des [encodages en pourcent](https://en.wikipedia.org/wiki/Percent-encoding).

Exemples d’encodage :

- `System.Threading.Tasks.Task``1` est encodé sous la forme `System.Threading.Tasks.Task%601` (consultez la [section sur les types génériques](#generic-types)).

- `System.Exception.#ctor` est encodé sous la forme `System.Exception.%23ctor`.

- `System.Object.Equals*` est encodé sous la forme `System.Object.Equals%2A`.

### <a name="generic-types"></a>Types génériques

Les types génériques sont des types tels que `System.Collections.Generic.List<T>`. Si vous accédez à ce type dans le [navigateur d’API .NET](https://docs.microsoft.com/dotnet/api/) et que vous examinez son URL, vous pouvez voir que `<T>` est écrit `-1` dans l’URL, ce qui représente en fait **`1** :

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

Pour établir un lien vers un type générique tel que **List\<T>** , encodez le caractère d’accent grave ( **\`** ) sous la forme **%60**, comme illustré dans l’exemple suivant :

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a>Méthodes

Pour établir un lien vers une méthode, vous pouvez soit créer un lien vers la page de la méthode générale en ajoutant un astérisque (`*`) après le nom de la méthode, soit créer un lien vers une surcharge spécifique. Par exemple, utilisez la page générale quand vous souhaitez établir un lien vers la méthode `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` sans types de paramètres spécifiques. Le caractère astérisque est encodé sous la forme `%2A`. Par exemple :

`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` crée un lien vers <xref:System.Object.Equals%2A?displayProperty=nameWithType>

Pour établir un lien vers une surcharge spécifique, ajoutez des parenthèses après le nom de la méthode et placez dans celles-ci le nom de type complet de chaque paramètre. N’insérez aucun espace entre les noms de types ; sinon, le lien ne fonctionnera pas. Par exemple :

`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` crée un lien vers <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>

## <a name="links-from-includes"></a>Liens des includes

Les fichiers include étant situés dans un autre répertoire, vous devez utiliser des chemins d'accès relatifs plus longs. Pour faire un lien vers un article à partir d'un fichier include, utilisez ce format :

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> L’extension [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) pour Visual Studio Code peut vous aider à insérer correctement des signets et des liens relatifs sans avoir à deviner les chemins.

## <a name="links-in-selectors"></a>Liens dans les sélecteurs

Un sélecteur est un composant de navigation qui apparaît dans un article de documentation sous forme de liste déroulante. Quand un lecteur sélectionne une valeur dans la liste déroulante, le navigateur ouvre l’article sélectionné. En général, la liste du sélecteur contient des liens vers des articles qui ont un rapport étroit avec celui-ci, par exemple traitant du même sujet dans différents langages de programmation, ou vers une série d’articles connexe.

Si vous avez des sélecteurs intégrés dans un include, utilisez la structure de liens suivante :

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a>Liens de type référence

Vous pouvez utiliser des liens de type référence pour rendre votre contenu source plus facile à lire. Les liens de type référence remplacent la syntaxe de lien inline par une syntaxe simplifiée vous permettant de déplacer les URL longues à la fin de l’article. Voici l'exemple de [Daring Fireball](https://daringfireball.net/projects/markdown/) :

Texte intégré :

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Liens de référence à la fin de l'article :

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

Veillez à inclure l’espace après le signe deux-points, avant le lien. Lorsque vous liez d'autres articles techniques, si vous oubliez d'inclure l'espace, le lien sera rompu dans l’article publié.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Liens vers des pages qui ne font pas partie de l’ensemble de documentation technique

Pour établir un lien vers une page sur une autre propriété de Microsoft (par exemple la page de tarifs, la page du contrat SLA ou toute autre page qui n’est pas un article de documentation), utilisez une URL absolue, mais omettez les paramètres régionaux. Le but ici est que les liens fonctionnent dans GitHub et sur le site rendu :

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a>Liens vers des sites tiers

Une expérience utilisateur idéale minimise l'envoi d'utilisateurs vers d'autres sites. Basez donc les liens vers des sites tiers, dont nous avons parfois besoin, sur ces informations :

- **Responsabilité** : Établissez un lien vers du contenu tiers quand il s’agit des informations que le tiers est tenu de partager. Par exemple, il ne revient pas à Microsoft d’expliquer aux utilisateurs comment utiliser les outils pour développeurs d’Android. Cette tâche incombe à Google. Si besoin, nous pouvons expliquer comment utiliser les outils Android *avec* Azure, mais l'explication de l'utilisation des outils eux-mêmes est le travail de Google.
- **Validation des PM** : Demandez à Microsoft de valider le contenu tiers. En établissant un lien, nous donnons des indications de notre confiance et de nos obligations si les utilisateurs suivent les instructions.
- **Révisions d’actualisation** : Vérifiez que les informations tierces sont toujours actuelles, correctes et pertinentes, et que le lien n’a pas changé.
- **Hors site** : Informez les utilisateurs qu’ils vont vers un autre site. Si le contexte ne l’indique pas explicitement, ajoutez une phrase pour cela, Par exemple : « Les prérequis comprennent les outils pour développeurs d’Android, que vous pouvez télécharger sur le site d’Android Studio ».
- **Étapes suivantes** : Vous pouvez ajouter un lien vers, par exemple, un blog MVP dans une section « Étapes suivantes ». Encore une fois, vérifiez que les utilisateurs comprennent qu’ils vont quitter le site.
- **Juridique** : Nous sommes légalement couverts sous **Liens vers des sites tiers** dans les **Conditions d’utilisation** en pied de page de chaque page microsoft.com.

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Navigateur d’API .NET]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Site autocomplete]: https://xref.docs.microsoft.com/autocomplete?text=
