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
# <a name="use-links-in-documentation"></a><span data-ttu-id="5ebb7-103">Utiliser des liens dans la documentation</span><span class="sxs-lookup"><span data-stu-id="5ebb7-103">Use links in documentation</span></span>

<span data-ttu-id="5ebb7-104">Cet article décrit comment utiliser des liens hypertexte à partir de pages hébergées sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="5ebb7-105">Vous pouvez facilement ajouter des liens dans la syntaxe Markdown en tenant compte de quelques conventions.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="5ebb7-106">Les liens pointent vers du contenu situé dans la même page, dans d’autres pages voisines ou vers des sites et des URL externes.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-106">Links point users to content in the same page, in other neighboring pages, or on external sites and URLs.</span></span>

<span data-ttu-id="5ebb7-107">Le back-end du site docs.microsoft.com utilise OPS (Open Publishing Services) qui prend en charge Markdown conforme avec [CommonMark][] analysé via le moteur [Markdig][].</span><span class="sxs-lookup"><span data-stu-id="5ebb7-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS), which supports [CommonMark][]-compliant markdown parsed through the [Markdig][] parsing engine.</span></span> <span data-ttu-id="5ebb7-108">Ce type Markdown est essentiellement compatible avec [GitHub Flavored Markdown (GFM)][GFM], car la plupart des documents sont stockés dans GitHub et peuvent être modifiés à cet endroit.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-108">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)][GFM], as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="5ebb7-109">Des fonctionnalités sont ajoutées via des extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-109">Additional functionality is added through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ebb7-110">Tous les liens doivent être sécurisés (`https` et `http`) lorsque la cible le permet (dans la grande majorité des cas).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-110">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="5ebb7-111">Texte du lien</span><span class="sxs-lookup"><span data-stu-id="5ebb7-111">Link text</span></span>

<span data-ttu-id="5ebb7-112">Les mots que vous incluez dans le texte doivent être conviviaux.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-112">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="5ebb7-113">En d’autres termes, il doit s’agir de mots simples ou du titre de la page vers laquelle vous établissez le lien.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-113">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ebb7-114">N’utilisez pas de texte de type « cliquez ici ».</span><span class="sxs-lookup"><span data-stu-id="5ebb7-114">Do not use "click here."</span></span> <span data-ttu-id="5ebb7-115">Ce n’est pas bon pour l’optimisation du référencement d’un site auprès d’un moteur de recherche et cela ne décrit pas correctement la cible.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-115">It's bad for search engine optimization and doesn't adequately describe the target.</span></span>

<span data-ttu-id="5ebb7-116">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="5ebb7-116">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://docs.microsoft.com/sql/t-sql/statements/set-transaction-isolation-level-transact-sql) reference.`

<span data-ttu-id="5ebb7-117">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="5ebb7-117">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="5ebb7-118">Liens d'un article à un autre</span><span class="sxs-lookup"><span data-stu-id="5ebb7-118">Links from one article to another</span></span>

<span data-ttu-id="5ebb7-119">Deux types de liens hypertexte sont pris en charge par le système de publication : les **URL** et les **liens vers des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-119">There are two types of hyperlinks supported by the publishing system: **URLs** and **file links**.</span></span>

