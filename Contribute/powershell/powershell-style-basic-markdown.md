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
# <a name="markdown-style-guide-for-powershell-docs"></a><span data-ttu-id="e7c94-103">Guide de style Markdown pour PowerShell-Docs</span><span class="sxs-lookup"><span data-stu-id="e7c94-103">Markdown style guide for PowerShell-Docs</span></span>

<span data-ttu-id="e7c94-104">Cet article fournit des conseils de style spécifiques au contenu PowerShell-Docs.</span><span class="sxs-lookup"><span data-stu-id="e7c94-104">This article provides some style guidance specific to the PowerShell-Docs content.</span></span>

<span data-ttu-id="e7c94-105">Pour d’autres conseils sur le style d’écriture, consultez le [Guide de style Microsoft](https://docs.microsoft.com/style-guide/welcome/).</span><span class="sxs-lookup"><span data-stu-id="e7c94-105">For other writing style guidance, see the [Microsoft Style Guide](https://docs.microsoft.com/style-guide/welcome/).</span></span>

## <a name="metadata"></a><span data-ttu-id="e7c94-106">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="e7c94-106">Metadata</span></span>

<span data-ttu-id="e7c94-107">Ce modèle contient des exemples de syntaxe Markdown ainsi que des conseils sur la définition des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e7c94-107">This template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>
<span data-ttu-id="e7c94-108">Lors de la création d’un fichier Markdown, vous devez copier le modèle inclus dans un nouveau fichier, renseigner les métadonnées come indiqué ci-dessous et définir l’en-tête H1 ci-dessus dans le titre de l’article.</span><span class="sxs-lookup"><span data-stu-id="e7c94-108">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

<span data-ttu-id="e7c94-109">Le bloc de métadonnées requis se trouve dans l’exemple de bloc de métadonnées suivant :</span><span class="sxs-lookup"><span data-stu-id="e7c94-109">The required metadata block is in the following sample metadata block:</span></span>

```md
---
author: [GITHUB USERNAME]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
title: [ARTICLE TITLE]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="e7c94-110">Vous **devez** insérer un espace entre les deux-points (:) et la valeur d’un élément de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e7c94-110">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="e7c94-111">Les deux-points dans une valeur (par exemple un titre) rompent l’analyseur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e7c94-111">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="e7c94-112">Dans ce cas, placez le titre entre des guillemets doubles (par exemple `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span><span class="sxs-lookup"><span data-stu-id="e7c94-112">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="e7c94-113">**author** : le champ author doit contenir le **nom d’utilisateur GitHub** de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="e7c94-113">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="e7c94-114">**description** : fournit un récapitulatif du contenu de l’article.</span><span class="sxs-lookup"><span data-stu-id="e7c94-114">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="e7c94-115">Elle est généralement affichée dans la page des résultats de la recherche, mais elle n’entre pas en compte pour le classement des recherches.</span><span class="sxs-lookup"><span data-stu-id="e7c94-115">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="e7c94-116">Elle doit avoir une longueur comprise entre 115 et 145 caractères, espaces compris.</span><span class="sxs-lookup"><span data-stu-id="e7c94-116">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="e7c94-117">**ms.date** : date de la dernière mise à jour importante.</span><span class="sxs-lookup"><span data-stu-id="e7c94-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="e7c94-118">Mettez-la à jour dans les articles existants si vous avez révisé et mis à jour l’ensemble de l’article.</span><span class="sxs-lookup"><span data-stu-id="e7c94-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="e7c94-119">Les petites corrections, comme les fautes de frappe ou similaires, ne nécessitent pas de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e7c94-119">Small fixes, such as typos or similar don't warrant an update.</span></span>
- <span data-ttu-id="e7c94-120">**title** : apparaît dans les résultats des moteurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="e7c94-120">**title**: Appears in search engine results.</span></span> <span data-ttu-id="e7c94-121">Le titre ne doit pas être identique au titre de votre en-tête H1, et il doit contenir au plus 60 caractères.</span><span class="sxs-lookup"><span data-stu-id="e7c94-121">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or fewer.</span></span>

<span data-ttu-id="e7c94-122">D’autres métadonnées sont attachées à chaque article, mais nous appliquons en général la plupart des valeurs de métadonnées au niveau du dossier, spécifié dans **docfx.json**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-122">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="product-terminology"></a><span data-ttu-id="e7c94-123">Terminologie du produit</span><span class="sxs-lookup"><span data-stu-id="e7c94-123">Product Terminology</span></span>

<span data-ttu-id="e7c94-124">Il existe plusieurs variantes de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7c94-124">There are several variants of PowerShell.</span></span> <span data-ttu-id="e7c94-125">Ce tableau définit certains des différents termes utilisés pour parler de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7c94-125">This table defines some of the different terms used to discuss PowerShell.</span></span>

- <span data-ttu-id="e7c94-126">**PowerShell** : il s’agit du terme par défaut.</span><span class="sxs-lookup"><span data-stu-id="e7c94-126">**PowerShell** - This is the default.</span></span> <span data-ttu-id="e7c94-127">PowerShell est le produit que nous livrons.</span><span class="sxs-lookup"><span data-stu-id="e7c94-127">PowerShell is the product we ship.</span></span> <span data-ttu-id="e7c94-128">Le terme PowerShell peut être utilisé pour décrire n’importe quelle édition du produit.</span><span class="sxs-lookup"><span data-stu-id="e7c94-128">The term PowerShell can be used to describe any edition of the product.</span></span>
- <span data-ttu-id="e7c94-129">**PowerShell Core** : PowerShell basé sur le CLR (Common Language Runtime) .NET Core (CoreCLR) pour toutes les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e7c94-129">**PowerShell Core** - PowerShell built on .NET Core Common Language Runtime (CoreCLR) for any of the supported platforms.</span></span>
- <span data-ttu-id="e7c94-130">**Windows PowerShell** : PowerShell basé sur le CLR (Common Language Runtime) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e7c94-130">**Windows PowerShell** - PowerShell built on .NET Framework Common Language Runtime (CLR).</span></span> <span data-ttu-id="e7c94-131">Windows PowerShell est fourni uniquement sur Windows et nécessite le CLR .NET Framework complet.</span><span class="sxs-lookup"><span data-stu-id="e7c94-131">Windows PowerShell ships only on Windows and requires the full .Net Framework CLR.</span></span>

<span data-ttu-id="e7c94-132">En général, les références à « Windows PowerShell » dans la documentation peuvent être remplacées par « PowerShell ».</span><span class="sxs-lookup"><span data-stu-id="e7c94-132">In general, references to "Windows PowerShell" in documentation can be changed to "PowerShell".</span></span>
<span data-ttu-id="e7c94-133">« Windows PowerShell » ne doit **pas** être changé quand il est question de la technologie spécifique à Windows.</span><span class="sxs-lookup"><span data-stu-id="e7c94-133">"Windows PowerShell" should **not** be changed when Windows-specific technology is being discussed.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="e7c94-134">Markdown de base, GFM et caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="e7c94-134">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="e7c94-135">Pour découvrir les principes de base de Markdown, de GFM (GitHub Flavored Markdown) et des extensions propres à OPS, consultez les articles généraux sur [Markdown](../how-to-write-use-markdown.md) et la [référence Markdown](../markdown-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-135">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](../how-to-write-use-markdown.md) and [Markdown reference](../markdown-reference.md).</span></span>

<span data-ttu-id="e7c94-136">Markdown utilise des caractères spéciaux tels que \*, \` et \# pour la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="e7c94-136">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="e7c94-137">Si vous souhaitez inclure l’un de ces caractères dans votre contenu, vous devez effectuer l’une des deux opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e7c94-137">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="e7c94-138">Placer une barre oblique inverse avant le caractère spécial pour l’« échapper » (par exemple `\*` pour \*)</span><span class="sxs-lookup"><span data-stu-id="e7c94-138">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="e7c94-139">Utiliser le [code d’entité HTML](http://www.ascii.cl/htmlcodes.htm) pour le caractère (par exemple `&#42;` pour &#42;)</span><span class="sxs-lookup"><span data-stu-id="e7c94-139">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>
- <span data-ttu-id="e7c94-140">Les fichiers Markdown doivent utiliser du texte ASCII brut ou l’encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="e7c94-140">Markdown files should use plain ASCII text or UTF-8 encoding.</span></span> <span data-ttu-id="e7c94-141">Évitez cependant d’utiliser des caractères UTF-8 multioctets.</span><span class="sxs-lookup"><span data-stu-id="e7c94-141">However, avoid using multi-byte UTF-8 characters.</span></span> <span data-ttu-id="e7c94-142">Utilisez à la place une entité HTML.</span><span class="sxs-lookup"><span data-stu-id="e7c94-142">Instead use an HTML entity.</span></span> <span data-ttu-id="e7c94-143">Par exemple, pour les symboles de copyright, utilisez `&copy;`.</span><span class="sxs-lookup"><span data-stu-id="e7c94-143">For example, for the copyright symbols use `&copy;`.</span></span>
  <span data-ttu-id="e7c94-144">Il est rendu sous la forme &copy;.</span><span class="sxs-lookup"><span data-stu-id="e7c94-144">It is rendered as: "&copy;".</span></span>

## <a name="hyperlinks"></a><span data-ttu-id="e7c94-145">Liens hypertexte</span><span class="sxs-lookup"><span data-stu-id="e7c94-145">Hyperlinks</span></span>

- <span data-ttu-id="e7c94-146">Évitez d’utiliser des URL nues.</span><span class="sxs-lookup"><span data-stu-id="e7c94-146">Avoid using bare URLs.</span></span> <span data-ttu-id="e7c94-147">Les liens doivent utiliser la syntaxe Markdown `[friendlyname](url-or-path)`</span><span class="sxs-lookup"><span data-stu-id="e7c94-147">Links should use Markdown syntax `[friendlyname](url-or-path)`</span></span>
- <span data-ttu-id="e7c94-148">Les liens doivent avoir un nom convivial, généralement le titre de la rubrique liée</span><span class="sxs-lookup"><span data-stu-id="e7c94-148">Links must have a friendly name, usually the title of the linked topic</span></span>
- <span data-ttu-id="e7c94-149">Tous les éléments de la section « Liens connexes » dans le bas doivent être liés par un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="e7c94-149">All items in the "related links" section at the bottom should be hyperlinked.</span></span>
- <span data-ttu-id="e7c94-150">Utilisez des liens relatifs pour lier à un autre contenu hébergé sur **docs.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-150">Use relative links when linking to other content that is hosted on **docs.microsoft.com**.</span></span>
- <span data-ttu-id="e7c94-151">N’utilisez pas d’accents graves, du gras ou un autre balisage à l’intérieur des crochets d’un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="e7c94-151">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

<span data-ttu-id="e7c94-152">Pour plus d’informations sur les liens, consultez [Utilisation de liens dans la documentation](../how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-152">For more detailed information about linking, see [Using links in documentation](../how-to-write-links.md).</span></span>

## <a name="filenames"></a><span data-ttu-id="e7c94-153">Noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="e7c94-153">Filenames</span></span>

<span data-ttu-id="e7c94-154">Les noms de fichiers suivent les règles ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e7c94-154">Filenames use the following rules:</span></span>

- <span data-ttu-id="e7c94-155">Ils contiennent seulement des lettres, des chiffres et des traits d’union.</span><span class="sxs-lookup"><span data-stu-id="e7c94-155">Contain only letters, numbers, and hyphens.</span></span>
- <span data-ttu-id="e7c94-156">Ils ne doivent pas contenir d’espaces ni de caractères de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="e7c94-156">No spaces or punctuation characters.</span></span> <span data-ttu-id="e7c94-157">Utilisez des traits d’union pour séparer les mots et les chiffres compris dans le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e7c94-157">Use the hyphens to separate words and numbers in the file name.</span></span>
- <span data-ttu-id="e7c94-158">Utilisez des verbes d’action spécifiques, tels que « développer », « acheter », « créer », « dépanner », etc.</span><span class="sxs-lookup"><span data-stu-id="e7c94-158">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="e7c94-159">Ils ne doivent pas comprendre de mots se terminant par « -ing ».</span><span class="sxs-lookup"><span data-stu-id="e7c94-159">No -ing words.</span></span>
- <span data-ttu-id="e7c94-160">Ils ne doivent pas comprendre de mots courts (« un », « et », « le », « en », « ou », etc.).</span><span class="sxs-lookup"><span data-stu-id="e7c94-160">No small words - don't include a, and, the, in, or, etc.</span></span>
- <span data-ttu-id="e7c94-161">Ils doivent être au format Markdown et avoir l’extension de fichier .md.</span><span class="sxs-lookup"><span data-stu-id="e7c94-161">Must be in Markdown and use the .md file extension.</span></span>
- <span data-ttu-id="e7c94-162">Faites en sorte que les noms de fichiers soient le plus court possible.</span><span class="sxs-lookup"><span data-stu-id="e7c94-162">Keep file names reasonably short.</span></span> <span data-ttu-id="e7c94-163">Ils font partie de l’URL de vos articles.</span><span class="sxs-lookup"><span data-stu-id="e7c94-163">They are part of the URL for your articles.</span></span>

## <a name="blank-lines-spaces-and-tabs"></a><span data-ttu-id="e7c94-164">Lignes vides, espaces et tabulations</span><span class="sxs-lookup"><span data-stu-id="e7c94-164">Blank lines, spaces, and tabs</span></span>

<span data-ttu-id="e7c94-165">Supprimez les lignes vides en double.</span><span class="sxs-lookup"><span data-stu-id="e7c94-165">Remove duplicate blank lines.</span></span> <span data-ttu-id="e7c94-166">Les lignes vides multiples s’affichent sous la forme d’une seule ligne vide en HTML : il est donc inutile de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="e7c94-166">Multiple blank lines render as a single blank line in HTML so there is not purpose for multiple blank lines.</span></span>

<span data-ttu-id="e7c94-167">Les lignes vides indiquent aussi la fin d’un bloc dans Markdown.</span><span class="sxs-lookup"><span data-stu-id="e7c94-167">Blank lines also signal the end of a block in Markdown.</span></span> <span data-ttu-id="e7c94-168">Il ne doit y avoir qu’un seul espace entre les blocs Markdown de différents types (par exemple entre un paragraphe et une liste ou un en-tête).</span><span class="sxs-lookup"><span data-stu-id="e7c94-168">There should be a single blank between Markdown blocks of different types (for example, between a paragraph and a list or header).</span></span>

> [!NOTE]
> <span data-ttu-id="e7c94-169">L’espacement a une signification dans Markdown.</span><span class="sxs-lookup"><span data-stu-id="e7c94-169">Spacing is significant in Markdown.</span></span> <span data-ttu-id="e7c94-170">Utilisez toujours des espaces à la place de tabulations en dur.</span><span class="sxs-lookup"><span data-stu-id="e7c94-170">Always uses spaces instead of hard tabs.</span></span> <span data-ttu-id="e7c94-171">Supprimez les espaces en trop à la fin des lignes.</span><span class="sxs-lookup"><span data-stu-id="e7c94-171">Remove extra spaces at the end of lines.</span></span>

## <a name="titles-and-headings"></a><span data-ttu-id="e7c94-172">Titres et en-têtes</span><span class="sxs-lookup"><span data-stu-id="e7c94-172">Titles and headings</span></span>

<span data-ttu-id="e7c94-173">Utilisez uniquement des [en-têtes ATX][atx] (de style #, et non pas des en-têtes de style `=` ou `-`).</span><span class="sxs-lookup"><span data-stu-id="e7c94-173">Only use [ATX headings][atx] (# style, as opposed to `=` or `-` style headers).</span></span>

- <span data-ttu-id="e7c94-174">Utilisez la casse classique des phrases : seuls les noms propres et la première lettre d’un titre ou d’un en-tête prennent une majuscule</span><span class="sxs-lookup"><span data-stu-id="e7c94-174">Use sentence case - only proper nouns and the first letter of a title or header should be capitalized</span></span>
- <span data-ttu-id="e7c94-175">Il doit y avoir un seul espace entre le `#` et la première lettre du titre</span><span class="sxs-lookup"><span data-stu-id="e7c94-175">There must be a single space between the `#` and the first letter of the heading</span></span>
- <span data-ttu-id="e7c94-176">Les titres doivent être précédés et suivis d’une seule ligne vide</span><span class="sxs-lookup"><span data-stu-id="e7c94-176">Headings should be surrounded by a single blank line</span></span>
- <span data-ttu-id="e7c94-177">Un seul titre H1 par document</span><span class="sxs-lookup"><span data-stu-id="e7c94-177">Only one H1 per document</span></span>
- <span data-ttu-id="e7c94-178">Les niveaux d’en-tête doivent être incrémentés d’une unité : ne passez pas un niveau</span><span class="sxs-lookup"><span data-stu-id="e7c94-178">Header levels should increment by one - do not skip levels</span></span>
- <span data-ttu-id="e7c94-179">N’utilisez pas d’accents graves, de gras ou un autre balisage dans les en-têtes</span><span class="sxs-lookup"><span data-stu-id="e7c94-179">Do not use backticks, bold, or other markup in headers</span></span>

> [!CAUTION]
> <span data-ttu-id="e7c94-180">Le schéma appliqué par [PlatyPS][platyPS] pour les informations de référence des applets de commande nécessite des en-têtes H2 et H3 spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e7c94-180">The schema enforced by [PlatyPS][platyPS] for cmdlet reference requires specific H2 and H3 headers.</span></span> <span data-ttu-id="e7c94-181">L’ajout ou la suppression d’en-têtes peut entraîner un arrêt de la build.</span><span class="sxs-lookup"><span data-stu-id="e7c94-181">Adding or removing headers can break the build.</span></span> <span data-ttu-id="e7c94-182">Pour plus d’informations, consultez le [Guide de style des informations de référence des applets de commande](powershell-style-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e7c94-182">For more information, see the [cmdlet reference style guide](powershell-style-reference.md).</span></span>

## <a name="limit-line-length-to-100-characters"></a><span data-ttu-id="e7c94-183">Limitez la longueur des lignes à 100 caractères</span><span class="sxs-lookup"><span data-stu-id="e7c94-183">Limit line length to 100 characters</span></span>

<span data-ttu-id="e7c94-184">Cela simplifie la sortie des différences et de l’historique des lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="e7c94-184">This simplifies the command-line output of diffs and history.</span></span>

<span data-ttu-id="e7c94-185">Cette règle n’a pas été appliquée pour la majeure partie du contenu existant dans PowerShell-Docs, mais nous l’appliquons au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="e7c94-185">This rule was not in force for much of the existing content in PowerShell-Docs, but we are working towards it over time.</span></span> <span data-ttu-id="e7c94-186">N’hésitez pas à nous aider. L’extension [reflow][reflow] de Visual Studio Code (VSCode) facilite la remise en forme des paragraphes avec cette limite.</span><span class="sxs-lookup"><span data-stu-id="e7c94-186">Feel free to help out. The [reflow extension][reflow] in Visual Studio Code (VSCode) makes it easy to reformat paragraphs to this limit.</span></span>

## <a name="lists"></a><span data-ttu-id="e7c94-187">Listes</span><span class="sxs-lookup"><span data-stu-id="e7c94-187">Lists</span></span>

<span data-ttu-id="e7c94-188">Si votre liste contient plusieurs phrases ou paragraphes, envisagez d’utiliser un en-tête de sous-niveau au lieu d’une liste.</span><span class="sxs-lookup"><span data-stu-id="e7c94-188">If your list contains multiple sentences or paragraphs, consider using a sub-level header rather than a list.</span></span>

<span data-ttu-id="e7c94-189">Les listes doivent être précédées et suivies d’une seule ligne vide.</span><span class="sxs-lookup"><span data-stu-id="e7c94-189">List should be surrounded by a single blank line.</span></span>

### <a name="unordered-lists"></a><span data-ttu-id="e7c94-190">Listes non triées</span><span class="sxs-lookup"><span data-stu-id="e7c94-190">Unordered lists</span></span>

<span data-ttu-id="e7c94-191">Ne terminez pas les éléments d’une liste par un point, sauf s’ils contiennent plusieurs phrases.</span><span class="sxs-lookup"><span data-stu-id="e7c94-191">Do not end list items with a period unless they contain multiple sentences.</span></span> <span data-ttu-id="e7c94-192">Utilisez le caractère de trait d’union (`-`) pour les puces des éléments d’une liste.</span><span class="sxs-lookup"><span data-stu-id="e7c94-192">Use the hyphen character (`-`) for list item bullets.</span></span> <span data-ttu-id="e7c94-193">Cela évite la confusion avec un balisage en gras ou en italique qui utilise l’astérisque [`*`].</span><span class="sxs-lookup"><span data-stu-id="e7c94-193">This avoids confusion with bold or italic markup that uses the asterisk [`*`].</span></span> <span data-ttu-id="e7c94-194">Pour inclure un paragraphe ou d’autres éléments sous un élément à puce, insérez un saut de ligne et alignez l’indentation sur le premier caractère après la puce.</span><span class="sxs-lookup"><span data-stu-id="e7c94-194">To include a paragraph or other elements under a bullet item, insert a line break and align indentation with the first character after the bullet.</span></span>

<span data-ttu-id="e7c94-195">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-195">For example:</span></span>

```markdown
This is a list that contain sub-elements under a bullet item.

- First bullet item

  Sentence explaining the first bullet.

  - Sub-bullet item

    Sentence explaining the sub-bullet.

- Second bullet item
- Third bullet item
```

<span data-ttu-id="e7c94-196">Voici une liste qui contient des sous-éléments sous un élément à puce.</span><span class="sxs-lookup"><span data-stu-id="e7c94-196">This is a list that contains sub-elements under a bullet item.</span></span>

- <span data-ttu-id="e7c94-197">Premier élément à puce</span><span class="sxs-lookup"><span data-stu-id="e7c94-197">First bullet item</span></span>

  <span data-ttu-id="e7c94-198">Phrase expliquant la première puce.</span><span class="sxs-lookup"><span data-stu-id="e7c94-198">Sentence explaining the first bullet.</span></span>

  - <span data-ttu-id="e7c94-199">Élément à sous-puce</span><span class="sxs-lookup"><span data-stu-id="e7c94-199">Sub-bullet item</span></span>

    <span data-ttu-id="e7c94-200">Phrase expliquant la sous-puce.</span><span class="sxs-lookup"><span data-stu-id="e7c94-200">Sentence explaining the sub-bullet.</span></span>

- <span data-ttu-id="e7c94-201">Deuxième élément à puce</span><span class="sxs-lookup"><span data-stu-id="e7c94-201">Second bullet item</span></span>
- <span data-ttu-id="e7c94-202">Troisième élément à puce</span><span class="sxs-lookup"><span data-stu-id="e7c94-202">Third bullet item</span></span>

### <a name="ordered-lists"></a><span data-ttu-id="e7c94-203">Listes triées</span><span class="sxs-lookup"><span data-stu-id="e7c94-203">Ordered lists</span></span>

<span data-ttu-id="e7c94-204">Pour inclure un paragraphe ou d’autres éléments sous un élément numéroté, alignez l’indentation sur le premier caractère après le numéro de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e7c94-204">To include a paragraph or other elements under a numbered item, align indentation with the first character after the item number.</span></span>

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

<span data-ttu-id="e7c94-205">Pour obtenir ce résultat :</span><span class="sxs-lookup"><span data-stu-id="e7c94-205">to get this output:</span></span>

> 1. <span data-ttu-id="e7c94-206">Pour le premier élément, insérez un espace après 1.</span><span class="sxs-lookup"><span data-stu-id="e7c94-206">For the first element, insert a single space after the 1.</span></span> <span data-ttu-id="e7c94-207">Les phrases longues doivent être renvoyées à la ligne suivante et être alignées sur le premier caractère après le marqueur de liste numérotée.</span><span class="sxs-lookup"><span data-stu-id="e7c94-207">Long sentences should be wrapped to the next line and must line up with the first character after the numbered list marker.</span></span>
>
>    <span data-ttu-id="e7c94-208">Pour inclure un deuxième élément (comme celui-ci), insérez un saut de ligne après le premier élément et alignez les indentations.</span><span class="sxs-lookup"><span data-stu-id="e7c94-208">To include a second element (like this one), insert a line break after the first and align indentations.</span></span> <span data-ttu-id="e7c94-209">L’indentation du deuxième élément doit être alignée sur le premier caractère après le marqueur de liste numérotée.</span><span class="sxs-lookup"><span data-stu-id="e7c94-209">The indentation of the second element must line up with the first character after the numbered list marker.</span></span> <span data-ttu-id="e7c94-210">Pour les éléments à un seul chiffre, comme celui-ci, vous indentez à la colonne 4.</span><span class="sxs-lookup"><span data-stu-id="e7c94-210">For single digit items, like this one, you indent to column 4.</span></span> <span data-ttu-id="e7c94-211">Pour les éléments à deux chiffres, par exemple le numéro d’élément 10, vous indentez à la colonne 5.</span><span class="sxs-lookup"><span data-stu-id="e7c94-211">For double digits items, for example item number 10, you indent to column 5.</span></span>
>
> 1. <span data-ttu-id="e7c94-212">L’élément numéroté suivant commence ici.</span><span class="sxs-lookup"><span data-stu-id="e7c94-212">The next numbered item starts here.</span></span>

<span data-ttu-id="e7c94-213">Tous les éléments d’une liste numérotée doivent utiliser le nombre `1.` au lieu de l’incrémenter pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="e7c94-213">All items in a numbered listed should use the number `1.` instead of incrementing for each item.</span></span>
<span data-ttu-id="e7c94-214">Le rendu de Markdown incrémente automatiquement la valeur.</span><span class="sxs-lookup"><span data-stu-id="e7c94-214">Markdown rendering increments the value automatically.</span></span> <span data-ttu-id="e7c94-215">Cela facilite la réorganisation des éléments et standardise l’indentation du contenu subordonné.</span><span class="sxs-lookup"><span data-stu-id="e7c94-215">This makes reordering items easier and standardizes the indentation of subordinate content.</span></span>

## <a name="formatting-command-syntax-elements"></a><span data-ttu-id="e7c94-216">Mise en forme des éléments de la syntaxe des commandes</span><span class="sxs-lookup"><span data-stu-id="e7c94-216">Formatting command syntax elements</span></span>

- <span data-ttu-id="e7c94-217">Les noms des applets de commande PowerShell ont une [casse Pascal][pascal-case].</span><span class="sxs-lookup"><span data-stu-id="e7c94-217">PowerShell cmdlet names are [Pascal Cased][pascal-case].</span></span> <span data-ttu-id="e7c94-218">Les verbes sont séparés des noms par un trait d’union.</span><span class="sxs-lookup"><span data-stu-id="e7c94-218">Verbs are separated from nouns by a hyphen.</span></span> <span data-ttu-id="e7c94-219">Utilisez toujours le nom complet en casse Pascal pour les applets de commande et les paramètres.</span><span class="sxs-lookup"><span data-stu-id="e7c94-219">Always use the full Pascal Case name for cmdlets and parameters.</span></span> <span data-ttu-id="e7c94-220">Évitez d’utiliser des alias, sauf si vous parlez spécifiquement d’un alias.</span><span class="sxs-lookup"><span data-stu-id="e7c94-220">Avoid using aliases unless you are specifically talking about an alias.</span></span>

- <span data-ttu-id="e7c94-221">Dans un paragraphe, les mots clés du langage, les noms des applets de commande et les références de variable doivent être entourés de caractères d’accent grave (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="e7c94-221">Within a paragraph, language keywords, cmdlet names, and variable references should be wrapped in backtick (`` ` ``) characters.</span></span> <span data-ttu-id="e7c94-222">Les noms des propriétés, des paramètres et des classes doivent être en **gras**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-222">Property, parameter, and class names should be **bold**.</span></span>

  <span data-ttu-id="e7c94-223">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-223">For example:</span></span>

  ~~~markdown
  The following code assigns the output of `Get-ChildItem` to the `$files` variable.

  ```powershell
  $files = Get-ChildItem C:\Windows
  ```
  ~~~

- <span data-ttu-id="e7c94-224">Quand vous faites référence à un paramètre par son nom, le nom doit être en **gras**.</span><span class="sxs-lookup"><span data-stu-id="e7c94-224">When referring to a parameter by name, the name should be **bold**.</span></span> <span data-ttu-id="e7c94-225">Lors de l’illustration de l’utilisation d’un paramètre avec le préfixe de trait d’union, le paramètre doit être entouré d’accents graves.</span><span class="sxs-lookup"><span data-stu-id="e7c94-225">When illustrating the use of a parameter with the hyphen prefix, the parameter should be wrapped in backticks.</span></span> <span data-ttu-id="e7c94-226">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-226">For example:</span></span>

  ```markdown
  The parameter's name is **Name**, but it is typed as `-Name` when used on the command
  line as a parameter.
  ```

- <span data-ttu-id="e7c94-227">Quand vous faites référence à des commandes externes (des fichiers exécutables, des scripts, etc.), le nom de la commande doit être en gras, tout en minuscules (ou avec une majuscule s’il est au début d’une phrase) et inclure l’extension de fichier appropriée.</span><span class="sxs-lookup"><span data-stu-id="e7c94-227">When referring to external commands (EXEs, scripts, etc.), the command name should be bold, all lowercase (or capitalized if at the beginning of a sentence), and include the appropriate file extension.</span></span> <span data-ttu-id="e7c94-228">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-228">For example:</span></span>

  ```markdown
  For example, on Windows systems, you can use the `net start` and `net stop` commands
  to start and stop a service. **Sc.exe** is another service control tool for Windows.
  That name does not fit into the naming pattern for the **net.exe** service commands.
  ```

- <span data-ttu-id="e7c94-229">Quand vous montrez un exemple d’utilisation d’une commande externe, l’exemple doit être entouré d’accents graves.</span><span class="sxs-lookup"><span data-stu-id="e7c94-229">When showing example usage of an external command, the example should be wrapped in backticks.</span></span>
  <span data-ttu-id="e7c94-230">En cas de conflit de noms avec un alias, vous devez inclure l’extension de fichier dans l’exemple de commande.</span><span class="sxs-lookup"><span data-stu-id="e7c94-230">When there is a name collision with an alias you must include the file extension in the command example.</span></span> <span data-ttu-id="e7c94-231">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-231">For example:</span></span>

  ```markdown
  To start the spooler service on a remote computer named DC01, you type `sc.exe \\DC01 start spooler`.
  ```

- <span data-ttu-id="e7c94-232">Lors de l’écriture d’un article conceptuel (par opposition au contenu des informations de référence), la première occurrence du nom d’une applet de commande doit avoir un lien hypertexte vers la documentation de l’applet de commande.</span><span class="sxs-lookup"><span data-stu-id="e7c94-232">When writing a conceptual article (as opposed to reference content), the first instance of a cmdlet name should be hyperlinked to the cmdlet documentation.</span></span> <span data-ttu-id="e7c94-233">N’utilisez pas d’accents graves, du gras ou un autre balisage à l’intérieur des crochets d’un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="e7c94-233">Do not use backticks, bold, or other markup inside the brackets of a hyperlink.</span></span>

  <span data-ttu-id="e7c94-234">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-234">For example:</span></span>

  ```markdown
  This [Write-Host](/powershell/module/Microsoft.PowerShell.Utility/Write-Host) cmdlet
  uses the **Object** parameter to ...
  ```

  <span data-ttu-id="e7c94-235">Pour plus d’informations, consultez la section [Liens hypertexte](#hyperlinks) du Guide de style.</span><span class="sxs-lookup"><span data-stu-id="e7c94-235">For more information, see [Hyperlinks](#hyperlinks) section of the Style Guide.</span></span>

## <a name="images"></a><span data-ttu-id="e7c94-236">Images</span><span class="sxs-lookup"><span data-stu-id="e7c94-236">Images</span></span>

<span data-ttu-id="e7c94-237">La syntaxe pour inclure une image est :</span><span class="sxs-lookup"><span data-stu-id="e7c94-237">The syntax to include an image is:</span></span>

```Syntax
![[alt text]](<folderPath>)
```

<span data-ttu-id="e7c94-238">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e7c94-238">Example:</span></span>

```markdown
![Introduction](./media/overview/Introduction.png)
```

<span data-ttu-id="e7c94-239">Où `alt text` est une brève description de l’image et `<folder path>` un chemin relatif de l’image.</span><span class="sxs-lookup"><span data-stu-id="e7c94-239">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="e7c94-240">Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants.</span><span class="sxs-lookup"><span data-stu-id="e7c94-240">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="e7c94-241">Ce texte est également utile dans le cas où un bogue du site empêche l’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="e7c94-241">It is also useful in case there is a site bug where the image cannot be rendered.</span></span>

<span data-ttu-id="e7c94-242">Les images doivent être stockées dans un dossier `media/<article-name>` dans le dossier contenant votre article.</span><span class="sxs-lookup"><span data-stu-id="e7c94-242">Images should be stored in a `media/<article-name>` folder within the folder containing your article.</span></span> <span data-ttu-id="e7c94-243">Les images ne doivent pas être partagées entre des articles.</span><span class="sxs-lookup"><span data-stu-id="e7c94-243">Images should not be shared between articles.</span></span> <span data-ttu-id="e7c94-244">Créez un dossier qui correspond au nom de fichier de votre article sous le dossier `media`.</span><span class="sxs-lookup"><span data-stu-id="e7c94-244">Create a folder that matches the filename of your article under the `media` folder.</span></span> <span data-ttu-id="e7c94-245">Copiez les images pour cet article dans ce nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="e7c94-245">Copy the images for that article to that new folder.</span></span> <span data-ttu-id="e7c94-246">Si une image est utilisée par plusieurs articles, chaque dossier d’images doit avoir une copie de ce fichier d’image.</span><span class="sxs-lookup"><span data-stu-id="e7c94-246">If an image is used by multiple articles, each image folder must have a copy of that image file.</span></span> <span data-ttu-id="e7c94-247">Cette pratique permet d’éviter que la modification d’une image dans un article affecte un autre article.</span><span class="sxs-lookup"><span data-stu-id="e7c94-247">This practice prevents a change to an image in one article affecting another article.</span></span>

<span data-ttu-id="e7c94-248">Dans certains cas, vous voulez partager des images, comme des logos et des icônes, entre plusieurs articles.</span><span class="sxs-lookup"><span data-stu-id="e7c94-248">In some cases, you want to share images, like logos and icons, across multiple articles.</span></span> <span data-ttu-id="e7c94-249">Ces images sont stockées dans le dossier `/media/shared` à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="e7c94-249">These images are stored in the `/media/shared` folder at the root of the repository.</span></span>

<span data-ttu-id="e7c94-250">Les types de fichiers d’image suivants sont pris en charge : \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span><span class="sxs-lookup"><span data-stu-id="e7c94-250">The following image file types are supported: \*.png", \*.gif", \*.jpeg", \*.jpg", \*.svg</span></span>

<!-- External URLs -->
[platyPS]: https://github.com/PowerShell/platyPS
[markdig]: https://github.com/lunet-io/markdig
[CommonMark]: https://spec.commonmark.org/
[atx]: https://github.github.com/gfm/#atx-headings
[pascal-case]: https://en.wikipedia.org/wiki/PascalCase
[reflow]: https://marketplace.visualstudio.com/items?itemName=marvhen.reflow-markdown
