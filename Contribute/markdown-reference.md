---
title: Informations de référence sur Markdown pour docs.microsoft.com
description: Guide de la plateforme Docs sur Markdown.
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 1023f3036e5c1facd0bcd4c31069e6faf3c95483
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245869"
---
# <a name="markdown-reference"></a><span data-ttu-id="40413-103">Informations de référence sur Markdown</span><span class="sxs-lookup"><span data-stu-id="40413-103">Markdown Reference</span></span>

<span data-ttu-id="40413-104">Markdown est un langage de balisage léger avec une syntaxe de mise en forme en texte brut.</span><span class="sxs-lookup"><span data-stu-id="40413-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="40413-105">La plateforme Docs prend en charge la norme CommonMark pour Markdown, ainsi que certaines extensions Markdown personnalisées conçues pour fournir du contenu enrichi sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="40413-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="40413-106">Cet article fournit des informations de référence par ordre alphabétique, qui facilitent l’utilisation de Markdown pour docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="40413-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="40413-107">Vous pouvez utiliser n’importe quel éditeur de texte pour créer du contenu Markdown.</span><span class="sxs-lookup"><span data-stu-id="40413-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="40413-108">Comme éditeur facilitant l’insertion à la fois d’une syntaxe Markdown standard et d’extensions Docs personnalisées, nous recommandons [VS Code](https://code.visualstudio.com/) avec le [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installé.</span><span class="sxs-lookup"><span data-stu-id="40413-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="40413-109">Docs utilise le moteur Markdown Markdig.</span><span class="sxs-lookup"><span data-stu-id="40413-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="40413-110">Vous pouvez tester le rendu de Markdown dans Markdig par rapport à d’autre moteurs sur [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="40413-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="40413-111">Alertes (Remarque, Conseil, Important, Attention, Avertissement)</span><span class="sxs-lookup"><span data-stu-id="40413-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="40413-112">Les alertes sont une extension Markdown Docs pour créer des citations qui s’affichent sur docs.microsoft.com avec des couleurs et des icônes indiquant la signification du contenu.</span><span class="sxs-lookup"><span data-stu-id="40413-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="40413-113">Les types d’alerte suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="40413-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="40413-114">Ces alertes ressemblent à ceci sur docs.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="40413-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="40413-115">Informations que l’utilisateur doit remarquer même s’il parcourt le contenu rapidement.</span><span class="sxs-lookup"><span data-stu-id="40413-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="40413-116">Informations facultatives qui aident l’utilisateur à être plus performant.</span><span class="sxs-lookup"><span data-stu-id="40413-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40413-117">Informations essentielles nécessaires à la réussite de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="40413-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="40413-118">Conséquences éventuellement négatives d’une action.</span><span class="sxs-lookup"><span data-stu-id="40413-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="40413-119">Certaines conséquences dangereuses d’une action.</span><span class="sxs-lookup"><span data-stu-id="40413-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="40413-120">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="40413-120">Code snippets</span></span>

<span data-ttu-id="40413-121">Vous pouvez incorporer des extraits de code dans vos fichiers Markdown :</span><span class="sxs-lookup"><span data-stu-id="40413-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="40413-122">En-têtes</span><span class="sxs-lookup"><span data-stu-id="40413-122">Headings</span></span>

<span data-ttu-id="40413-123">Docs prend en charge six niveaux de titres Markdown :</span><span class="sxs-lookup"><span data-stu-id="40413-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="40413-124">Il doit y avoir un espace entre le signe `#` et le texte du titre.</span><span class="sxs-lookup"><span data-stu-id="40413-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="40413-125">Chaque fichier Markdown doit avoir un, et un seul, titre H1.</span><span class="sxs-lookup"><span data-stu-id="40413-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="40413-126">Le titre H1 doit être le premier contenu du fichier après le bloc de métadonnées YML.</span><span class="sxs-lookup"><span data-stu-id="40413-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="40413-127">Les titres H2 apparaissent automatiquement dans le menu de navigation de droite du fichier publié.</span><span class="sxs-lookup"><span data-stu-id="40413-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="40413-128">Ce n’est pas le cas des titres de niveau inférieur, donc privilégiez l’utilisation de titres H2 pour aider les lecteurs à parcourir votre contenu.</span><span class="sxs-lookup"><span data-stu-id="40413-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="40413-129">Les titres HMTL, comme `<h1>`, ne sont pas recommandés. En effet, dans certains cas, ils entraînent l’affichage d’avertissements de génération.</span><span class="sxs-lookup"><span data-stu-id="40413-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="40413-130">Vous pouvez créer un lien vers des titres spécifiques dans un fichier par le biais de [signets](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="40413-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="40413-131">HTML</span><span class="sxs-lookup"><span data-stu-id="40413-131">HTML</span></span>

<span data-ttu-id="40413-132">Bien que Markdown prenne en charge la syntaxe HTML inline, HTML n’est pas recommandé pour une publication sur Docs, car, sauf pour un ensemble limité de valeurs, il entraîne des avertissements ou des erreurs de génération.</span><span class="sxs-lookup"><span data-stu-id="40413-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="40413-133">Images</span><span class="sxs-lookup"><span data-stu-id="40413-133">Images</span></span>

<span data-ttu-id="40413-134">La syntaxe pour inclure une image est :</span><span class="sxs-lookup"><span data-stu-id="40413-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="40413-135">Où `alt text` est une brève description de l’image et `<folder path>` un chemin relatif de l’image.</span><span class="sxs-lookup"><span data-stu-id="40413-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="40413-136">Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants.</span><span class="sxs-lookup"><span data-stu-id="40413-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="40413-137">Ce texte est également utile si le site contient un bogue qui empêche l’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="40413-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="40413-138">Les images doivent être stockées dans un dossier `/media` au sein de votre documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="40413-139">Les types de fichiers suivants sont pris en charge par défaut pour les images :</span><span class="sxs-lookup"><span data-stu-id="40413-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="40413-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="40413-140">.jpg</span></span>
- <span data-ttu-id="40413-141">.png</span><span class="sxs-lookup"><span data-stu-id="40413-141">.png</span></span>

<span data-ttu-id="40413-142">Vous pouvez ajouter la prise en charge d’autres types d’image en les ajoutant en tant que ressources au fichier docfx.json <!--add link to reference when available--> de votre documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="40413-143">Liens</span><span class="sxs-lookup"><span data-stu-id="40413-143">Links</span></span>

<span data-ttu-id="40413-144">Dans la plupart des cas, Docs utilise des liens Markdown standard vers d’autres fichiers et pages.</span><span class="sxs-lookup"><span data-stu-id="40413-144">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="40413-145">Les types de liens sont décrits dans des sous-sections plus loin.</span><span class="sxs-lookup"><span data-stu-id="40413-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="40413-146">Le Docs Authoring Pack pour VS Code peut aider à insérer correctement des signets et des liens relatifs sans avoir à deviner les chemins !</span><span class="sxs-lookup"><span data-stu-id="40413-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40413-147">N’incluez pas de codes de paramètres régionaux, comme en-us, dans vos liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="40413-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="40413-148">Les codes de paramètres régionaux codés en dur empêchent l’affichage du contenu traduit, ce qui procure une mauvaise expérience aux utilisateurs dans d’autres paramètres régionaux et engendre des coûts de traduction significatifs.</span><span class="sxs-lookup"><span data-stu-id="40413-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="40413-149">Quand vous copiez une URL à partir d’un navigateur, le code de paramètres régionaux est inclus par défaut ; vous devez le supprimer manuellement quand vous créez votre lien.</span><span class="sxs-lookup"><span data-stu-id="40413-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="40413-150">Par exemple, utilisez :</span><span class="sxs-lookup"><span data-stu-id="40413-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="40413-151">Pas :</span><span class="sxs-lookup"><span data-stu-id="40413-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="40413-152">Liens relatifs vers des fichiers de la même documentation</span><span class="sxs-lookup"><span data-stu-id="40413-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="40413-153">Un chemin relatif est le chemin du fichier cible par rapport au fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="40413-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="40413-154">Dans Docs, vous pouvez utiliser un chemin relatif pour créer un lien vers un autre fichier de la même documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-154">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="40413-155">La syntaxe d’un chemin relatif est la suivante :</span><span class="sxs-lookup"><span data-stu-id="40413-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="40413-156">Où `../` indique un niveau au-dessus dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="40413-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="40413-157">Le chemin relatif est résolu pendant la génération, qui inclut la suppression de l’extension .md.</span><span class="sxs-lookup"><span data-stu-id="40413-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="40413-158">Vous pouvez utiliser « ../ » pour créer un lien vers le fichier dans le dossier parent, mais ce fichier doit se trouver dans la même documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="40413-159">Vous ne pouvez pas utiliser « ../ » pour créer un lien vers un fichier d’une autre documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="40413-160">Docs prend également en charge une forme spéciale de chemin relatif qui commence par « ~ » (par exemple, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="40413-160">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="40413-161">Cette syntaxe indique un fichier par rapport au dossier racine d’une documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="40413-162">Ce genre de chemin est aussi validé et résolu pendant la génération.</span><span class="sxs-lookup"><span data-stu-id="40413-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40413-163">Ajoutez l’extension de fichier dans le chemin relatif.</span><span class="sxs-lookup"><span data-stu-id="40413-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="40413-164">La génération valide l’existence du fichier cible de ce chemin relatif.</span><span class="sxs-lookup"><span data-stu-id="40413-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="40413-165">Si le chemin relatif n’inclut pas d’extension de fichier, il est probable qu’un avertissement de lien rompu apparaisse lors de la génération.</span><span class="sxs-lookup"><span data-stu-id="40413-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="40413-166">Par exemple, utilisez :</span><span class="sxs-lookup"><span data-stu-id="40413-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="40413-167">Pas :</span><span class="sxs-lookup"><span data-stu-id="40413-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="40413-168">Liens relatifs de site vers d’autres fichiers sur Docs</span><span class="sxs-lookup"><span data-stu-id="40413-168">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="40413-169">N’incluez pas l’extension de fichier (.md).</span><span class="sxs-lookup"><span data-stu-id="40413-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="40413-170">Ce lien dirige vers le fichier Linux « overview » depuis l’extérieur de la documentation Azure « articles ».</span><span class="sxs-lookup"><span data-stu-id="40413-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="40413-171">Liens vers des sites externes</span><span class="sxs-lookup"><span data-stu-id="40413-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="40413-172">Lien basé sur une URL vers une autre page web (doit inclure https://).</span><span class="sxs-lookup"><span data-stu-id="40413-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="40413-173">Liens de signet</span><span class="sxs-lookup"><span data-stu-id="40413-173">Bookmark links</span></span>

<span data-ttu-id="40413-174">Lien de signet vers un titre d’un autre fichier du même dépôt :</span><span class="sxs-lookup"><span data-stu-id="40413-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="40413-175">Lien de signet vers un titre du fichier actuel :</span><span class="sxs-lookup"><span data-stu-id="40413-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="40413-176">Utilisez un signe dièse suivi des mots du titre sans signe de ponctuation et en remplaçant les espaces par des tirets.</span><span class="sxs-lookup"><span data-stu-id="40413-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="40413-177">Liens d’ancrage explicites</span><span class="sxs-lookup"><span data-stu-id="40413-177">Explicit anchor links</span></span>

<span data-ttu-id="40413-178">Les liens d’ancrage explicites utilisant la balise HTML `<a>` **ne sont pas obligatoires ou recommandés** sauf dans les pages d’arrivée et hub.</span><span class="sxs-lookup"><span data-stu-id="40413-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="40413-179">Utilisez des signets comme indiqué plus haut dans les fichiers Markdown généraux.</span><span class="sxs-lookup"><span data-stu-id="40413-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="40413-180">Pour les pages hub et d’arrivée, utilisez des ancrages comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="40413-181">`## <a id="AnchorText"> </a>Header text` ou `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="40413-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="40413-182">Pour créer un lien vers des ancrages explicites, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="40413-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="40413-183">Liens XREF (référence croisée)</span><span class="sxs-lookup"><span data-stu-id="40413-183">XREF (cross reference) links</span></span>

<span data-ttu-id="40413-184">Pour créer un lien vers des pages de références d’API générées automatiquement dans la documentation actuelle ou dans d’autres documentations, utilisez des liens XREF avec l’ID unique (UID).</span><span class="sxs-lookup"><span data-stu-id="40413-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="40413-185">Pour référencer des pages de références d’API dans d’autres jeux de documentation, vous devez ajouter la configuration `xrefService` dans le fichier `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="40413-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="40413-186">L’UID équivaut au nom complet de la classe et du membre.</span><span class="sxs-lookup"><span data-stu-id="40413-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="40413-187">Si vous ajoutez un \* après l’UID, le lien représente alors la page de la surcharge et non pas une API spécifique.</span><span class="sxs-lookup"><span data-stu-id="40413-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="40413-188">Par exemple, utilisez `List<T>.BinarySearch*` pour créer un lien vers la page Méthode BinarySearch au lieu de créer un lien vers une surcharge spécifique telle que `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="40413-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="40413-189">Vous pouvez utiliser une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40413-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="40413-190">Lien automatique : `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="40413-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="40413-191">Le paramètre de requête `displayProperty` facultatif produit un texte de lien complet.</span><span class="sxs-lookup"><span data-stu-id="40413-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="40413-192">Par défaut, le texte du lien montre seulement le nom du membre ou du type.</span><span class="sxs-lookup"><span data-stu-id="40413-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="40413-193">Lien Markdown : `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="40413-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="40413-194">À utiliser quand vous voulez personnaliser le texte du lien affiché.</span><span class="sxs-lookup"><span data-stu-id="40413-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="40413-195">Exemples :</span><span class="sxs-lookup"><span data-stu-id="40413-195">Examples:</span></span>

- <span data-ttu-id="40413-196">`<xref:System.String>` s’affiche sous la forme « String ».</span><span class="sxs-lookup"><span data-stu-id="40413-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="40413-197">`<xref:System.String?displayProperty=nameWithType>` s’affiche sous la forme « System.String ».</span><span class="sxs-lookup"><span data-stu-id="40413-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="40413-198">`[String class](xref:System.String)` s’affiche sous la forme « String class ».</span><span class="sxs-lookup"><span data-stu-id="40413-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="40413-199">Il n’existe actuellement aucun moyen facile de trouver les UID.</span><span class="sxs-lookup"><span data-stu-id="40413-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="40413-200"><!-- ? -->La meilleure façon de trouver l’UID pour une API consiste à afficher le source de la page de l’API vers laquelle vous voulez créer un lien et à rechercher la valeur de ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="40413-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="40413-201">Les valeurs des surcharges individuelles ne figurent pas dans la source.</span><span class="sxs-lookup"><span data-stu-id="40413-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="40413-202">Nous nous efforçons de mettre au point un meilleur système dans le futur.</span><span class="sxs-lookup"><span data-stu-id="40413-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="40413-203">Quand l’UID contient les caractères spéciaux \`, \# ou \*, la valeur de l’UID doit être encodée en HTML en tant que `%60`, `%23` et `%2A`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="40413-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="40413-204">Vous pouvez parfois trouver des parenthèses dans l’encodage, mais elles ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="40413-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="40413-205">Exemples :</span><span class="sxs-lookup"><span data-stu-id="40413-205">Examples:</span></span>

- <span data-ttu-id="40413-206">System.Threading.Tasks.Task\`1 devient `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="40413-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="40413-207">System.Exception.\#ctor devient `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="40413-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="40413-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) devient `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="40413-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="40413-209">Listes (numérotées, à puces, liste de contrôle)</span><span class="sxs-lookup"><span data-stu-id="40413-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="40413-210">Liste numérotée</span><span class="sxs-lookup"><span data-stu-id="40413-210">Numbered list</span></span>

<span data-ttu-id="40413-211">Pour créer une liste numérotée, vous pouvez utiliser exclusivement des « 1 », qui sont restitués sous la forme d’une liste séquentielle au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="40413-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="40413-212">Pour accroître la lisibilité du texte source, vous pouvez incrémenter vos listes.</span><span class="sxs-lookup"><span data-stu-id="40413-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="40413-213">N’utilisez pas de lettres dans les listes, y compris dans les listes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="40413-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="40413-214">Elles ne sont pas restituées correctement au moment de la publication sur Docs. Les listes imbriquées utilisant des nombres sont restituées avec des lettres minuscules au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="40413-214">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="40413-215">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40413-215">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="40413-216">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-216">This renders as follows:</span></span>

1. <span data-ttu-id="40413-217">This is</span><span class="sxs-lookup"><span data-stu-id="40413-217">This is</span></span>
1. <span data-ttu-id="40413-218">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="40413-218">a parent numbered list</span></span>
   1. <span data-ttu-id="40413-219">and this is</span><span class="sxs-lookup"><span data-stu-id="40413-219">and this is</span></span>
   1. <span data-ttu-id="40413-220">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="40413-220">a nested numbered list</span></span>
1. <span data-ttu-id="40413-221">(fin)</span><span class="sxs-lookup"><span data-stu-id="40413-221">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="40413-222">Liste à puces</span><span class="sxs-lookup"><span data-stu-id="40413-222">Bulleted list</span></span>

<span data-ttu-id="40413-223">Pour créer une liste à puces, utilisez `-` suivi d’un espace au début de chaque ligne :</span><span class="sxs-lookup"><span data-stu-id="40413-223">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="40413-224">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-224">This renders as follows:</span></span>

- <span data-ttu-id="40413-225">This is</span><span class="sxs-lookup"><span data-stu-id="40413-225">This is</span></span>
- <span data-ttu-id="40413-226">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="40413-226">a parent bulleted list</span></span>
  - <span data-ttu-id="40413-227">and this is</span><span class="sxs-lookup"><span data-stu-id="40413-227">and this is</span></span>
  - <span data-ttu-id="40413-228">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="40413-228">a nested bulleted list</span></span>
- <span data-ttu-id="40413-229">All done!</span><span class="sxs-lookup"><span data-stu-id="40413-229">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="40413-230">Liste de contrôle</span><span class="sxs-lookup"><span data-stu-id="40413-230">Checklist</span></span>

<span data-ttu-id="40413-231">Les listes de contrôle sont utilisables sur docs.microsoft.com (uniquement) par le biais d’une extension Markdown personnalisée :</span><span class="sxs-lookup"><span data-stu-id="40413-231">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="40413-232">Cet exemple s’affiche sur docs.microsoft.com ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-232">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="40413-233">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="40413-233">List item 1</span></span>
> * <span data-ttu-id="40413-234">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="40413-234">List item 2</span></span>
> * <span data-ttu-id="40413-235">Élément de liste 3</span><span class="sxs-lookup"><span data-stu-id="40413-235">List item 3</span></span>

<span data-ttu-id="40413-236">Utilisez des listes de contrôle au début ou à la fin d’un article pour récapituler le contenu que l’utilisateur va étudier ou a étudié.</span><span class="sxs-lookup"><span data-stu-id="40413-236">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="40413-237">N’ajoutez pas de listes de contrôle aléatoires dans vos articles.</span><span class="sxs-lookup"><span data-stu-id="40413-237">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="40413-238">Action d’étape suivante</span><span class="sxs-lookup"><span data-stu-id="40413-238">Next step action</span></span>

<span data-ttu-id="40413-239">Vous pouvez utiliser une extension personnalisée pour ajouter un bouton d’action d’étape suivante à des pages sur docs.microsoft.com (uniquement).</span><span class="sxs-lookup"><span data-stu-id="40413-239">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="40413-240">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="40413-240">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="40413-241">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="40413-241">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="40413-242">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-242">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="40413-243">Découvrir le style simple</span><span class="sxs-lookup"><span data-stu-id="40413-243">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="40413-244">Vous pouvez utiliser n’importe quel lien pris en charge dans une action d’étape suivante, y compris un lien Markdown vers une autre page web.</span><span class="sxs-lookup"><span data-stu-id="40413-244">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="40413-245">Dans la plupart des cas, le lien d’action suivante est un lien relatif vers un autre fichier de la même documentation.</span><span class="sxs-lookup"><span data-stu-id="40413-245">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="40413-246">Définition de section</span><span class="sxs-lookup"><span data-stu-id="40413-246">Section definition</span></span>

<span data-ttu-id="40413-247"><!-- more info about this would be helpful! --> Vous aurez peut-être à définir une section.</span><span class="sxs-lookup"><span data-stu-id="40413-247"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="40413-248">Cette syntaxe est principalement utilisée pour les tables de code.</span><span class="sxs-lookup"><span data-stu-id="40413-248">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="40413-249">Regardez l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="40413-249">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="40413-250">Le texte Markdown de citation précédent s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-250">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="40413-251">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="40413-251">Selectors</span></span>

<span data-ttu-id="40413-252"><!-- could be more clear! --> Vous pouvez utiliser un sélecteur pour lier plusieurs pages d’un même article.</span><span class="sxs-lookup"><span data-stu-id="40413-252"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="40413-253">Les lecteurs peuvent ainsi passer d’une page à l’autre.</span><span class="sxs-lookup"><span data-stu-id="40413-253">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="40413-254">Cette extension fonctionne différemment sur docs.microsoft.com et sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="40413-254">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="40413-255">Sélecteur unique</span><span class="sxs-lookup"><span data-stu-id="40413-255">Single selector</span></span>

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

<span data-ttu-id="40413-256">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-256">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Windows universel](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="40413-265">Sélecteur multiple</span><span class="sxs-lookup"><span data-stu-id="40413-265">Multi-selector</span></span>

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

<span data-ttu-id="40413-266">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-266">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
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

## <a name="tables"></a><span data-ttu-id="40413-277">les tableaux</span><span class="sxs-lookup"><span data-stu-id="40413-277">Tables</span></span>

<span data-ttu-id="40413-278">Le moyen le plus simple de créer un tableau en Markdown est d’utiliser des barres verticales et des lignes.</span><span class="sxs-lookup"><span data-stu-id="40413-278">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="40413-279">Pour créer un tableau standard avec un en-tête, faites suivre la première ligne d’une ligne en pointillés :</span><span class="sxs-lookup"><span data-stu-id="40413-279">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="40413-280">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-280">This renders as follows:</span></span>

|<span data-ttu-id="40413-281">This is</span><span class="sxs-lookup"><span data-stu-id="40413-281">This is</span></span>   |<span data-ttu-id="40413-282">a simple</span><span class="sxs-lookup"><span data-stu-id="40413-282">a simple</span></span>   |<span data-ttu-id="40413-283">table header</span><span class="sxs-lookup"><span data-stu-id="40413-283">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="40413-284">table</span><span class="sxs-lookup"><span data-stu-id="40413-284">table</span></span>     |<span data-ttu-id="40413-285">data</span><span class="sxs-lookup"><span data-stu-id="40413-285">data</span></span>       |<span data-ttu-id="40413-286">here</span><span class="sxs-lookup"><span data-stu-id="40413-286">here</span></span>        |
|<span data-ttu-id="40413-287">it doesn't</span><span class="sxs-lookup"><span data-stu-id="40413-287">it doesn't</span></span>|<span data-ttu-id="40413-288">actually</span><span class="sxs-lookup"><span data-stu-id="40413-288">actually</span></span>   |<span data-ttu-id="40413-289">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="40413-289">have to line up nicely!</span></span>||

<span data-ttu-id="40413-290">Vous pouvez également créer un tableau sans en-tête.</span><span class="sxs-lookup"><span data-stu-id="40413-290">You can also create a table without a header.</span></span> <span data-ttu-id="40413-291">Par exemple, pour créer une liste à plusieurs colonnes :</span><span class="sxs-lookup"><span data-stu-id="40413-291">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="40413-292">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-292">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="40413-293">This</span><span class="sxs-lookup"><span data-stu-id="40413-293">This</span></span> | <span data-ttu-id="40413-294">table</span><span class="sxs-lookup"><span data-stu-id="40413-294">table</span></span> |
| <span data-ttu-id="40413-295">has no</span><span class="sxs-lookup"><span data-stu-id="40413-295">has no</span></span> | <span data-ttu-id="40413-296">header</span><span class="sxs-lookup"><span data-stu-id="40413-296">header</span></span> |

<span data-ttu-id="40413-297">Vous pouvez aligner les colonnes à l’aide de signes deux-points :</span><span class="sxs-lookup"><span data-stu-id="40413-297">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="40413-298">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="40413-298">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="40413-299">right aligned:</span><span class="sxs-lookup"><span data-stu-id="40413-299">right aligned:</span></span>|
|<span data-ttu-id="40413-300">:left aligned</span><span class="sxs-lookup"><span data-stu-id="40413-300">:left aligned</span></span>     |
|<span data-ttu-id="40413-301">:centered        :</span><span class="sxs-lookup"><span data-stu-id="40413-301">:centered        :</span></span>|

> [!TIP]
> L’extension Docs Authoring pour VS Code facilite l’ajout de tableaux Markdown simples !
>
> Vous pouvez également utiliser un [ générateur de tableau en ligne](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="40413-304">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="40413-304">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Cette classe fonctionne uniquement sur le site docs.microsoft.com.

<span data-ttu-id="40413-306">Si vous créez un tableau en Markdown, le tableau peut s’étendre sur la barre de navigation de droite et devient alors illisible.</span><span class="sxs-lookup"><span data-stu-id="40413-306">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="40413-307">Vous pouvez résoudre ce problème en permettant à l’affichage Docs de scinder le tableau.</span><span class="sxs-lookup"><span data-stu-id="40413-307">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="40413-308">Pour cela, il vous suffit d’encapsuler le tableau avec la classe personnalisée `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="40413-308">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="40413-309">Voici un exemple de code Markdown d’un tableau, avec trois lignes encapsulées par un `div`, avec le nom de classe `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="40413-309">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="40413-310">Cela s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-310">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="40413-311">Nom</span><span class="sxs-lookup"><span data-stu-id="40413-311">Name</span></span>|<span data-ttu-id="40413-312">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40413-312">Syntax</span></span>|<span data-ttu-id="40413-313">Obligatoire pour une installation sans assistance ?</span><span class="sxs-lookup"><span data-stu-id="40413-313">Mandatory for silent installation?</span></span>|<span data-ttu-id="40413-314">Description</span><span class="sxs-lookup"><span data-stu-id="40413-314">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="40413-315">Silencieux</span><span class="sxs-lookup"><span data-stu-id="40413-315">Quiet</span></span>|<span data-ttu-id="40413-316">/quiet</span><span class="sxs-lookup"><span data-stu-id="40413-316">/quiet</span></span>|<span data-ttu-id="40413-317">Oui</span><span class="sxs-lookup"><span data-stu-id="40413-317">Yes</span></span>|<span data-ttu-id="40413-318">Exécute le programme d’installation sans afficher d’interface utilisateur ni d’invites.</span><span class="sxs-lookup"><span data-stu-id="40413-318">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="40413-319">NoRestart</span><span class="sxs-lookup"><span data-stu-id="40413-319">NoRestart</span></span>|<span data-ttu-id="40413-320">/norestart</span><span class="sxs-lookup"><span data-stu-id="40413-320">/norestart</span></span>|<span data-ttu-id="40413-321">Non</span><span class="sxs-lookup"><span data-stu-id="40413-321">No</span></span>|<span data-ttu-id="40413-322">Supprime toute tentative de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="40413-322">Suppresses any attempts to restart.</span></span> <span data-ttu-id="40413-323">Par défaut, l’interface utilisateur invite l’utilisateur à confirmer le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="40413-323">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="40413-324">Aide</span><span class="sxs-lookup"><span data-stu-id="40413-324">Help</span></span>|<span data-ttu-id="40413-325">/help</span><span class="sxs-lookup"><span data-stu-id="40413-325">/help</span></span>|<span data-ttu-id="40413-326">Non</span><span class="sxs-lookup"><span data-stu-id="40413-326">No</span></span>|<span data-ttu-id="40413-327">Fournit de l’aide et un aide-mémoire.</span><span class="sxs-lookup"><span data-stu-id="40413-327">Provides help and quick reference.</span></span> <span data-ttu-id="40413-328">Affiche l’utilisation correcte de la commande d’installation, y compris la liste de tous les comportements et options.</span><span class="sxs-lookup"><span data-stu-id="40413-328">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="40413-329">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="40413-329">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40413-330">Cette classe fonctionne uniquement sur le site docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="40413-330">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="40413-331">Il arrive parfois que la deuxième colonne d’un tableau contienne de très longs mots.</span><span class="sxs-lookup"><span data-stu-id="40413-331">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="40413-332">Pour qu’ils soient correctement scindés, vous pouvez appliquer la classe `mx-tdCol2BreakAll` à l’aide de la syntaxe du wrapper `div`, comme indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="40413-332">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="40413-333">Tableaux HTML</span><span class="sxs-lookup"><span data-stu-id="40413-333">HTML Tables</span></span>

<span data-ttu-id="40413-334">Les tableaux HTML ne sont pas recommandés dans docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="40413-334">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="40413-335">Ils ne se présentent pas sous une forme conviviale dans le source, ce qui va à l’encontre d’un principe essentiel de Markdown.</span><span class="sxs-lookup"><span data-stu-id="40413-335">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="40413-336">Vidéos</span><span class="sxs-lookup"><span data-stu-id="40413-336">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="40413-337">Incorporation de vidéos dans une page Markdown</span><span class="sxs-lookup"><span data-stu-id="40413-337">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="40413-338">À l’heure actuelle, Docs peut prendre en charge les vidéos publiées sur :</span><span class="sxs-lookup"><span data-stu-id="40413-338">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="40413-339">YouTube</span><span class="sxs-lookup"><span data-stu-id="40413-339">YouTube</span></span>
- <span data-ttu-id="40413-340">Canal 9</span><span class="sxs-lookup"><span data-stu-id="40413-340">Channel 9</span></span>
- <span data-ttu-id="40413-341">Système « One Player » de Microsoft</span><span class="sxs-lookup"><span data-stu-id="40413-341">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="40413-342">Vous pouvez incorporer une vidéo avec la syntaxe suivante et permettre à Docs de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="40413-342">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="40413-343">Exemple :</span><span class="sxs-lookup"><span data-stu-id="40413-343">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="40413-344">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="40413-344">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="40413-345">Elle s’affiche ainsi sur les pages publiées :</span><span class="sxs-lookup"><span data-stu-id="40413-345">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="40413-346">L’URL de la vidéo CH9 doit commencer par `https` et se terminer par `/player`.</span><span class="sxs-lookup"><span data-stu-id="40413-346">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="40413-347">Sinon, le code incorpore la page entière au lieu de la vidéo uniquement.</span><span class="sxs-lookup"><span data-stu-id="40413-347">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="40413-348">Chargement de nouvelles vidéos</span><span class="sxs-lookup"><span data-stu-id="40413-348">Uploading new videos</span></span>

<span data-ttu-id="40413-349">Toute nouvelle vidéo doit être chargée à l’aide du processus suivant :</span><span class="sxs-lookup"><span data-stu-id="40413-349">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="40413-350">Rejoignez le groupe **docs_video_users** sur IDWEB.</span><span class="sxs-lookup"><span data-stu-id="40413-350">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="40413-351">Accédez à https://aka.ms/VideoUploadRequest, puis indiquez les détails de votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="40413-351">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="40413-352">Munissez-vous des éléments suivants (dont aucun ne sera visible publiquement) :</span><span class="sxs-lookup"><span data-stu-id="40413-352">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="40413-353">Titre de votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="40413-353">A title for your video.</span></span>
    1. <span data-ttu-id="40413-354">Liste de produits/services avec lesquels votre vidéo a un lien.</span><span class="sxs-lookup"><span data-stu-id="40413-354">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="40413-355">Page cible ou, à défaut, documentation qui hébergera votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="40413-355">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="40413-356">Lien vers le fichier MP4 de votre vidéo (si vous n’avez pas d’emplacement pour le fichier, vous pouvez le placer ici provisoirement : `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="40413-356">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="40413-357">Les fichiers MP4 doivent être au format 720p ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="40413-357">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="40413-358">Description de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="40413-358">A description of the video.</span></span>
1. <span data-ttu-id="40413-359">Soumettez (enregistrez) cet élément.</span><span class="sxs-lookup"><span data-stu-id="40413-359">Submit (save) that item.</span></span>
1. <span data-ttu-id="40413-360">La vidéo est chargée dans un délai maximal de deux jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="40413-360">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="40413-361">Le lien dont vous avez besoin pour l’incorporation est placé dans l’élément de travail et *vous sera rendu* prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="40413-361">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="40413-362">Une fois que vous avez récupéré le lien de la vidéo, fermez l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="40413-362">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="40413-363">Vous pouvez alors ajouter le lien de la vidéo à votre publication à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="40413-363">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