<span data-ttu-id="5ebb7-120">Un lien URL peut être un chemin d’URL relatif à la racine de docs.microsoft.com ou une URL absolue qui inclut la syntaxe complète de l’URL (par exemple, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-120">A URL link can be a URL path that is relative to the root of docs.microsoft.com, or an absolute URL that includes the full URL syntax (for example, `https://github.com/MicrosoftDocs/PowerShell-Docs`).</span></span>

- <span data-ttu-id="5ebb7-121">Utilisez un lien URL pour établir un lien vers du contenu situé en dehors du _docset_ actif ou entre des articles de référence et conceptuels générés automatiquement dans le docset.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-121">Use URL links when linking to content outside of the current _docset_ or between autogenerated reference and conceptual articles within the docset.</span></span>
- <span data-ttu-id="5ebb7-122">Le moyen le plus simple de créer un lien relatif consiste à copier l’URL à partir de votre navigateur, puis à supprimer `https://docs.microsoft.com/en-us` de la valeur que vous collez dans le code Markdown.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-122">The simplest way to create a relative link is to copy the URL from your browser, then remove `https://docs.microsoft.com/en-us` from the value you paste into markdown.</span></span>
   - <span data-ttu-id="5ebb7-123">N’incluez pas de paramètres régionaux dans les URL pour les propriétés Microsoft (par exemple, supprimez « /en-US » de l’URL).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-123">Do not include locales in URLs for Microsoft properties (for example, remove "/en-us" from the URL).</span></span>

<span data-ttu-id="5ebb7-124">Un lien vers un fichier permet de lier un article à un autre dans le docset.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-124">A file link is used to link from one article to another within the docset.</span></span>

- <span data-ttu-id="5ebb7-125">Tous les chemins à des fichiers utilisent des barres obliques (`/`), et non des barres obliques inverses.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-125">All file paths use forward-slash (`/`) characters instead of back-slash characters.</span></span>
- <span data-ttu-id="5ebb7-126">Un article a un lien vers un autre article du même répertoire :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-126">An article links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="5ebb7-127">Un article a un lien vers un article du répertoire parent du répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-127">An article links to an article in the parent directory of the current directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="5ebb7-128">Un article a un lien vers un article d’un sous-répertoire du répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-128">An article links to an article in a subdirectory of the current directory:</span></span>

  `[link text](directory/article-name.md)`

- <span data-ttu-id="5ebb7-129">Un article a un lien vers un article d’un sous-répertoire du répertoire parent du répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-129">An article links to an article in a subdirectory of the parent directory of the current directory:</span></span>

  `[link text](../directory/article-name.md)`

> [!NOTE]
> <span data-ttu-id="5ebb7-130">Aucun des exemples précédents n’utilise de `~/` dans le lien.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-130">None of the previous examples use the `~/` as part of the link.</span></span> <span data-ttu-id="5ebb7-131">Pour créer un lien vers un chemin absolu qui commence à la racine du dépôt, commencez le lien avec `/`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-131">To link to an absolute path that begins at the root of the repository, start the link with `/`.</span></span> <span data-ttu-id="5ebb7-132">L’ajout d’un `~/` produit des liens non valides quand vous accédez aux dépôts sources sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-132">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="5ebb7-133">En commençant par une `/`, le problème est résolu.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-133">Starting the path with `/` resolves correctly.</span></span>

### <a name="structure-of-links-on-docsmicrosoftcom"></a><span data-ttu-id="5ebb7-134">Structure des liens sur docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5ebb7-134">Structure of links on docs.microsoft.com</span></span>

<span data-ttu-id="5ebb7-135">Le contenu publié sur docs.microsoft.com repose sur la structure d’URL suivante :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-135">Content published on docs.microsoft.com has the following URL structure:</span></span>

```
https://docs.microsoft.com/<locale>/<product-service>/[<feature-service>]/[<subfolder>]/<topic>[?view=<view-name>]
```

<span data-ttu-id="5ebb7-136">Exemples :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-136">Examples:</span></span>

```
https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview
https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-5.1.1
```

- <span data-ttu-id="5ebb7-137">`<locale>` - Identifie la langue de l’article (par exemple : en-us ou fr-fr)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-137">`<locale>` - identifies the language of the article (example: en-us or de-de)</span></span>
- <span data-ttu-id="5ebb7-138">`<product-service>` - Nom du produit ou du service (par exemple : powershell, dotnet ou azure)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-138">`<product-service>` - the name of the product or service (example: powershell, dotnet, or azure)</span></span>
- <span data-ttu-id="5ebb7-139">`[<feature-service>]` (facultatif) - Nom de la fonctionnalité ou du sous-service du produit (par exemple : csharp ou load-balancer)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-139">`[<feature-service>]` - (optional) the name of the product's feature or subservice (example: csharp or load-balancer)</span></span>
- <span data-ttu-id="5ebb7-140">`[<subfolder>]` (facultatif) - Nom d’un sous-dossier dans une fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="5ebb7-140">`[<subfolder>]` - (optional) the name of a subfolder within a feature</span></span>
- <span data-ttu-id="5ebb7-141">`<topic>` - Nom du fichier de l’article pour la rubrique (par exemple : load-balancer-overview ou overview)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-141">`<topic>` - the name of the article file for the topic (example: load-balancer-overview or overview)</span></span>
- <span data-ttu-id="5ebb7-142">`[?view=\<view-name>]` (facultatif) - Nom de la vue utilisée par le sélecteur de version pour du contenu disponible dans plusieurs versions (par exemple : azps-3.5.0)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-142">`[?view=\<view-name>]` - (optional) the view name used by the version selector for content that has multiple versions available (example: azps-3.5.0)</span></span>

> [!TIP]
> <span data-ttu-id="5ebb7-143">Dans la plupart des cas, les articles d’un même _docset_ ont le même fragment d’URL `<product-service>`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-143">In most cases, articles in the same _docset_ have the same `<product-service>` URL fragment.</span></span> <span data-ttu-id="5ebb7-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-144">For example:</span></span>
> - <span data-ttu-id="5ebb7-145">Même docset</span><span class="sxs-lookup"><span data-stu-id="5ebb7-145">Same docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/dotnet/framework/install`
> - <span data-ttu-id="5ebb7-146">Docset différent</span><span class="sxs-lookup"><span data-stu-id="5ebb7-146">Different docset</span></span>
>   - `https://docs.microsoft.com/dotnet/core/get-started`
>   - `https://docs.microsoft.com/visualstudio/whats-new`

## <a name="bookmark-links"></a><span data-ttu-id="5ebb7-147">Liens de signet</span><span class="sxs-lookup"><span data-stu-id="5ebb7-147">Bookmark links</span></span>

<span data-ttu-id="5ebb7-148">Pour établir un lien vers un titre marqué d’un signet dans le fichier *actif*, utilisez un symbole de hachage suivi des mots du titre en minuscules.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-148">For a bookmark link to a heading in the *current* file, use a hash symbol followed by the lowercase words of the heading.</span></span> <span data-ttu-id="5ebb7-149">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-149">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="5ebb7-150">Pour établir un lien vers un titre marqué d’un signet dans un autre article, utilisez le lien relatif à un fichier ou relatif à un site plus un symbole dièse, suivi des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-150">To link to a bookmark heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="5ebb7-151">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-151">Remove punctuation from the heading and replace spaces with dashes:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="5ebb7-152">Vous pouvez également copier le lien vers le signet à partir de l’URL.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-152">You can also copy the bookmark link from the URL.</span></span> <span data-ttu-id="5ebb7-153">Pour trouver l’URL, pointez votre souris sur la ligne du titre sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-153">To find the URL, hover your mouse over the heading line on docs.microsoft.com.</span></span> <span data-ttu-id="5ebb7-154">Vous devriez voir une icône de lien :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-154">You should see a link icon appear:</span></span>

![Icône de lien dans le titre de l’article](media/how-to-write-links/bookmark-link.png)

<span data-ttu-id="5ebb7-156">Cliquez sur l’icône de lien, puis copiez le texte de l’ancre du signet à partir de l’URL (c’est-à-dire la partie située après le hachage).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-156">Click the link icon and then copy the bookmark anchor text from the URL (that is, the part after the hash).</span></span>

> [!NOTE]
> <span data-ttu-id="5ebb7-157">L’extension Docs contient également des outils pour vous aider à créer des liens.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-157">The Docs Extension also has tools to help create links.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="5ebb7-158">Liens d’ancrage explicites</span><span class="sxs-lookup"><span data-stu-id="5ebb7-158">Explicit anchor links</span></span>

<span data-ttu-id="5ebb7-159">L’ajout de liens vers des ancres explicites utilisant la balise HTML `<a>` n’est ni obligatoire ni recommandé, sauf dans les pages hub et d’arrivée.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-159">Adding explicit anchor links using the `<a>` HTML tag isn't required or recommended, except in hub and landing pages.</span></span> <span data-ttu-id="5ebb7-160">Utilisez plutôt les signets générés automatiquement, comme décrit dans [Liens de signet](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-160">Instead, use the auto-generated bookmarks as described in [bookmark links](#bookmark-links).</span></span> <span data-ttu-id="5ebb7-161">Pour les pages hub et d’arrivée, déclarez les ancres comme ceci :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-161">For hub and landing pages, declare anchors as follows:</span></span>

```markdown
## <a id="anchortext" />Header text
```

<span data-ttu-id="5ebb7-162">ou</span><span class="sxs-lookup"><span data-stu-id="5ebb7-162">or</span></span>

```markdown
## <a name="anchortext" />Header text
```

<span data-ttu-id="5ebb7-163">Ajoutez ce qui suit pour établir un lien vers l’ancre :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-163">And the following to link to the anchor:</span></span>

```markdown
To go to a section on the same page:
[text](#anchortext)

To go to a section on another page.
[text](filename.md#anchortext)
```

> [!NOTE]
> <span data-ttu-id="5ebb7-164">Le texte de l’ancre doit toujours être en minuscules et ne doit pas contenir d’espaces.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-164">Anchor text must always be lowercase and not contain spaces.</span></span>

## <a name="xref-cross-reference-links"></a><span data-ttu-id="5ebb7-165">Liens XRef (référence croisée)</span><span class="sxs-lookup"><span data-stu-id="5ebb7-165">XRef (cross reference) links</span></span>

<span data-ttu-id="5ebb7-166">Les liens XRef sont la méthode recommandée pour établir des liens vers des API, car ils sont validés au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-166">XRef links are the recommended way to link to APIs, because they're validated at build time.</span></span> <span data-ttu-id="5ebb7-167">Pour créer un lien vers des pages de références d’API générées automatiquement dans le docset actif ou dans d’autres docsets, utilisez des liens XRef avec l’ID unique ([UID](#determine-the-uid)) du type ou membre.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-167">To link to auto-generated API reference pages in the current docset or other docsets, use XRef links with the unique ID ([UID](#determine-the-uid)) of the type or member.</span></span>

> [!TIP]
> <span data-ttu-id="5ebb7-168">Vous pouvez utiliser l’[extension Docs Markdown pour VS Code][docsextension] (fournie avec le Docs Authoring Pack) pour insérer des liens XRref .NET qui sont exposés dans le [navigateur d’API .NET][].</span><span class="sxs-lookup"><span data-stu-id="5ebb7-168">You can use the [Docs Markdown extension for VS Code][docsextension] (part of the Docs Authoring Pack) to insert .NET XRref links that are surfaced in the [.NET API Browser][].</span></span>

<span data-ttu-id="5ebb7-169">Vérifiez que l’API vers laquelle doit pointer votre lien se trouve sur [docs.microsoft.com][docs]. Pour cela, tapez tout ou partie de son nom complet dans la zone de recherche du [navigateur d’API .NET][] ou de [Windows UWP][].</span><span class="sxs-lookup"><span data-stu-id="5ebb7-169">Check if the API you want to link to is on [docs.microsoft.com][docs] by typing all or some of its full name in the [.NET API browser][] or [Windows UWP][] search box.</span></span> <span data-ttu-id="5ebb7-170">Si aucun résultat n’est retourné, le type n’est pas encore sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-170">If you don't see any results displayed, the type isn't yet on docs.microsoft.com.</span></span>

<span data-ttu-id="5ebb7-171">Vous pouvez utiliser une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-171">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="5ebb7-172">Liens automatiques :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-172">Auto-links:</span></span>

   ```markdown
   <xref:UID>
   <xref:UID?displayProperty=nameWithType>
   ```

   <span data-ttu-id="5ebb7-173">Par défaut, le texte du lien montre seulement le nom du membre ou du type.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-173">By default, link text shows only the member or type name.</span></span> <span data-ttu-id="5ebb7-174">Le paramètre de requête `displayProperty=nameWithType` facultatif produit un texte de lien complet, à savoir **namespace.type** pour les types et **type.member** pour les membres de type, notamment les membres de type énumération.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-174">The optional `displayProperty=nameWithType` query parameter produces fully qualified link text, that is, **namespace.type** for types, and **type.member** for type members, including enumeration type members.</span></span>

- <span data-ttu-id="5ebb7-175">Liens de style Markdown :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-175">Markdown-style links:</span></span>

   ```markdown
   [link text](xref:UID)
   ```

   <span data-ttu-id="5ebb7-176">Utilisez des liens de style Markdown pour XRef quand vous souhaitez personnaliser le texte du lien affiché.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-176">Use Markdown-style links for XRef when you want to customize the link text that's displayed.</span></span>

<span data-ttu-id="5ebb7-177">Exemples :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-177">Examples:</span></span>

- <span data-ttu-id="5ebb7-178">**\<xref:System.String>** apparaît sous la forme <xref:System.String>.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-178">**\<xref:System.String>** displays as <xref:System.String></span></span>

- <span data-ttu-id="5ebb7-179">**\<xref:System.String?displayProperty=nameWithType>** apparaît sous la forme <xref:System.String?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-179">**\<xref:System.String?displayProperty=nameWithType>** displays as <xref:System.String?displayProperty=nameWithType></span></span>

- <span data-ttu-id="5ebb7-180">**\[String class](xref:System.String)** apparaît sous la forme [String class](xref:System.String).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-180">**\[String class](xref:System.String)** displays as [String class](xref:System.String).</span></span>

<span data-ttu-id="5ebb7-181">Le paramètre de requête `displayProperty=fullName` fonctionne de la même façon que `displayProperty=nameWithType` pour les classes.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-181">The `displayProperty=fullName` query parameter works the same way as `displayProperty=nameWithType` for classes.</span></span> <span data-ttu-id="5ebb7-182">Autrement dit, le texte du lien devient **namespace.classname**.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-182">That is, the link text becomes **namespace.classname**.</span></span> <span data-ttu-id="5ebb7-183">Toutefois, pour les membres, le texte du lien apparaît sous la forme **namespace.classname.membername**, ce qui peut être indésirable.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-183">However, for members, the link text displays as **namespace.classname.membername**, which may be undesirable.</span></span>

> [!NOTE]
> <span data-ttu-id="5ebb7-184">Les UID respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-184">UIDs are case sensitive.</span></span> <span data-ttu-id="5ebb7-185">Par exemple, `<xref:System.Object>` est résolu correctement, mais pas `<xref:system.object>`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-185">For example, `<xref:System.Object>` resolves correctly but `<xref:system.object>` does not.</span></span>

### <a name="xref-build-warnings-and-incremental-builds"></a><span data-ttu-id="5ebb7-186">Avertissements de build XRef et builds incrémentielles</span><span class="sxs-lookup"><span data-stu-id="5ebb7-186">XRef build warnings and incremental builds</span></span>

<span data-ttu-id="5ebb7-187">Une build incrémentielle génère uniquement les fichiers qui ont changé ou ceux qui ont été affectés par un changement.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-187">An incremental build only builds files that have changed or been affected by a change.</span></span> <span data-ttu-id="5ebb7-188">Si vous recevez un avertissement de build à propos d’un lien XREF non valide alors que le lien est valide, cela peut être dû au fait que la build est incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-188">If you see a build warning about an invalid XREF link, but the link is actually valid, this could be because the build was incremental.</span></span> <span data-ttu-id="5ebb7-189">Le fichier à l’origine de l’avertissement n’a pas changé. Il n’a donc pas été généré et des avertissements antérieurs ont été relus.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-189">The file causing the warning didn't change, so it wasn't built and past warnings were replayed.</span></span> <span data-ttu-id="5ebb7-190">L’avertissement disparaît quand le fichier change ou si vous déclenchez une build complète (vous pouvez démarrer une build complète sur ops.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-190">The warning will disappear when the file changes or if you trigger a full build (you can start a full build on ops.microsoft.com).</span></span> <span data-ttu-id="5ebb7-191">C’est un inconvénient pour les builds incrémentielles, car DocFX ne peut pas détecter de mise à jour de données à l’intérieur du service XREF.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-191">This is a drawback to incremental builds, because DocFX can't detect a data update inside the XREF service.</span></span>

### <a name="determine-the-uid"></a><span data-ttu-id="5ebb7-192">Déterminer l’UID</span><span class="sxs-lookup"><span data-stu-id="5ebb7-192">Determine the UID</span></span>

<span data-ttu-id="5ebb7-193">L’UID est généralement le nom complet de la classe ou du membre.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-193">The UID is usually the fully qualified class or member name.</span></span> <span data-ttu-id="5ebb7-194">Il existe au moins deux façons de déterminer l’UID :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-194">There are at least two ways to determine the UID:</span></span>

- <span data-ttu-id="5ebb7-195">Cliquez avec le bouton droit sur la page [Docs][docs] pour un type ou un membre, sélectionnez **Afficher la source**, puis copiez la valeur **content** pour **ms.assetid** :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-195">Right-click on the [Docs][docs] page for a type or member, select **View source**, and then copy the **content** value for **ms.assetid**:</span></span>

  ![ms.assetid dans la source de la page web](media/how-to-write-links/ms-assetid.png)

- <span data-ttu-id="5ebb7-197">Utilisez le [site autocomplete][] en ajoutant une partie ou la totalité du nom du type à l’URL.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-197">Use the [autocomplete site][] by appending some or all of the name of the type to the URL.</span></span> <span data-ttu-id="5ebb7-198">Par exemple, si vous entrez `https://xref.docs.microsoft.com/autocomplete?text=Writeline` dans la barre d’adresses de votre navigateur, vous pouvez voir l’ensemble des types et des méthodes contenant **WriteLine** dans leur nom ainsi que leur UID.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-198">For example, entering `https://xref.docs.microsoft.com/autocomplete?text=Writeline` in the address bar of your browser displays all the types and methods that contain **Writeline** in their name, along with their UID.</span></span>

#### <a name="verify-the-uid"></a><span data-ttu-id="5ebb7-199">Vérifier l’UID</span><span class="sxs-lookup"><span data-stu-id="5ebb7-199">Verify the UID</span></span>

<span data-ttu-id="5ebb7-200">Pour vérifier si votre UID est correct, remplacez **System.String** dans l’URL suivante par votre UID, puis collez-la dans la barre d’adresses d’un navigateur :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-200">To test if you have the correct UID, replace **System.String** in the following URL with your UID, and then paste it into the address bar of a browser:</span></span>

`https://xref.docs.microsoft.com/query?uid=System.String`

> [!TIP]
> <span data-ttu-id="5ebb7-201">L’UID dans l’URL respecte la casse. Si vous vérifiez une UID de surcharge de méthode, n’incluez pas d’espace entre les types de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-201">The UID in the URL is case-sensitive, and if you're checking a method overload UID, don't include spaces between the parameter types.</span></span>

<span data-ttu-id="5ebb7-202">Si vous obtenez un message semblable au suivant, votre UID est correct :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-202">If you see something like the following, you have the correct UID:</span></span>

```text
[{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,...xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"},{"uid":"System.String","name":"String","fullName":"System.String","href":"https://docs.microsoft.com/dotnet/api/system.string","tags":",/dotnet,netframework-4.5.1,netframework-4.5.2,netframework-4.5,netframework-4.6,netframework-4.6.1,...,xamarinmac-3.0,public,","vendor":null,"hash":null,"commentId":"T:System.String","nameWithType":"System.String"}]
```

<span data-ttu-id="5ebb7-203">Si la page affiche uniquement `[]`, votre UID est incorrect.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-203">If you just see `[]` displayed on the page, you have the wrong UID.</span></span>

### <a name="percent-encoding-of-urls"></a><span data-ttu-id="5ebb7-204">Encodage en pourcent des URL</span><span class="sxs-lookup"><span data-stu-id="5ebb7-204">Percent-encoding of URLs</span></span>

<span data-ttu-id="5ebb7-205">Les caractères spéciaux de l’UID doivent être encodés au format HTML comme ceci :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-205">Special characters in the UID need to be HTML encoded as follows:</span></span>

| <span data-ttu-id="5ebb7-206">Caractère</span><span class="sxs-lookup"><span data-stu-id="5ebb7-206">Character</span></span> | <span data-ttu-id="5ebb7-207">Encodage HTML</span><span class="sxs-lookup"><span data-stu-id="5ebb7-207">HTML encoding</span></span> |
| --------- | ------------- |
| `` ` ``   | <span data-ttu-id="5ebb7-208">%60</span><span class="sxs-lookup"><span data-stu-id="5ebb7-208">%60</span></span>           |
| `#`       | <span data-ttu-id="5ebb7-209">%23</span><span class="sxs-lookup"><span data-stu-id="5ebb7-209">%23</span></span>           |
| `*`       | <span data-ttu-id="5ebb7-210">%2A</span><span class="sxs-lookup"><span data-stu-id="5ebb7-210">%2A</span></span>           |

<span data-ttu-id="5ebb7-211">Consultez la liste complète des [encodages en pourcent](https://en.wikipedia.org/wiki/Percent-encoding).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-211">See a full list of [percent-codes](https://en.wikipedia.org/wiki/Percent-encoding).</span></span>

<span data-ttu-id="5ebb7-212">Exemples d’encodage :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-212">Encoding examples:</span></span>

- <span data-ttu-id="5ebb7-213">`System.Threading.Tasks.Task``1` est encodé sous la forme `System.Threading.Tasks.Task%601` (consultez la [section sur les types génériques](#generic-types)).</span><span class="sxs-lookup"><span data-stu-id="5ebb7-213">`System.Threading.Tasks.Task``1` encodes as `System.Threading.Tasks.Task%601` (see the [section on generic types](#generic-types))</span></span>

- <span data-ttu-id="5ebb7-214">`System.Exception.#ctor` est encodé sous la forme `System.Exception.%23ctor`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-214">`System.Exception.#ctor` encodes as `System.Exception.%23ctor`</span></span>

- <span data-ttu-id="5ebb7-215">`System.Object.Equals*` est encodé sous la forme `System.Object.Equals%2A`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-215">`System.Object.Equals*` encodes as `System.Object.Equals%2A`</span></span>

### <a name="generic-types"></a><span data-ttu-id="5ebb7-216">Types génériques</span><span class="sxs-lookup"><span data-stu-id="5ebb7-216">Generic types</span></span>

<span data-ttu-id="5ebb7-217">Les types génériques sont des types tels que `System.Collections.Generic.List<T>`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-217">Generic types are those types such as `System.Collections.Generic.List<T>`.</span></span> <span data-ttu-id="5ebb7-218">Si vous accédez à ce type dans le [navigateur d’API .NET](https://docs.microsoft.com/dotnet/api/) et que vous examinez son URL, vous pouvez voir que `<T>` est écrit `-1` dans l’URL, ce qui représente en fait **\`1** :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-218">If you browse to this type in the [.NET API browser](https://docs.microsoft.com/dotnet/api/) and look at its URL, you see that `<T>` is written as `-1` in the URL, which actually represents **\`1**:</span></span>

`https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1`

<span data-ttu-id="5ebb7-219">Pour établir un lien vers un type générique tel que **List\<T>** , encodez le caractère d’accent grave ( **\`** ) sous la forme **%60**, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-219">To link to a generic type such as **List\<T>**, encode the **\`** backtick character as **%60**, as shown in the following example:</span></span>

```markdown
<xref:System.Collections.Generic.List%601>
```

### <a name="methods"></a><span data-ttu-id="5ebb7-220">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5ebb7-220">Methods</span></span>

<span data-ttu-id="5ebb7-221">Pour établir un lien vers une méthode, vous pouvez soit créer un lien vers la page de la méthode générale en ajoutant un astérisque (`*`) après le nom de la méthode, soit créer un lien vers une surcharge spécifique.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-221">To link to a method, you can either link to the general method page by adding an asterisk (`*`) after the method name, or to a specific overload.</span></span> <span data-ttu-id="5ebb7-222">Par exemple, utilisez la page générale quand vous souhaitez établir un lien vers la méthode `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` sans types de paramètres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-222">For example, use the general page when you want to link to the `<xref:System.Object.Equals%2A?displayProperty=nameWithType>` method without specific parameter types.</span></span> <span data-ttu-id="5ebb7-223">Le caractère astérisque est encodé sous la forme `%2A`.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-223">The asterisk character is encoded as `%2A`.</span></span> <span data-ttu-id="5ebb7-224">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-224">For example:</span></span>

<span data-ttu-id="5ebb7-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` crée un lien vers <xref:System.Object.Equals%2A?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="5ebb7-225">`<xref:System.Object.Equals%2a?displayProperty=nameWithType>` links to <xref:System.Object.Equals%2A?displayProperty=nameWithType></span></span>

<span data-ttu-id="5ebb7-226">Pour établir un lien vers une surcharge spécifique, ajoutez des parenthèses après le nom de la méthode et placez dans celles-ci le nom de type complet de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-226">To link to a specific overload, add parenthesis after the method name and include the full type name of each parameter.</span></span> <span data-ttu-id="5ebb7-227">N’insérez aucun espace entre les noms de types ; sinon, le lien ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-227">Do not put a space character between the type names or the link won't work.</span></span> <span data-ttu-id="5ebb7-228">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-228">For example:</span></span>

<span data-ttu-id="5ebb7-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` crée un lien vers <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="5ebb7-229">`<xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType>` links to <xref:System.Object.Equals(System.Object,System.Object)?displayProperty=nameWithType></span></span>

## <a name="links-from-includes"></a><span data-ttu-id="5ebb7-230">Liens des includes</span><span class="sxs-lookup"><span data-stu-id="5ebb7-230">Links from includes</span></span>

<span data-ttu-id="5ebb7-231">Les fichiers include étant situés dans un autre répertoire, vous devez utiliser des chemins d'accès relatifs plus longs.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-231">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="5ebb7-232">Pour faire un lien vers un article à partir d'un fichier include, utilisez ce format :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-232">To link to an article from an include file, use this format:</span></span>

```markdown
[link text](../articles/folder/article-name.md)
```

> [!TIP]
> <span data-ttu-id="5ebb7-233">L’extension [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) pour Visual Studio Code peut vous aider à insérer correctement des signets et des liens relatifs sans avoir à deviner les chemins.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-233">The [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) extension for Visual Studio Code helps you insert relative links and bookmarks correctly without the tedium of figuring out paths.</span></span>

## <a name="links-in-selectors"></a><span data-ttu-id="5ebb7-234">Liens dans les sélecteurs</span><span class="sxs-lookup"><span data-stu-id="5ebb7-234">Links in selectors</span></span>

<span data-ttu-id="5ebb7-235">Un sélecteur est un composant de navigation qui apparaît dans un article de documentation sous forme de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-235">A selector is a navigation component that appears in a docs article as a drop-down list.</span></span> <span data-ttu-id="5ebb7-236">Quand un lecteur sélectionne une valeur dans la liste déroulante, le navigateur ouvre l’article sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-236">When a reader selects a value in the drop-down, the browser opens the selected article.</span></span> <span data-ttu-id="5ebb7-237">En général, la liste du sélecteur contient des liens vers des articles qui ont un rapport étroit avec celui-ci, par exemple traitant du même sujet dans différents langages de programmation, ou vers une série d’articles connexe.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-237">Typically the selector list contains links to closely related articles, for example the same subject matter in multiple programming languages or a closely related series of articles.</span></span>

<span data-ttu-id="5ebb7-238">Si vous avez des sélecteurs intégrés dans un include, utilisez la structure de liens suivante :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-238">If you have selectors that are embedded in an include, use the following link structure:</span></span>

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md)
   ```

## <a name="reference-style-links"></a><span data-ttu-id="5ebb7-239">Liens de type référence</span><span class="sxs-lookup"><span data-stu-id="5ebb7-239">Reference-style links</span></span>

<span data-ttu-id="5ebb7-240">Vous pouvez utiliser des liens de type référence pour rendre votre contenu source plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-240">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="5ebb7-241">Les liens de type référence remplacent la syntaxe de lien inline par une syntaxe simplifiée vous permettant de déplacer les URL longues à la fin de l’article.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-241">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="5ebb7-242">Voici l'exemple de [Daring Fireball](https://daringfireball.net/projects/markdown/) :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-242">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="5ebb7-243">Texte intégré :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-243">Inline text:</span></span>

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

<span data-ttu-id="5ebb7-244">Liens de référence à la fin de l'article :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-244">Link references at the end of the article:</span></span>

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```

<span data-ttu-id="5ebb7-245">Veillez à inclure l’espace après le signe deux-points, avant le lien.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-245">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="5ebb7-246">Lorsque vous liez d'autres articles techniques, si vous oubliez d'inclure l'espace, le lien sera rompu dans l’article publié.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-246">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="5ebb7-247">Liens vers des pages qui ne font pas partie de l’ensemble de documentation technique</span><span class="sxs-lookup"><span data-stu-id="5ebb7-247">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="5ebb7-248">Pour établir un lien vers une page sur une autre propriété de Microsoft (par exemple la page de tarifs, la page du contrat SLA ou toute autre page qui n’est pas un article de documentation), utilisez une URL absolue, mais omettez les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-248">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="5ebb7-249">Le but ici est que les liens fonctionnent dans GitHub et sur le site rendu :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-249">The goal here is that links work in GitHub and on the rendered site:</span></span>

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```

## <a name="links-to-third-party-sites"></a><span data-ttu-id="5ebb7-250">Liens vers des sites tiers</span><span class="sxs-lookup"><span data-stu-id="5ebb7-250">Links to third-party sites</span></span>

<span data-ttu-id="5ebb7-251">Une expérience utilisateur idéale minimise l'envoi d'utilisateurs vers d'autres sites.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-251">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="5ebb7-252">Basez donc les liens vers des sites tiers, dont nous avons parfois besoin, sur ces informations :</span><span class="sxs-lookup"><span data-stu-id="5ebb7-252">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="5ebb7-253">**Responsabilité** : Établissez un lien vers du contenu tiers quand il s’agit des informations que le tiers est tenu de partager.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-253">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="5ebb7-254">Par exemple, il ne revient pas à Microsoft d’expliquer aux utilisateurs comment utiliser les outils pour développeurs d’Android. Cette tâche incombe à Google.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-254">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="5ebb7-255">Si besoin, nous pouvons expliquer comment utiliser les outils Android *avec* Azure, mais l'explication de l'utilisation des outils eux-mêmes est le travail de Google.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-255">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="5ebb7-256">**Validation des PM** : Demandez à Microsoft de valider le contenu tiers.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-256">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="5ebb7-257">En établissant un lien, nous donnons des indications de notre confiance et de nos obligations si les utilisateurs suivent les instructions.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-257">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="5ebb7-258">**Révisions d’actualisation** : Vérifiez que les informations tierces sont toujours actuelles, correctes et pertinentes, et que le lien n’a pas changé.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-258">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn't changed.</span></span>
- <span data-ttu-id="5ebb7-259">**Hors site** : Informez les utilisateurs qu’ils vont vers un autre site.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-259">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="5ebb7-260">Si le contexte ne l’indique pas explicitement, ajoutez une phrase pour cela,</span><span class="sxs-lookup"><span data-stu-id="5ebb7-260">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="5ebb7-261">Par exemple : « Les prérequis comprennent les outils pour développeurs d’Android, que vous pouvez télécharger sur le site d’Android Studio ».</span><span class="sxs-lookup"><span data-stu-id="5ebb7-261">For example: "Prerequisites include the Android Developer Tools, which you can download on the Android Studio site."</span></span>
- <span data-ttu-id="5ebb7-262">**Étapes suivantes** : Vous pouvez ajouter un lien vers, par exemple, un blog MVP dans une section « Étapes suivantes ».</span><span class="sxs-lookup"><span data-stu-id="5ebb7-262">**Next steps**: It's fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="5ebb7-263">Encore une fois, vérifiez que les utilisateurs comprennent qu’ils vont quitter le site.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-263">Again, just make sure that users understand they'll be leaving the site.</span></span>
- <span data-ttu-id="5ebb7-264">**Juridique** : Nous sommes légalement couverts sous **Liens vers des sites tiers** dans les **Conditions d’utilisation** en pied de page de chaque page microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="5ebb7-264">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every microsoft.com page.</span></span>

<!-- link references -->
[CommonMark]: https://commonmark.org/
[Markdig]: https://github.com/lunet-io/markdig
[GFM]: https://help.github.com/categories/writing-on-github/
[docs]: https://docs.microsoft.com
[Navigateur d’API .NET]: https://docs.microsoft.com/dotnet/api/
[.NET API browser]: https://docs.microsoft.com/dotnet/api/
[Windows UWP]: https://docs.microsoft.com/uwp/api
[docsextension]: https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown
[Site autocomplete]: https://xref.docs.microsoft.com/autocomplete?text=
[autocomplete site]: https://xref.docs.microsoft.com/autocomplete?text=
