---
title: Modèle et aide-mémoire pour les articles .NET
description: Cet article contient un modèle pratique que vous pouvez utiliser pour créer des articles pour les dépôts de documentation .NET.
ms.date: 11/07/2018
ms.openlocfilehash: 9b57abd96093940c96f90a4a01b9f81eae063ffb
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653617"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="da0d4-103">Modèle de métadonnées et de Markdown pour la documentation .NET</span><span class="sxs-lookup"><span data-stu-id="da0d4-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="da0d4-104">Ce modèle dotnet/docs contient des exemples de syntaxe Markdown ainsi que des conseils sur la configuration des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da0d4-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="da0d4-105">Lors de la création d’un fichier Markdown, vous devez copier le modèle inclus dans un nouveau fichier, renseigner les métadonnées come indiqué ci-dessous et définir l’en-tête H1 ci-dessus dans le titre de l’article.</span><span class="sxs-lookup"><span data-stu-id="da0d4-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="da0d4-106">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="da0d4-106">Metadata</span></span>

<span data-ttu-id="da0d4-107">Le bloc de métadonnées requis se trouve dans l’exemple de bloc de métadonnées suivant :</span><span class="sxs-lookup"><span data-stu-id="da0d4-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="da0d4-108">Vous **devez** insérer un espace entre les deux-points (:) et la valeur d’un élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da0d4-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="da0d4-109">Les deux-points dans une valeur (par exemple un titre) rompent l’analyseur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="da0d4-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="da0d4-110">Dans ce cas, placez le titre entre des guillemets doubles (par exemple `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="da0d4-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="da0d4-111">**title** : apparaît dans les résultats des moteurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="da0d4-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="da0d4-112">Le titre ne doit pas être identique au titre de votre en-tête H1, et il doit contenir au plus 60 caractères.</span><span class="sxs-lookup"><span data-stu-id="da0d4-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="da0d4-113">**description** : fournit un récapitulatif du contenu de l’article.</span><span class="sxs-lookup"><span data-stu-id="da0d4-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="da0d4-114">Elle est généralement affichée dans la page des résultats de la recherche, mais elle n’entre pas en compte pour le classement des recherches.</span><span class="sxs-lookup"><span data-stu-id="da0d4-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="da0d4-115">Elle doit avoir une longueur comprise entre 115 et 145 caractères, espaces compris.</span><span class="sxs-lookup"><span data-stu-id="da0d4-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="da0d4-116">**author** : le champ author doit contenir le **nom d’utilisateur GitHub** de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="da0d4-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="da0d4-117">**ms.date** : date de la dernière mise à jour importante.</span><span class="sxs-lookup"><span data-stu-id="da0d4-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="da0d4-118">Mettez-la à jour dans les articles existants si vous avez révisé et mis à jour l’ensemble de l’article.</span><span class="sxs-lookup"><span data-stu-id="da0d4-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="da0d4-119">Les petites corrections, telles que les fautes de frappe ou similaires, ne nécessitent pas de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="da0d4-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="da0d4-120">D’autres métadonnées sont attachées à chaque article, mais nous appliquons en général la plupart des valeurs de métadonnées au niveau du dossier, spécifié dans **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="da0d4-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="da0d4-121">Markdown de base, GFM et caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="da0d4-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="da0d4-122">Pour découvrir les principes de base de Markdown, de GFM (GitHub Flavored Markdown) et des extensions propres à OPS, consultez les articles généraux sur [Markdown](how-to-write-use-markdown.md) et la [référence Markdown](markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="da0d4-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="da0d4-123">Markdown utilise des caractères spéciaux tels que \*, \` et \# pour la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="da0d4-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="da0d4-124">Si vous souhaitez inclure l’un de ces caractères dans votre contenu, vous devez effectuer l’une des deux opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="da0d4-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="da0d4-125">Placer une barre oblique inverse avant le caractère spécial pour l’« échapper » (par exemple `\*` pour \*)</span><span class="sxs-lookup"><span data-stu-id="da0d4-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="da0d4-126">Utiliser le [code d’entité HTML](http://www.ascii.cl/htmlcodes.htm) pour le caractère (par exemple `&#42;` pour &#42;)</span><span class="sxs-lookup"><span data-stu-id="da0d4-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="da0d4-127">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="da0d4-127">File names</span></span>

<span data-ttu-id="da0d4-128">Les noms de fichiers suivent les règles ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="da0d4-128">File names use the following rules:</span></span>

* <span data-ttu-id="da0d4-129">Ils ne doivent contenir que des lettres, des chiffres et des traits d’union.</span><span class="sxs-lookup"><span data-stu-id="da0d4-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="da0d4-130">Ils ne doivent pas contenir d’espaces ni de caractères de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="da0d4-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="da0d4-131">Utilisez des traits d’union pour séparer les mots et les chiffres compris dans le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="da0d4-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="da0d4-132">Utilisez des verbes d’action spécifiques, tels que « développer », « acheter », « créer », « dépanner », etc.</span><span class="sxs-lookup"><span data-stu-id="da0d4-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="da0d4-133">Ils ne doivent pas comprendre de mots se terminant par « -ing ».</span><span class="sxs-lookup"><span data-stu-id="da0d4-133">No -ing words.</span></span>
* <span data-ttu-id="da0d4-134">Ils ne doivent pas comprendre de mots courts (« un », « et », « le », « en », « ou », etc.).</span><span class="sxs-lookup"><span data-stu-id="da0d4-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="da0d4-135">Ils doivent être au format Markdown et avoir l’extension de fichier .md.</span><span class="sxs-lookup"><span data-stu-id="da0d4-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="da0d4-136">Faites en sorte que les noms de fichiers soient le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="da0d4-136">Keep file names reasonably short.</span></span> <span data-ttu-id="da0d4-137">Ils font partie de l’URL de vos articles.</span><span class="sxs-lookup"><span data-stu-id="da0d4-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="da0d4-138">En-têtes</span><span class="sxs-lookup"><span data-stu-id="da0d4-138">Headings</span></span>

<span data-ttu-id="da0d4-139">Utilisez les majuscules comme pour les phrases.</span><span class="sxs-lookup"><span data-stu-id="da0d4-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="da0d4-140">Mettez toujours une majuscule au premier mot d’un titre.</span><span class="sxs-lookup"><span data-stu-id="da0d4-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="da0d4-141">Style de texte</span><span class="sxs-lookup"><span data-stu-id="da0d4-141">Text styling</span></span>

<span data-ttu-id="da0d4-142">*Italique* À utiliser pour les fichiers, dossiers, chemins (les éléments longs doivent figurer sur leur propre ligne), nouveaux termes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="da0d4-143">**Gras** À utiliser pour les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da0d4-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="da0d4-144">`Code` À utiliser pour le code inline, les mots clés de langage, les noms des packages NuGet, les commandes de la ligne de commande, les noms des colonnes et tables de base de données, et les URL qui ne doivent pas être cliquables.</span><span class="sxs-lookup"><span data-stu-id="da0d4-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="da0d4-145">Liens</span><span class="sxs-lookup"><span data-stu-id="da0d4-145">Links</span></span>

<span data-ttu-id="da0d4-146">Pour plus d’informations sur les ancrages, les liens internes, les liens vers d’autres documents, les ajouts de code et les liens externes, consultez l’article général sur les [Liens](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="da0d4-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="da0d4-147">L’équipe de documentation .NET applique les conventions suivantes :</span><span class="sxs-lookup"><span data-stu-id="da0d4-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="da0d4-148">Dans la plupart des cas, nous utilisons des liens relatifs et déconseillons l’utilisation de `~/` dans les liens, car les liens relatifs sont résolus dans la source sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="da0d4-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="da0d4-149">Toutefois, chaque fois que nous établissons une liaison vers un fichier dans un dépôt dépendant, nous utilisons le caractère `~/` pour spécifier le chemin.</span><span class="sxs-lookup"><span data-stu-id="da0d4-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="da0d4-150">Étant donné que les fichiers d’un dépôt dépendant sont à un emplacement différent dans GitHub, les liens relatifs ne seront pas résolus correctement, quelle que soit la manière dont ils sont écrits.</span><span class="sxs-lookup"><span data-stu-id="da0d4-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="da0d4-151">Les spécifications des langages C# et Visual Basic sont comprises dans la documentation .NET en incluant la source à partir des dépôts de langage.</span><span class="sxs-lookup"><span data-stu-id="da0d4-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="da0d4-152">Les sources Markdown sont gérées dans les dépôts [csharplang](https://github.com/dotnet/csharplang) et [vblang](https://github.com/dotnet/vblang).</span><span class="sxs-lookup"><span data-stu-id="da0d4-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="da0d4-153">Les liens vers les spécifications doivent pointer vers les répertoires sources dans lesquels ces spécifications sont stockées.</span><span class="sxs-lookup"><span data-stu-id="da0d4-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="da0d4-154">Pour C#, il s’agit de **~/_csharplang/spec**, et pour VB, il s’agit de **~/_vblang/spec**, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="da0d4-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="da0d4-155">Liens vers les API</span><span class="sxs-lookup"><span data-stu-id="da0d4-155">Links to APIs</span></span>

<span data-ttu-id="da0d4-156">Le système de build comprend certaines extensions qui nous permettent d’établir des liaisons vers des API .NET sans avoir à recourir à des liens externes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="da0d4-157">Vous devez utiliser l’une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="da0d4-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="da0d4-158">Lien automatique : `<xref:UID>` ou `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="da0d4-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="da0d4-159">Le paramètre de requête `displayProperty` produit un texte de lien complet.</span><span class="sxs-lookup"><span data-stu-id="da0d4-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="da0d4-160">Par défaut, le texte du lien montre seulement le nom du membre ou du type.</span><span class="sxs-lookup"><span data-stu-id="da0d4-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="da0d4-161">Lien Markdown : `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="da0d4-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="da0d4-162">À utiliser quand vous voulez personnaliser le texte du lien affiché.</span><span class="sxs-lookup"><span data-stu-id="da0d4-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="da0d4-163">Exemples :</span><span class="sxs-lookup"><span data-stu-id="da0d4-163">Examples:</span></span>

- <span data-ttu-id="da0d4-164">`<xref:System.String>` est rendu en tant que [String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="da0d4-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="da0d4-165">`<xref:System.String?displayProperty=nameWithType>` est rendu en tant que [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="da0d4-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="da0d4-166">`[String class](xref:System.String)` est rendu en tant que [classe String](https://docs.microsoft.com/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="da0d4-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="da0d4-167">Pour plus d’informations sur l’utilisation de cette notation, consultez [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span><span class="sxs-lookup"><span data-stu-id="da0d4-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="da0d4-168">Certains UID contiennent les caractères spéciaux \`, \# ou \*. La valeur de l’UID doit être encodée en HTML en tant que `%60`, `%23` et `%2A`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="da0d4-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="da0d4-169">Vous pouvez parfois trouver des parenthèses dans l’encodage, mais elles ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="da0d4-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="da0d4-170">Exemples :</span><span class="sxs-lookup"><span data-stu-id="da0d4-170">Examples:</span></span>

- <span data-ttu-id="da0d4-171">System.Threading.Tasks.Task\`1 devient `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="da0d4-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="da0d4-172">System.Exception.\#ctor devient `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="da0d4-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="da0d4-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) devient `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="da0d4-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="da0d4-174">Vous pouvez obtenir les UID des types, une liste des surcharges de membres ou un membre surchargé spécifique à partir de`https://xref.docs.microsoft.com/autocomplete`.</span><span class="sxs-lookup"><span data-stu-id="da0d4-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="da0d4-175">La chaîne de requête `?text=*\<type-member-name>*` identifie le type ou le membre dont vous souhaitez voir les UID.</span><span class="sxs-lookup"><span data-stu-id="da0d4-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="da0d4-176">Par exemple, `https://xref.docs.microsoft.com/autocomplete?text=string.format` récupère les surcharges [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format).</span><span class="sxs-lookup"><span data-stu-id="da0d4-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="da0d4-177">L’outil recherche le paramètre de requête `text` fourni dans n’importe quelle partie de l’UID.</span><span class="sxs-lookup"><span data-stu-id="da0d4-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="da0d4-178">Par exemple, vous pouvez rechercher le nom du membre (ToString), le nom du membre partiel (ToStri), le type et le le nom du membre (Double.ToString), et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="da0d4-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="da0d4-179">Si vous ajoutez un \* (ou un `%2A`) après l’UID, le lien représente alors la page de la surcharge et non une API spécifique.</span><span class="sxs-lookup"><span data-stu-id="da0d4-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="da0d4-180">Par exemple, vous pouvez utiliser cela quand vous voulez créer un lien vers la page de la méthode [List\<T>.BinarySearch](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) de façon générique, au lieu d’une surcharge spécifique, comme [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span><span class="sxs-lookup"><span data-stu-id="da0d4-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="da0d4-181">Vous pouvez aussi utiliser \* pour établir une liaison vers une page de membre quand le membre n’est pas surchargé. Cela vous évite d’avoir à inclure la liste des paramètres dans l’UID.</span><span class="sxs-lookup"><span data-stu-id="da0d4-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="da0d4-182">Pour établir une liaison à une surcharge de méthode spécifique, vous devez inclure le nom de type qualifié complet de chacun des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="da0d4-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="da0d4-183">Par exemple, \<xref:System.DateTime.ToString> établit une liaison à la méthode sans paramètre [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString), tandis que \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> établit une liaison à la méthode [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_).</span><span class="sxs-lookup"><span data-stu-id="da0d4-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="da0d4-184">Pour établir une liaison à un type générique, tel que [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), vous utilisez le caractère \` (`%60`) suivi du nombre de paramètres de type générique.</span><span class="sxs-lookup"><span data-stu-id="da0d4-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="da0d4-185">Par exemple, `<xref:System.Nullable%601>` établit une liaison au type [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1), tandis que `<xref:System.Func%602>` établit une liaison au délégué [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2).</span><span class="sxs-lookup"><span data-stu-id="da0d4-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="da0d4-186">Code</span><span class="sxs-lookup"><span data-stu-id="da0d4-186">Code</span></span>

<span data-ttu-id="da0d4-187">Le meilleur moyen d’inclure du code consiste à inclure des extraits à partir d’un exemple opérationnel.</span><span class="sxs-lookup"><span data-stu-id="da0d4-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="da0d4-188">Créez votre exemple en suivant les instructions fournies dans l’article [Contribution à .NET](dotnet-contribute-process.md#contributing-to-samples).</span><span class="sxs-lookup"><span data-stu-id="da0d4-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="da0d4-189">Les règles de base pour l’inclusion de code figurent dans les instructions générales concernant le [code](how-to-write-use-markdown.md#code-snippets).</span><span class="sxs-lookup"><span data-stu-id="da0d4-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="da0d4-190">Vous pouvez inclure le code à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="da0d4-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="da0d4-191">`-<language>` (*facultatif* mais *recommandé*)</span><span class="sxs-lookup"><span data-stu-id="da0d4-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="da0d4-192">Langage de l’extrait de code référencé.</span><span class="sxs-lookup"><span data-stu-id="da0d4-192">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="da0d4-193">`<name>` (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="da0d4-193">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="da0d4-194">Nom de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="da0d4-194">Name for the code snippet.</span></span> <span data-ttu-id="da0d4-195">Il n’a aucun impact sur la sortie HTML, mais vous pouvez l’utiliser pour améliorer la lisibilité de votre source Markdown.</span><span class="sxs-lookup"><span data-stu-id="da0d4-195">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="da0d4-196">`<pathToFile>` (*obligatoire*)</span><span class="sxs-lookup"><span data-stu-id="da0d4-196">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="da0d4-197">Chemin relatif dans le système de fichiers qui indique le fichier d’extrait de code à référencer.</span><span class="sxs-lookup"><span data-stu-id="da0d4-197">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="da0d4-198">Il peut être compliqué du fait des différents dépôts qui composent le jeu de documentation .NET.</span><span class="sxs-lookup"><span data-stu-id="da0d4-198">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="da0d4-199">Les exemples .NET se trouvent dans le dépôt dotnet/samples.</span><span class="sxs-lookup"><span data-stu-id="da0d4-199">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="da0d4-200">Tous les chemins des extraits commenceraient par `~/samples`, le reste du chemin étant constitué du chemin vers la source à partir de la racine de ce dépôt.</span><span class="sxs-lookup"><span data-stu-id="da0d4-200">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="da0d4-201">`<queryoption>` (*facultatif*)</span><span class="sxs-lookup"><span data-stu-id="da0d4-201">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="da0d4-202">Utilisé pour spécifier la manière dont le code doit être récupéré à partir du fichier :</span><span class="sxs-lookup"><span data-stu-id="da0d4-202">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="da0d4-203">`#` :  `#{tagname}` (nom de balise) *ou* `#L{startlinenumber}-L{endlinenumber}` (plage de lignes).</span><span class="sxs-lookup"><span data-stu-id="da0d4-203">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="da0d4-204">Nous déconseillons l’utilisation de numéros de lignes, car ils sont très fragiles.</span><span class="sxs-lookup"><span data-stu-id="da0d4-204">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="da0d4-205">Il est préférable de référencer les exemples de code par nom de balise.</span><span class="sxs-lookup"><span data-stu-id="da0d4-205">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="da0d4-206">Utilisez des noms de balises significatifs.</span><span class="sxs-lookup"><span data-stu-id="da0d4-206">Use meaningful tag names.</span></span> <span data-ttu-id="da0d4-207">(De nombreux extraits de code ont été migrés à partir d’une plateforme antérieure, et les balise ont des noms tels que `Snippet1`, `Snippet2` et ainsi de suite. Cette pratique est beaucoup plus difficile à maintenir.)</span><span class="sxs-lookup"><span data-stu-id="da0d4-207">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="da0d4-208">`range` : `?range=1,3-5` plage de lignes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-208">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="da0d4-209">Cet exemple inclut les lignes 1, 3, 4 et 5.</span><span class="sxs-lookup"><span data-stu-id="da0d4-209">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="da0d4-210">Nous recommandons d’utiliser l’option de nom de balise dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="da0d4-210">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="da0d4-211">Le nom de balise est le nom d’une région ou d’un commentaire de code au format `Snippettagname` présent dans le code source.</span><span class="sxs-lookup"><span data-stu-id="da0d4-211">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="da0d4-212">L’exemple suivant montre comment faire référence au nom de balise `BasicThrow` :</span><span class="sxs-lookup"><span data-stu-id="da0d4-212">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="da0d4-213">Le chemin relatif à la source dans le dépôt **dotnet/samples** suit le chemin `~/samples`.</span><span class="sxs-lookup"><span data-stu-id="da0d4-213">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="da0d4-214">Et vous pouvez voir comment les balises de l’extrait sont structurées dans [ce fichier source](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span><span class="sxs-lookup"><span data-stu-id="da0d4-214">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="da0d4-215">Pour plus d’informations sur la représentation des balises de noms dans les fichiers sources d’extrait de code selon les langages, consultez les [Instructions DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span><span class="sxs-lookup"><span data-stu-id="da0d4-215">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="da0d4-216">L’exemple suivant montre du code inclus dans les trois langages .NET :</span><span class="sxs-lookup"><span data-stu-id="da0d4-216">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="da0d4-217">Le fait d’inclure des extraits tirés de programmes complets permet de s’assurer que tout le code transite par notre système d’intégration continue.</span><span class="sxs-lookup"><span data-stu-id="da0d4-217">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="da0d4-218">Toutefois, si vous souhaitez afficher quelque chose qui provoque des erreurs de compilation ou d’exécution, vous pouvez utiliser des blocs de code inline.</span><span class="sxs-lookup"><span data-stu-id="da0d4-218">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="da0d4-219">Images</span><span class="sxs-lookup"><span data-stu-id="da0d4-219">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="da0d4-220">Image statique ou GIF animé</span><span class="sxs-lookup"><span data-stu-id="da0d4-220">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="da0d4-221">Image liée</span><span class="sxs-lookup"><span data-stu-id="da0d4-221">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="da0d4-222">Vidéos</span><span class="sxs-lookup"><span data-stu-id="da0d4-222">Videos</span></span>

<span data-ttu-id="da0d4-223">Actuellement, vous pouvez incorporer des vidéos Channel 9 et YouTube avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="da0d4-223">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="da0d4-224">Canal 9</span><span class="sxs-lookup"><span data-stu-id="da0d4-224">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="da0d4-225">Pour obtenir l’URL correcte de la vidéo, sélectionnez l’onglet **Incorporer** sous la trame vidéo et copiez l’URL à partir de l’élément `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="da0d4-225">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="da0d4-226">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="da0d4-226">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="da0d4-227">YouTube</span><span class="sxs-lookup"><span data-stu-id="da0d4-227">YouTube</span></span>

<span data-ttu-id="da0d4-228">Pour obtenir l’URL correcte de la vidéo, cliquez avec le bouton droit sur la vidéo, sélectionnez **Copier le code incorporé** et copiez l’URL à partir de l’élément `<iframe>`.</span><span class="sxs-lookup"><span data-stu-id="da0d4-228">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="da0d4-229">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="da0d4-229">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="da0d4-230">Extensions docs.microsoft</span><span class="sxs-lookup"><span data-stu-id="da0d4-230">docs.microsoft extensions</span></span>

<span data-ttu-id="da0d4-231">docs.microsoft fournit quelques extensions supplémentaires de GitHub Flavored Markdown.</span><span class="sxs-lookup"><span data-stu-id="da0d4-231">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="da0d4-232">Listes de cases à cocher</span><span class="sxs-lookup"><span data-stu-id="da0d4-232">Checked lists</span></span>

<span data-ttu-id="da0d4-233">Un style personnalisé est disponible pour les listes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-233">A custom style is available for lists.</span></span> <span data-ttu-id="da0d4-234">Vous pouvez afficher des listes avec des coches vertes.</span><span class="sxs-lookup"><span data-stu-id="da0d4-234">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="da0d4-235">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="da0d4-235">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="da0d4-236">Guide pratique pour créer une application .NET Core</span><span class="sxs-lookup"><span data-stu-id="da0d4-236">How to create a .NET Core app</span></span>
> * <span data-ttu-id="da0d4-237">Guide pratique pour ajouter une référence au package Microsoft.XmlSerializer.Generator</span><span class="sxs-lookup"><span data-stu-id="da0d4-237">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="da0d4-238">Guide pratique pour modifier votre fichier MyApp.csproj afin d’ajouter des dépendances</span><span class="sxs-lookup"><span data-stu-id="da0d4-238">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="da0d4-239">Guide pratique pour ajouter une classe et un XmlSerializer</span><span class="sxs-lookup"><span data-stu-id="da0d4-239">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="da0d4-240">Guide pratique pour générer et exécuter l’application</span><span class="sxs-lookup"><span data-stu-id="da0d4-240">How to build and run the application</span></span>

<span data-ttu-id="da0d4-241">Vous pouvez obtenir un exemple de listes vérifiées en action dans la [documentation .NET Core](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span><span class="sxs-lookup"><span data-stu-id="da0d4-241">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="da0d4-242">Boutons</span><span class="sxs-lookup"><span data-stu-id="da0d4-242">Buttons</span></span>

<span data-ttu-id="da0d4-243">Liens de boutons :</span><span class="sxs-lookup"><span data-stu-id="da0d4-243">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="da0d4-244">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="da0d4-244">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="da0d4-245">liens de boutons</span><span class="sxs-lookup"><span data-stu-id="da0d4-245">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="da0d4-246">Vous pouvez obtenir un exemple de boutons en action dans la [documentation Visual Studio](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="da0d4-246">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="da0d4-247">Pas à pas</span><span class="sxs-lookup"><span data-stu-id="da0d4-247">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="da0d4-248">Vous pouvez obtenir un exemple de pas à pas en action dans le [Guide C#](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span><span class="sxs-lookup"><span data-stu-id="da0d4-248">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
