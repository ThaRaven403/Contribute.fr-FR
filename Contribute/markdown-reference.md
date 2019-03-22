---
title: Informations de référence sur Markdown pour docs.microsoft.com
description: Découvrez la syntaxe et les fonctionnalités Markdown utilisées dans la plateforme Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.openlocfilehash: b4ac631a4ebdf7daf00bc39be80fe2e479720392
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987879"
---
# <a name="markdown-reference"></a><span data-ttu-id="0b2a4-103">Informations de référence sur Markdown</span><span class="sxs-lookup"><span data-stu-id="0b2a4-103">Markdown Reference</span></span>

<span data-ttu-id="0b2a4-104">Markdown est un langage de balisage léger avec une syntaxe de mise en forme en texte brut.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="0b2a4-105">La plateforme Docs prend en charge la norme CommonMark pour Markdown, ainsi que certaines extensions Markdown personnalisées conçues pour fournir du contenu enrichi sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-105">The Docs platform supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="0b2a4-106">Cet article fournit des informations de référence par ordre alphabétique, qui facilitent l’utilisation de Markdown pour docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-106">This article provides an alphabetical reference for using Markdown for docs.microsoft.com.</span></span>

<span data-ttu-id="0b2a4-107">Vous pouvez utiliser n’importe quel éditeur de texte pour créer du contenu Markdown.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="0b2a4-108">Comme éditeur facilitant l’insertion à la fois d’une syntaxe Markdown standard et d’extensions Docs personnalisées, nous recommandons [VS Code](https://code.visualstudio.com/) avec le [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installé.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-108">For an editor that facilitates inserting both standard Markdown syntax and custom Docs extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="0b2a4-109">Docs utilise le moteur Markdown Markdig.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-109">Docs uses the Markdig Markdown engine.</span></span> <span data-ttu-id="0b2a4-110">Vous pouvez tester le rendu de Markdown dans Markdig par rapport à d’autre moteurs sur [https://babelmark.github.io/](https://babelmark.github.io/).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="0b2a4-111">Alertes (Remarque, Conseil, Important, Attention, Avertissement)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="0b2a4-112">Les alertes sont une extension Markdown Docs pour créer des citations qui s’affichent sur docs.microsoft.com avec des couleurs et des icônes indiquant la signification du contenu.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-112">Alerts are a Docs Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="0b2a4-113">Les types d’alerte suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-113">The following alert types are supported:</span></span>

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

<span data-ttu-id="0b2a4-114">Ces alertes ressemblent à ceci sur docs.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="0b2a4-115">Informations que l’utilisateur doit remarquer même s’il parcourt le contenu rapidement.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="0b2a4-116">Informations facultatives qui aident l’utilisateur à être plus performant.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2a4-117">Informations essentielles nécessaires à la réussite de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="0b2a4-118">Conséquences éventuellement négatives d’une action.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="0b2a4-119">Certaines conséquences dangereuses d’une action.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="0b2a4-120">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="0b2a4-120">Code snippets</span></span>

<span data-ttu-id="0b2a4-121">Vous pouvez incorporer des extraits de code dans vos fichiers Markdown :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="0b2a4-122">En-têtes</span><span class="sxs-lookup"><span data-stu-id="0b2a4-122">Headings</span></span>

<span data-ttu-id="0b2a4-123">Docs prend en charge six niveaux de titres Markdown :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-123">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="0b2a4-124">Il doit y avoir un espace entre le signe `#` et le texte du titre.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="0b2a4-125">Chaque fichier Markdown doit avoir un, et un seul, titre H1.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="0b2a4-126">Le titre H1 doit être le premier contenu du fichier après le bloc de métadonnées YML.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="0b2a4-127">Les titres H2 apparaissent automatiquement dans le menu de navigation de droite du fichier publié.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="0b2a4-128">Ce n’est pas le cas des titres de niveau inférieur, donc privilégiez l’utilisation de titres H2 pour aider les lecteurs à parcourir votre contenu.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="0b2a4-129">Les titres HMTL, comme `<h1>`, ne sont pas recommandés. En effet, dans certains cas, ils entraînent l’affichage d’avertissements de génération.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="0b2a4-130">Vous pouvez créer un lien vers des titres spécifiques dans un fichier par le biais de [signets](#bookmark-links).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="0b2a4-131">HTML</span><span class="sxs-lookup"><span data-stu-id="0b2a4-131">HTML</span></span>

<span data-ttu-id="0b2a4-132">Bien que Markdown prenne en charge la syntaxe HTML inline, HTML n’est pas recommandé pour une publication sur Docs, car, sauf pour un ensemble limité de valeurs, il entraîne des avertissements ou des erreurs de génération.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-132">Although Markdown supports inline HTML, HTML is not recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span>

## <a name="images"></a><span data-ttu-id="0b2a4-133">Images</span><span class="sxs-lookup"><span data-stu-id="0b2a4-133">Images</span></span>

<span data-ttu-id="0b2a4-134">La syntaxe pour inclure une image est :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="0b2a4-135">Où `alt text` est une brève description de l’image et `<folder path>` un chemin relatif de l’image.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="0b2a4-136">Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="0b2a4-137">Ce texte est également utile si le site contient un bogue qui empêche l’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="0b2a4-138">Les images doivent être stockées dans un dossier `/media` au sein de votre documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="0b2a4-139">Les types de fichiers suivants sont pris en charge par défaut pour les images :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="0b2a4-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="0b2a4-140">.jpg</span></span>
- <span data-ttu-id="0b2a4-141">.png</span><span class="sxs-lookup"><span data-stu-id="0b2a4-141">.png</span></span>

<span data-ttu-id="0b2a4-142">Vous pouvez ajouter la prise en charge d’autres types d’image en les ajoutant comme ressources au fichier docfx.json</span><span class="sxs-lookup"><span data-stu-id="0b2a4-142">You can add support for other image types by adding them as resources to the docfx.json file</span></span><!--add link to reference when available--> <span data-ttu-id="0b2a4-143">de votre documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-143">for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="0b2a4-144">Liens</span><span class="sxs-lookup"><span data-stu-id="0b2a4-144">Links</span></span>

<span data-ttu-id="0b2a4-145">Dans la plupart des cas, Docs utilise des liens Markdown standard vers d’autres fichiers et pages.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-145">In most cases, Docs uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="0b2a4-146">Les types de liens sont décrits dans des sous-sections plus loin.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-146">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="0b2a4-147">Le Docs Authoring Pack pour VS Code peut aider à insérer correctement des signets et des liens relatifs sans avoir à deviner les chemins !</span><span class="sxs-lookup"><span data-stu-id="0b2a4-147">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2a4-148">N’incluez pas de codes de paramètres régionaux, comme en-us, dans vos liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-148">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="0b2a4-149">Les codes de paramètres régionaux codés en dur empêchent l’affichage du contenu traduit, ce qui procure une mauvaise expérience aux utilisateurs dans d’autres paramètres régionaux et engendre des coûts de traduction significatifs.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-149">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="0b2a4-150">Quand vous copiez une URL à partir d’un navigateur, le code de paramètres régionaux est inclus par défaut ; vous devez le supprimer manuellement quand vous créez votre lien.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-150">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="0b2a4-151">Par exemple, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-151">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="0b2a4-152">Pas :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-152">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="0b2a4-153">Liens relatifs vers des fichiers de la même documentation</span><span class="sxs-lookup"><span data-stu-id="0b2a4-153">Relative links to files in the same doc set</span></span>

<span data-ttu-id="0b2a4-154">Un chemin relatif est le chemin du fichier cible par rapport au fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-154">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="0b2a4-155">Dans Docs, vous pouvez utiliser un chemin relatif pour créer un lien vers un autre fichier de la même documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-155">In Docs, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="0b2a4-156">La syntaxe d’un chemin relatif est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-156">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="0b2a4-157">Où `../` indique un niveau au-dessus dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-157">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="0b2a4-158">Le chemin relatif est résolu pendant la génération, qui inclut la suppression de l’extension .md.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-158">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="0b2a4-159">Vous pouvez utiliser « ../ » pour créer un lien vers le fichier dans le dossier parent, mais ce fichier doit se trouver dans la même documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-159">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="0b2a4-160">Vous ne pouvez pas utiliser « ../ » pour créer un lien vers un fichier d’une autre documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-160">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="0b2a4-161">Docs prend également en charge une forme spéciale de chemin relatif qui commence par « ~ » (par exemple, ~/foo/bar.md).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-161">Docs also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="0b2a4-162">Cette syntaxe indique un fichier par rapport au dossier racine d’une documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-162">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="0b2a4-163">Ce genre de chemin est aussi validé et résolu pendant la génération.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-163">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2a4-164">Ajoutez l’extension de fichier dans le chemin relatif.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-164">Include the file extension in the relative path.</span></span> <span data-ttu-id="0b2a4-165">La génération valide l’existence du fichier cible de ce chemin relatif.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-165">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="0b2a4-166">Si le chemin relatif n’inclut pas d’extension de fichier, il est probable qu’un avertissement de lien rompu apparaisse lors de la génération.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-166">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="0b2a4-167">Par exemple, utilisez :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-167">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="0b2a4-168">Pas :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-168">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="site-relative-links-to-other-files-on-docs"></a><span data-ttu-id="0b2a4-169">Liens relatifs de site vers d’autres fichiers sur Docs</span><span class="sxs-lookup"><span data-stu-id="0b2a4-169">Site relative links to other files on Docs</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="0b2a4-170">N’incluez pas l’extension de fichier (.md).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-170">Do not include the file extension (.md).</span></span> <span data-ttu-id="0b2a4-171">Ce lien dirige vers le fichier Linux « overview » depuis l’extérieur de la documentation Azure « articles ».</span><span class="sxs-lookup"><span data-stu-id="0b2a4-171">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="0b2a4-172">Liens vers des sites externes</span><span class="sxs-lookup"><span data-stu-id="0b2a4-172">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="0b2a4-173">Lien basé sur une URL vers une autre page web (doit inclure https://).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-173">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="0b2a4-174">Liens de signet</span><span class="sxs-lookup"><span data-stu-id="0b2a4-174">Bookmark links</span></span>

<span data-ttu-id="0b2a4-175">Lien de signet vers un titre d’un autre fichier du même dépôt</span><span class="sxs-lookup"><span data-stu-id="0b2a4-175">Bookmark link to a heading in another file in the same repo.</span></span> <span data-ttu-id="0b2a4-176">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-176">For example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="0b2a4-177">Lien de signet vers un titre du fichier actuel :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-177">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="0b2a4-178">Utilisez un signe dièse `#` suivi des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-178">Use a hash mark `#` followed by the words of the heading.</span></span> <span data-ttu-id="0b2a4-179">Pour changer le texte du titre dans le texte du lien :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-179">To change the heading text into link text:</span></span>
- <span data-ttu-id="0b2a4-180">Utiliser des caractères minuscules</span><span class="sxs-lookup"><span data-stu-id="0b2a4-180">Use all lowercase characters</span></span>
- <span data-ttu-id="0b2a4-181">Supprimer la ponctuation</span><span class="sxs-lookup"><span data-stu-id="0b2a4-181">Remove punctuation</span></span>
- <span data-ttu-id="0b2a4-182">Remplacer les espaces par des tirets</span><span class="sxs-lookup"><span data-stu-id="0b2a4-182">Replace spaces with dashes</span></span>

<span data-ttu-id="0b2a4-183">Par exemple, si le nom du titre est « Problèmes de sécurité 2.2 », le texte du lien du signet sera « #problèmes-de-sécurité-22 ».</span><span class="sxs-lookup"><span data-stu-id="0b2a4-183">For example, if the heading name is "2.2 Security concerns", then the bookmark link text will be "#22-security-concerns".</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="0b2a4-184">Liens d’ancrage explicites</span><span class="sxs-lookup"><span data-stu-id="0b2a4-184">Explicit anchor links</span></span>

<span data-ttu-id="0b2a4-185">Les liens d’ancrage explicites utilisant la balise HTML `<a>` **ne sont pas obligatoires ou recommandés** sauf dans les pages d’arrivée et hub.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-185">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="0b2a4-186">Utilisez des signets comme indiqué plus haut dans les fichiers Markdown généraux.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-186">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="0b2a4-187">Pour les pages hub et d’arrivée, utilisez des ancrages comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-187">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="0b2a4-188">`## <a id="AnchorText"> </a>Header text` ou `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-188">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="0b2a4-189">Pour créer un lien vers des ancrages explicites, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-189">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="0b2a4-190">Liens XREF (référence croisée)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-190">XREF (cross reference) links</span></span>

<span data-ttu-id="0b2a4-191">Pour créer un lien vers des pages de références d’API générées automatiquement dans la documentation actuelle ou dans d’autres documentations, utilisez des liens XREF avec l’ID unique (UID).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-191">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="0b2a4-192">Pour référencer des pages de références d’API dans d’autres jeux de documentation, vous devez ajouter la configuration `xrefService` dans le fichier `docfx.json`.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-192">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="0b2a4-193">L’UID équivaut au nom complet de la classe et du membre.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-193">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="0b2a4-194">Si vous ajoutez un \* après l’UID, le lien représente alors la page de la surcharge et non pas une API spécifique.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-194">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="0b2a4-195">Par exemple, utilisez `List<T>.BinarySearch*` pour créer un lien vers la page Méthode BinarySearch au lieu de créer un lien vers une surcharge spécifique telle que `List<T>.BinarySearch(T, IComparer<T>)`.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-195">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="0b2a4-196">Vous pouvez utiliser une des syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-196">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="0b2a4-197">Lien automatique : `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-197">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="0b2a4-198">Le paramètre de requête `displayProperty` facultatif produit un texte de lien complet.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-198">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="0b2a4-199">Par défaut, le texte du lien montre seulement le nom du membre ou du type.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-199">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="0b2a4-200">Lien Markdown : `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-200">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="0b2a4-201">À utiliser quand vous voulez personnaliser le texte du lien affiché.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-201">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="0b2a4-202">Exemples :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-202">Examples:</span></span>

- <span data-ttu-id="0b2a4-203">`<xref:System.String>` s’affiche sous la forme « String ».</span><span class="sxs-lookup"><span data-stu-id="0b2a4-203">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="0b2a4-204">`<xref:System.String?displayProperty=nameWithType>` s’affiche sous la forme « System.String ».</span><span class="sxs-lookup"><span data-stu-id="0b2a4-204">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="0b2a4-205">`[String class](xref:System.String)` s’affiche sous la forme « String class ».</span><span class="sxs-lookup"><span data-stu-id="0b2a4-205">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="0b2a4-206">Il n’existe actuellement aucun moyen facile de trouver les UID.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-206">Right now, there is no easy way to find the UIDs.</span></span> <!-- ? --><span data-ttu-id="0b2a4-207">La meilleure façon de trouver l’UID pour une API consiste à afficher la source de la page de l’API vers laquelle vous voulez créer un lien et à rechercher la valeur de ms.assetid.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-207">The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="0b2a4-208">Les valeurs des surcharges individuelles ne figurent pas dans la source.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-208">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="0b2a4-209">Nous nous efforçons de mettre au point un meilleur système dans le futur.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-209">We're working on having a better system in the future.</span></span>

<span data-ttu-id="0b2a4-210">Quand l’UID contient les caractères spéciaux \`, \# ou \*, la valeur de l’UID doit être encodée en HTML en tant que `%60`, `%23` et `%2A`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-210">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="0b2a4-211">Vous pouvez parfois trouver des parenthèses dans l’encodage, mais elles ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-211">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="0b2a4-212">Exemples :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-212">Examples:</span></span>

- <span data-ttu-id="0b2a4-213">System.Threading.Tasks.Task\`1 devient `System.Threading.Tasks.Task%601`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-213">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="0b2a4-214">System.Exception.\#ctor devient `System.Exception.%23ctor`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-214">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="0b2a4-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) devient `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span><span class="sxs-lookup"><span data-stu-id="0b2a4-215">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="0b2a4-216">Listes (numérotées, à puces, liste de contrôle)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-216">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="0b2a4-217">Liste numérotée</span><span class="sxs-lookup"><span data-stu-id="0b2a4-217">Numbered list</span></span>

<span data-ttu-id="0b2a4-218">Pour créer une liste numérotée, vous pouvez utiliser exclusivement des « 1 », qui sont restitués sous la forme d’une liste séquentielle au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-218">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="0b2a4-219">Pour accroître la lisibilité du texte source, vous pouvez incrémenter vos listes.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-219">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="0b2a4-220">N’utilisez pas de lettres dans les listes, y compris dans les listes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-220">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="0b2a4-221">Elles ne sont pas restituées correctement au moment de la publication sur Docs. Les listes imbriquées utilisant des nombres sont restituées avec des lettres minuscules au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-221">They do not render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="0b2a4-222">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-222">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="0b2a4-223">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-223">This renders as follows:</span></span>

1. <span data-ttu-id="0b2a4-224">This is</span><span class="sxs-lookup"><span data-stu-id="0b2a4-224">This is</span></span>
1. <span data-ttu-id="0b2a4-225">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="0b2a4-225">a parent numbered list</span></span>
   1. <span data-ttu-id="0b2a4-226">and this is</span><span class="sxs-lookup"><span data-stu-id="0b2a4-226">and this is</span></span>
   1. <span data-ttu-id="0b2a4-227">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="0b2a4-227">a nested numbered list</span></span>
1. <span data-ttu-id="0b2a4-228">(fin)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-228">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="0b2a4-229">Liste à puces</span><span class="sxs-lookup"><span data-stu-id="0b2a4-229">Bulleted list</span></span>

<span data-ttu-id="0b2a4-230">Pour créer une liste à puces, utilisez `-` suivi d’un espace au début de chaque ligne :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-230">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="0b2a4-231">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-231">This renders as follows:</span></span>

- <span data-ttu-id="0b2a4-232">This is</span><span class="sxs-lookup"><span data-stu-id="0b2a4-232">This is</span></span>
- <span data-ttu-id="0b2a4-233">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="0b2a4-233">a parent bulleted list</span></span>
  - <span data-ttu-id="0b2a4-234">and this is</span><span class="sxs-lookup"><span data-stu-id="0b2a4-234">and this is</span></span>
  - <span data-ttu-id="0b2a4-235">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="0b2a4-235">a nested bulleted list</span></span>
- <span data-ttu-id="0b2a4-236">All done!</span><span class="sxs-lookup"><span data-stu-id="0b2a4-236">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="0b2a4-237">Liste de contrôle</span><span class="sxs-lookup"><span data-stu-id="0b2a4-237">Checklist</span></span>

<span data-ttu-id="0b2a4-238">Les listes de contrôle sont utilisables sur docs.microsoft.com (uniquement) par le biais d’une extension Markdown personnalisée :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-238">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="0b2a4-239">Cet exemple s’affiche sur docs.microsoft.com ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-239">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="0b2a4-240">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="0b2a4-240">List item 1</span></span>
> * <span data-ttu-id="0b2a4-241">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="0b2a4-241">List item 2</span></span>
> * <span data-ttu-id="0b2a4-242">Élément de liste 3</span><span class="sxs-lookup"><span data-stu-id="0b2a4-242">List item 3</span></span>

<span data-ttu-id="0b2a4-243">Utilisez des listes de contrôle au début ou à la fin d’un article pour récapituler le contenu que l’utilisateur va étudier ou a étudié.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-243">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="0b2a4-244">N’ajoutez pas de listes de contrôle aléatoires dans vos articles.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-244">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="0b2a4-245">Action d’étape suivante</span><span class="sxs-lookup"><span data-stu-id="0b2a4-245">Next step action</span></span>

<span data-ttu-id="0b2a4-246">Vous pouvez utiliser une extension personnalisée pour ajouter un bouton d’action d’étape suivante à des pages sur docs.microsoft.com (uniquement).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-246">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="0b2a4-247">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-247">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="0b2a4-248">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-248">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="0b2a4-249">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-249">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="0b2a4-250">Découvrir le style simple</span><span class="sxs-lookup"><span data-stu-id="0b2a4-250">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="0b2a4-251">Vous pouvez utiliser n’importe quel lien pris en charge dans une action d’étape suivante, y compris un lien Markdown vers une autre page web.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-251">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="0b2a4-252">Dans la plupart des cas, le lien d’action suivante est un lien relatif vers un autre fichier de la même documentation.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-252">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="0b2a4-253">Définition de section</span><span class="sxs-lookup"><span data-stu-id="0b2a4-253">Section definition</span></span>

<!-- more info about this would be helpful! -->
<span data-ttu-id="0b2a4-254">Vous aurez peut-être à définir une section.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-254">You might need to define a section.</span></span> <span data-ttu-id="0b2a4-255">Cette syntaxe est principalement utilisée pour les tables de code.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-255">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="0b2a4-256">Regardez l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-256">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="0b2a4-257">Le texte Markdown de citation précédent s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-257">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="0b2a4-258">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="0b2a4-258">Selectors</span></span>

<!-- could be more clear! -->
<span data-ttu-id="0b2a4-259">Vous pouvez utiliser un sélecteur pour lier plusieurs pages d’un même article.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-259">You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="0b2a4-260">Les lecteurs peuvent ainsi passer d’une page à l’autre.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-260">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="0b2a4-261">Cette extension fonctionne différemment sur docs.microsoft.com et sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-261">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="0b2a4-262">Sélecteur unique</span><span class="sxs-lookup"><span data-stu-id="0b2a4-262">Single selector</span></span>

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

<span data-ttu-id="0b2a4-263">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-263">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Windows universel](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="0b2a4-272">Sélecteur multiple</span><span class="sxs-lookup"><span data-stu-id="0b2a4-272">Multi-selector</span></span>

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

<span data-ttu-id="0b2a4-273">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-273">... will be rendered like this:</span></span>

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

## <a name="tables"></a><span data-ttu-id="0b2a4-284">les tableaux</span><span class="sxs-lookup"><span data-stu-id="0b2a4-284">Tables</span></span>

<span data-ttu-id="0b2a4-285">Le moyen le plus simple de créer un tableau en Markdown est d’utiliser des barres verticales et des lignes.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-285">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="0b2a4-286">Pour créer un tableau standard avec un en-tête, faites suivre la première ligne d’une ligne en pointillés :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-286">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="0b2a4-287">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-287">This renders as follows:</span></span>

|<span data-ttu-id="0b2a4-288">This is</span><span class="sxs-lookup"><span data-stu-id="0b2a4-288">This is</span></span>   |<span data-ttu-id="0b2a4-289">a simple</span><span class="sxs-lookup"><span data-stu-id="0b2a4-289">a simple</span></span>   |<span data-ttu-id="0b2a4-290">table header</span><span class="sxs-lookup"><span data-stu-id="0b2a4-290">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="0b2a4-291">table</span><span class="sxs-lookup"><span data-stu-id="0b2a4-291">table</span></span>     |<span data-ttu-id="0b2a4-292">data</span><span class="sxs-lookup"><span data-stu-id="0b2a4-292">data</span></span>       |<span data-ttu-id="0b2a4-293">here</span><span class="sxs-lookup"><span data-stu-id="0b2a4-293">here</span></span>        |
|<span data-ttu-id="0b2a4-294">it doesn't</span><span class="sxs-lookup"><span data-stu-id="0b2a4-294">it doesn't</span></span>|<span data-ttu-id="0b2a4-295">actually</span><span class="sxs-lookup"><span data-stu-id="0b2a4-295">actually</span></span>   |<span data-ttu-id="0b2a4-296">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="0b2a4-296">have to line up nicely!</span></span>||

<span data-ttu-id="0b2a4-297">Vous pouvez également créer un tableau sans en-tête.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-297">You can also create a table without a header.</span></span> <span data-ttu-id="0b2a4-298">Par exemple, pour créer une liste à plusieurs colonnes :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-298">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="0b2a4-299">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-299">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="0b2a4-300">This</span><span class="sxs-lookup"><span data-stu-id="0b2a4-300">This</span></span> | <span data-ttu-id="0b2a4-301">table</span><span class="sxs-lookup"><span data-stu-id="0b2a4-301">table</span></span> |
| <span data-ttu-id="0b2a4-302">has no</span><span class="sxs-lookup"><span data-stu-id="0b2a4-302">has no</span></span> | <span data-ttu-id="0b2a4-303">header</span><span class="sxs-lookup"><span data-stu-id="0b2a4-303">header</span></span> |

<span data-ttu-id="0b2a4-304">Vous pouvez aligner les colonnes à l’aide de signes deux-points :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-304">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="0b2a4-305">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-305">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="0b2a4-306">right aligned:</span><span class="sxs-lookup"><span data-stu-id="0b2a4-306">right aligned:</span></span>|
|<span data-ttu-id="0b2a4-307">:left aligned</span><span class="sxs-lookup"><span data-stu-id="0b2a4-307">:left aligned</span></span>     |
|<span data-ttu-id="0b2a4-308">:centered        :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-308">:centered        :</span></span>|

> [!TIP]
> L’extension Docs Authoring pour VS Code facilite l’ajout de tableaux Markdown simples !
>
> Vous pouvez également utiliser un [ générateur de tableau en ligne](http://www.tablesgenerator.com/markdown_tables).

### <a name="mx-tdbreakall"></a><span data-ttu-id="0b2a4-311">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="0b2a4-311">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> Cette classe fonctionne uniquement sur le site docs.microsoft.com.

<span data-ttu-id="0b2a4-313">Si vous créez un tableau en Markdown, le tableau peut s’étendre sur la barre de navigation de droite et devient alors illisible.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-313">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="0b2a4-314">Vous pouvez résoudre ce problème en permettant à l’affichage Docs de scinder le tableau.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-314">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="0b2a4-315">Pour cela, il vous suffit d’encapsuler le tableau avec la classe personnalisée `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-315">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="0b2a4-316">Voici un exemple de code Markdown d’un tableau, avec trois lignes encapsulées par un `div`, avec le nom de classe `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-316">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="0b2a4-317">Cela s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-317">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="0b2a4-318">Nom</span><span class="sxs-lookup"><span data-stu-id="0b2a4-318">Name</span></span>|<span data-ttu-id="0b2a4-319">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b2a4-319">Syntax</span></span>|<span data-ttu-id="0b2a4-320">Obligatoire pour une installation sans assistance ?</span><span class="sxs-lookup"><span data-stu-id="0b2a4-320">Mandatory for silent installation?</span></span>|<span data-ttu-id="0b2a4-321">Description</span><span class="sxs-lookup"><span data-stu-id="0b2a4-321">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="0b2a4-322">Silencieux</span><span class="sxs-lookup"><span data-stu-id="0b2a4-322">Quiet</span></span>|<span data-ttu-id="0b2a4-323">/quiet</span><span class="sxs-lookup"><span data-stu-id="0b2a4-323">/quiet</span></span>|<span data-ttu-id="0b2a4-324">Oui</span><span class="sxs-lookup"><span data-stu-id="0b2a4-324">Yes</span></span>|<span data-ttu-id="0b2a4-325">Exécute le programme d’installation sans afficher d’interface utilisateur ni d’invites.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-325">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="0b2a4-326">NoRestart</span><span class="sxs-lookup"><span data-stu-id="0b2a4-326">NoRestart</span></span>|<span data-ttu-id="0b2a4-327">/norestart</span><span class="sxs-lookup"><span data-stu-id="0b2a4-327">/norestart</span></span>|<span data-ttu-id="0b2a4-328">Non</span><span class="sxs-lookup"><span data-stu-id="0b2a4-328">No</span></span>|<span data-ttu-id="0b2a4-329">Supprime toute tentative de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-329">Suppresses any attempts to restart.</span></span> <span data-ttu-id="0b2a4-330">Par défaut, l’interface utilisateur invite l’utilisateur à confirmer le redémarrage.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-330">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="0b2a4-331">Aide</span><span class="sxs-lookup"><span data-stu-id="0b2a4-331">Help</span></span>|<span data-ttu-id="0b2a4-332">/help</span><span class="sxs-lookup"><span data-stu-id="0b2a4-332">/help</span></span>|<span data-ttu-id="0b2a4-333">Non</span><span class="sxs-lookup"><span data-stu-id="0b2a4-333">No</span></span>|<span data-ttu-id="0b2a4-334">Fournit de l’aide et un aide-mémoire.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-334">Provides help and quick reference.</span></span> <span data-ttu-id="0b2a4-335">Affiche l’utilisation correcte de la commande d’installation, y compris la liste de tous les comportements et options.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-335">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="0b2a4-336">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="0b2a4-336">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b2a4-337">Cette classe fonctionne uniquement sur le site docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-337">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="0b2a4-338">Il arrive parfois que la deuxième colonne d’un tableau contienne de très longs mots.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-338">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="0b2a4-339">Pour qu’ils soient correctement scindés, vous pouvez appliquer la classe `mx-tdCol2BreakAll` à l’aide de la syntaxe du wrapper `div`, comme indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-339">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="0b2a4-340">Tableaux HTML</span><span class="sxs-lookup"><span data-stu-id="0b2a4-340">HTML Tables</span></span>

<span data-ttu-id="0b2a4-341">Les tableaux HTML ne sont pas recommandés dans docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-341">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="0b2a4-342">Ils ne se présentent pas sous une forme conviviale dans le source, ce qui va à l’encontre d’un principe essentiel de Markdown.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-342">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="0b2a4-343">Vidéos</span><span class="sxs-lookup"><span data-stu-id="0b2a4-343">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="0b2a4-344">Incorporation de vidéos dans une page Markdown</span><span class="sxs-lookup"><span data-stu-id="0b2a4-344">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="0b2a4-345">À l’heure actuelle, Docs peut prendre en charge les vidéos publiées sur :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-345">Currently, Docs can support videos published to one of three locations:</span></span>

- <span data-ttu-id="0b2a4-346">YouTube</span><span class="sxs-lookup"><span data-stu-id="0b2a4-346">YouTube</span></span>
- <span data-ttu-id="0b2a4-347">Canal 9</span><span class="sxs-lookup"><span data-stu-id="0b2a4-347">Channel 9</span></span>
- <span data-ttu-id="0b2a4-348">Système « One Player » de Microsoft</span><span class="sxs-lookup"><span data-stu-id="0b2a4-348">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="0b2a4-349">Vous pouvez incorporer une vidéo avec la syntaxe suivante et permettre à Docs de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-349">You can embed a video with the following syntax, and Docs will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="0b2a4-350">Exemple :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-350">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="0b2a4-351">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-351">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="0b2a4-352">Elle s’affiche ainsi sur les pages publiées :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-352">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="0b2a4-353">L’URL de la vidéo CH9 doit commencer par `https` et se terminer par `/player`.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-353">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="0b2a4-354">Sinon, le code incorpore la page entière au lieu de la vidéo uniquement.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-354">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="0b2a4-355">Chargement de nouvelles vidéos</span><span class="sxs-lookup"><span data-stu-id="0b2a4-355">Uploading new videos</span></span>

<span data-ttu-id="0b2a4-356">Toute nouvelle vidéo doit être chargée à l’aide du processus suivant :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-356">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="0b2a4-357">Rejoignez le groupe **docs_video_users** sur IDWEB.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-357">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="0b2a4-358">Accédez à https://aka.ms/VideoUploadRequest, puis indiquez les détails de votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-358">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="0b2a4-359">Munissez-vous des éléments suivants (dont aucun ne sera visible publiquement) :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-359">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="0b2a4-360">Titre de votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-360">A title for your video.</span></span>
    1. <span data-ttu-id="0b2a4-361">Liste de produits/services avec lesquels votre vidéo a un lien.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-361">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="0b2a4-362">Page cible ou, à défaut, documentation qui hébergera votre vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-362">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="0b2a4-363">Lien vers le fichier MP4 de votre vidéo (si vous n’avez pas d’emplacement pour le fichier, vous pouvez le placer ici provisoirement : `\\scratch2\scratch\apex`).</span><span class="sxs-lookup"><span data-stu-id="0b2a4-363">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="0b2a4-364">Les fichiers MP4 doivent être au format 720p ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-364">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="0b2a4-365">Description de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-365">A description of the video.</span></span>
1. <span data-ttu-id="0b2a4-366">Soumettez (enregistrez) cet élément.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-366">Submit (save) that item.</span></span>
1. <span data-ttu-id="0b2a4-367">La vidéo est chargée dans un délai maximal de deux jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-367">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="0b2a4-368">Le lien dont vous avez besoin pour l’incorporation est placé dans l’élément de travail et *vous sera rendu* prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-368">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="0b2a4-369">Une fois que vous avez récupéré le lien de la vidéo, fermez l’élément de travail.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-369">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="0b2a4-370">Vous pouvez alors ajouter le lien de la vidéo à votre publication à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="0b2a4-370">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
