---
title: Informations de référence sur Markdown pour docs.microsoft.com
description: Découvrez la syntaxe et les fonctionnalités Markdown utilisées dans la plateforme Microsoft Docs.
author: meganbradley
ms.author: mbradley
ms.date: 01/30/2020
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.openlocfilehash: c1568264c687ebaf26048f5432fdea7d5132c012
ms.sourcegitcommit: 216ef77ca2cd1eeb31c6c89d96778b178fc0d540
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "80070077"
---
# <a name="docs-markdown-reference"></a><span data-ttu-id="c0c8b-103">Informations de référence sur Docs Markdown</span><span class="sxs-lookup"><span data-stu-id="c0c8b-103">Docs Markdown reference</span></span>

<span data-ttu-id="c0c8b-104">Cet article fournit des informations de référence par ordre alphabétique, qui facilitent l’écriture de Markdown pour docs.microsoft.com (Docs).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-104">This article provides an alphabetical reference for writing Markdown for docs.microsoft.com (Docs).</span></span>

<span data-ttu-id="c0c8b-105">[Markdown](https://daringfireball.net/projects/markdown/) est un langage de balisage léger avec une syntaxe de mise en forme en texte brut.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-105">[Markdown](https://daringfireball.net/projects/markdown/) is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="c0c8b-106">Docs prend en charge le Markdown conforme à [CommonMark](https://commonmark.org/) analysé via le moteur d’analyse [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-106">Docs supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="c0c8b-107">Docs prend également en charge les extensions Markdown personnalisées qui fournissent du contenu plus riche sur le site Docs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-107">Docs also supports custom Markdown extensions that provide richer content on the Docs site.</span></span>

<span data-ttu-id="c0c8b-108">Vous pouvez utiliser n’importe quel éditeur de texte pour écrire du Markdown, mais nous vous recommandons [Visual Studio Code](https://code.visualstudio.com/) avec le [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-108">You can use any text editor to write Markdown, but we recommend [Visual Studio Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack).</span></span> <span data-ttu-id="c0c8b-109">Le Docs Authoring Pack fournit des outils d’édition et des fonctionnalités d’aperçu qui vous permettent de voir à quoi ressemblent vos articles une fois affichés sur Docs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-109">The Docs Authoring Pack provides editing tools and preview functionality that lets you see what your articles will look like when rendered on Docs.</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="c0c8b-110">Alertes (Remarque, Conseil, Important, Attention, Avertissement)</span><span class="sxs-lookup"><span data-stu-id="c0c8b-110">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="c0c8b-111">Les alertes sont une extension Markdown pour créer des citations qui s’affichent sur docs.microsoft.com avec des couleurs et des icônes indiquant la signification du contenu.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-111">Alerts are a Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="c0c8b-112">Les types d’alerte suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-112">The following alert types are supported:</span></span>

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

<span data-ttu-id="c0c8b-113">Ces alertes ressemblent à ceci sur docs.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-113">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="c0c8b-114">Information the user should notice even if skimming.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-114">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="c0c8b-115">Optional information to help a user be more successful.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-115">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0c8b-116">Essential information required for user success.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-116">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="c0c8b-117">Negative potential consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-117">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="c0c8b-118">Dangerous certain consequences of an action.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-118">Dangerous certain consequences of an action.</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="c0c8b-119">Crochets pointus</span><span class="sxs-lookup"><span data-stu-id="c0c8b-119">Angle brackets</span></span>

<span data-ttu-id="c0c8b-120">Si vous utilisez des crochets pointus dans le texte de votre fichier, par exemple pour signaler un espace réservé, vous devez manuellement encoder les crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-120">If you use angle brackets in text in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="c0c8b-121">Sinon, Markdown considère qu’il s’agit d’une balise HTML.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-121">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="c0c8b-122">Par exemple, encodez `<script name>` en `&lt;script name&gt;` ou `\<script name>`.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-122">For example, encode `<script name>` as `&lt;script name&gt;` or `\<script name>`.</span></span>

<span data-ttu-id="c0c8b-123">Les crochets pointus n’ont pas besoin d’être placés dans une séquence d’échappement dans du texte mis en forme en tant que code inline ou dans des blocs de code.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-123">Angle brackets don't have to be escaped in text formatted as inline code or in code blocks.</span></span>

## <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="c0c8b-124">Apostrophes et guillemets</span><span class="sxs-lookup"><span data-stu-id="c0c8b-124">Apostrophes and quotation marks</span></span>

<span data-ttu-id="c0c8b-125">Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-125">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="c0c8b-126">Vous devez les encoder ou les changer en apostrophes/guillemets de base.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-126">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="c0c8b-127">Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="c0c8b-127">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="c0c8b-128">Voici les encodages pour les versions courbes de ces signes de ponctuation :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-128">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="c0c8b-129">Guillemet gauche (ouvrant) : `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="c0c8b-129">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="c0c8b-130">Guillemet droit (fermant) : `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="c0c8b-130">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="c0c8b-131">Guillemet simple droit (fermant) ou apostrophe : `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="c0c8b-131">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="c0c8b-132">Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="c0c8b-132">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

## <a name="blockquotes"></a><span data-ttu-id="c0c8b-133">Éléments blockquote</span><span class="sxs-lookup"><span data-stu-id="c0c8b-133">Blockquotes</span></span>

<span data-ttu-id="c0c8b-134">Pour créer un élément blockquote, vous utilisez le caractère `>` :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-134">Blockquotes are created using the `>` character:</span></span>

```md
> This is a blockquote. It is usually rendered indented and with a different background color.
```

<span data-ttu-id="c0c8b-135">L’exemple précédent s’affiche comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-135">The preceding example renders as follows:</span></span>

> <span data-ttu-id="c0c8b-136">Il s’agit d’un bloc de citation.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-136">This is a blockquote.</span></span> <span data-ttu-id="c0c8b-137">Il est généralement affiché en retrait et avec une couleur d’arrière-plan différente.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-137">It is usually rendered indented and with a different background color.</span></span>

## <a name="bold-and-italic-text"></a><span data-ttu-id="c0c8b-138">Texte en gras et italique</span><span class="sxs-lookup"><span data-stu-id="c0c8b-138">Bold and italic text</span></span>

<span data-ttu-id="c0c8b-139">Pour mettre en forme le texte en **gras**, entourez-le de deux astérisques :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-139">To format text as **bold**, enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="c0c8b-140">Pour mettre en forme le texte en *italique*, entourez-le d’un seul astérisque :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-140">To format text as *italic*, enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="c0c8b-141">Pour mettre en forme le texte en ***gras et en italique***, entourez-le de trois astérisques :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-141">To format text as both ***bold and italic***, enclose it in three asterisks:</span></span>

```markdown
This text is both ***bold and italic***.
```

## <a name="code-snippets"></a><span data-ttu-id="c0c8b-142">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="c0c8b-142">Code snippets</span></span>

<span data-ttu-id="c0c8b-143">Docs Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-143">Docs Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="c0c8b-144">Pour plus d’informations, consultez [Guide pratique pour ajouter du code à la documentation](code-in-docs.md).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-144">For more information, see [How to add code to docs](code-in-docs.md).</span></span>

## <a name="columns"></a><span data-ttu-id="c0c8b-145">Colonnes</span><span class="sxs-lookup"><span data-stu-id="c0c8b-145">Columns</span></span>

<span data-ttu-id="c0c8b-146">L’extension Markdown pour les **colonnes** donne aux auteurs de documentation la possibilité d’ajouter des dispositions de contenu basées sur des colonnes qui sont plus flexibles et plus puissantes que les tableaux Markdown de base, qui sont adaptés uniquement aux données véritablement tabulaires.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-146">The **columns** Markdown extension gives Docs authors the ability to add column-based content layouts that are more flexible and powerful than basic Markdown tables, which are only suited for true tabular data.</span></span> <span data-ttu-id="c0c8b-147">Vous pouvez ajouter jusqu’à quatre colonnes et utiliser l’attribut facultatif `span` pour fusionner deux colonnes ou plus.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-147">You can add up to four columns, and use the optional `span` attribute to merge two or more columns.</span></span>

<span data-ttu-id="c0c8b-148">La syntaxe des colonnes est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-148">The syntax for columns is as follows:</span></span>

```markdown
:::row:::
   :::column span="":::
      Content...
   :::column-end:::
   :::column span="":::
      More content...
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="c0c8b-149">Les colonnes doivent contenir uniquement du Markdown de base, y compris des images.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-149">Columns should only contain basic Markdown, including images.</span></span> <span data-ttu-id="c0c8b-150">Les en-têtes, tableaux, onglets et autres structures complexes ne doivent pas être inclus.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-150">Headings, tables, tabs, and other complex structures shouldn't be included.</span></span> <span data-ttu-id="c0c8b-151">Une ligne ne peut pas avoir de contenu en dehors de la colonne.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-151">A row can't have any content outside of column.</span></span>

<span data-ttu-id="c0c8b-152">Par exemple, le Markdown suivant crée une colonne qui s’étend sur deux largeurs de colonne et une colonne standard (pas de `span`) :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-152">For example, the following Markdown creates one column that spans two column widths, and one standard (no `span`) column:</span></span>

```markdown
:::row:::
   :::column span="2":::
      **This is a 2-span column with lots of text.**

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec vestibulum mollis nunc
      ornare commodo. Nullam ac metus imperdiet, rutrum justo vel, vulputate leo. Donec
      rutrum non eros eget consectetur.
   :::column-end:::
   :::column span="":::
      **This is a single-span column with an image in it.**

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::
```

<span data-ttu-id="c0c8b-153">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-153">This renders as follows:</span></span>

:::row:::
   :::column span="2":::
      <span data-ttu-id="c0c8b-154">**Il s’agit d’une colonne à double étendue qui contient beaucoup de texte.**</span><span class="sxs-lookup"><span data-stu-id="c0c8b-154">**This is a 2-span column with lots of text.**</span></span>

      <span data-ttu-id="c0c8b-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-155">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</span></span> <span data-ttu-id="c0c8b-156">Donec vestibulum mollis nunc ornare commodo.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-156">Donec vestibulum mollis nunc ornare commodo.</span></span> <span data-ttu-id="c0c8b-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-157">Nullam ac metus imperdiet, rutrum justo vel, vulputate leo.</span></span> <span data-ttu-id="c0c8b-158">Donec rutrum non eros eget consectetur.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-158">Donec rutrum non eros eget consectetur.</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c0c8b-159">**Il s’agit d’une colonne à étendue unique avec une image.**</span><span class="sxs-lookup"><span data-stu-id="c0c8b-159">**This is a single-span column with an image in it.**</span></span>

      ![Doc.U.Ment](media/markdown-reference/document.png)
   :::column-end:::
:::row-end:::

## <a name="headings"></a><span data-ttu-id="c0c8b-161">En-têtes</span><span class="sxs-lookup"><span data-stu-id="c0c8b-161">Headings</span></span>

<span data-ttu-id="c0c8b-162">Docs prend en charge six niveaux de titres Markdown :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-162">Docs supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="c0c8b-163">Il doit y avoir un espace entre le signe `#` et le texte du titre.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-163">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="c0c8b-164">Chaque fichier Markdown doit avoir un, et un seul, titre H1.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-164">Each Markdown file must have one and only one H1 heading.</span></span>
- <span data-ttu-id="c0c8b-165">Le titre H1 doit être le premier contenu du fichier après le bloc de métadonnées YML.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-165">The H1 heading must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="c0c8b-166">Les titres H2 apparaissent automatiquement dans le menu de navigation de droite du fichier publié.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-166">H2 headings automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="c0c8b-167">Les titres de niveau inférieur n’apparaissant pas, privilégiez l’utilisation de titres H2 pour aider les lecteurs à parcourir votre contenu.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-167">Lower-level headings don't appear, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="c0c8b-168">Les titres HTML, comme `<h1>`, ne sont pas recommandés. En effet, dans certains cas, ils entraînent l’affichage d’avertissements de génération.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-168">HTML headings, such as `<h1>`, aren't recommended, and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="c0c8b-169">Vous pouvez créer un lien vers des titres spécifiques dans un fichier par le biais de [liens de signet](how-to-write-links.md#links-to-anchors).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-169">You can link to individual headings in a file via [bookmark links](how-to-write-links.md#links-to-anchors).</span></span>

## <a name="html"></a><span data-ttu-id="c0c8b-170">HTML</span><span class="sxs-lookup"><span data-stu-id="c0c8b-170">HTML</span></span>

<span data-ttu-id="c0c8b-171">Bien que Markdown prenne en charge la syntaxe HTML inline, HTML n’est pas recommandé pour une publication sur Docs, car, sauf pour un ensemble limité de valeurs, il entraîne des avertissements ou des erreurs de génération.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-171">Although Markdown supports inline HTML, HTML isn't recommended for publishing to Docs, and except for a limited list of values will cause build errors or warnings.</span></span> 

## <a name="images"></a><span data-ttu-id="c0c8b-172">Images</span><span class="sxs-lookup"><span data-stu-id="c0c8b-172">Images</span></span>

<span data-ttu-id="c0c8b-173">Les types de fichiers suivants sont pris en charge par défaut pour les images :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-173">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="c0c8b-174">.jpg</span><span class="sxs-lookup"><span data-stu-id="c0c8b-174">.jpg</span></span>
- <span data-ttu-id="c0c8b-175">.png</span><span class="sxs-lookup"><span data-stu-id="c0c8b-175">.png</span></span>

### <a name="standard-conceptual-images-default-markdown"></a><span data-ttu-id="c0c8b-176">Images conceptuelles standard (Markdown par défaut)</span><span class="sxs-lookup"><span data-stu-id="c0c8b-176">Standard conceptual images (default Markdown)</span></span>

<span data-ttu-id="c0c8b-177">La syntaxe Markdown de base pour incorporer une image est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-177">The basic Markdown syntax to embed an image is:</span></span>

```Markdown
![<alt text>](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="c0c8b-178">Où `<alt text>` est une brève description de l’image et `<folder path>` un chemin relatif de l’image.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-178">Where `<alt text>` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="c0c8b-179">Un texte de remplacement est nécessaire pour les lecteurs d’écran des malvoyants.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-179">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="c0c8b-180">Ce texte est également utile si le site contient un bogue qui empêche l’affichage de l’image.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-180">It's also useful if there's a site bug where the image can't render.</span></span>

<span data-ttu-id="c0c8b-181">Les traits de soulignement dans le texte de remplacement ne sont pas affichés correctement à moins de les placer dans une séquence d’échappement en les faisant précéder d’une barre oblique inverse (`\_`).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-181">Underscores in alt text aren't rendered properly unless you escape them by prefixing them with a backslash (`\_`).</span></span> <span data-ttu-id="c0c8b-182">Toutefois, ne copiez pas de noms de fichiers à utiliser comme texte de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-182">However, don't copy file names for use as alt text.</span></span> <span data-ttu-id="c0c8b-183">Par exemple, au lieu de ceci :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-183">For example, instead of this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="c0c8b-184">Écrivez ceci :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-184">Write this:</span></span>

```markdown
![Active Directory extension for two-factor authentication, step 4: Configure](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="standard-conceptual-images-docs-markdown"></a><span data-ttu-id="c0c8b-185">Images conceptuelles standard (Docs Markdown)</span><span class="sxs-lookup"><span data-stu-id="c0c8b-185">Standard conceptual images (Docs Markdown)</span></span>

<span data-ttu-id="c0c8b-186">L’extension `:::image:::` personnalisée Docs prend en charge les images standard, les images complexes et les icônes.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-186">The Docs custom `:::image:::` extension supports standard images, complex images, and icons.</span></span>

<span data-ttu-id="c0c8b-187">Pour les images standard, la syntaxe Markdown plus ancienne continue de fonctionner, mais la nouvelle extension est recommandée, car elle prend en charge des fonctionnalités plus puissantes, telles que la spécification d’une étendue de localisation différente de la rubrique parente.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-187">For standard images, the older Markdown syntax will still work, but the new extension is recommended because it supports more powerful functionality, such as specifying a localization scope that's different from the parent topic.</span></span> <span data-ttu-id="c0c8b-188">D’autres fonctionnalités avancées, telles que la sélection dans la galerie d’images partagées au lieu de la spécification d’une image locale, seront disponibles à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-188">Other advanced functionality, such as selecting from the shared image gallery instead of specifying a local image, will be available in the future.</span></span> <span data-ttu-id="c0c8b-189">La nouvelle syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-189">The new syntax is as follows:</span></span>

```Markdown
:::image type="content" source="<folderPath>" alt-text="<alt text>":::
```

<span data-ttu-id="c0c8b-190">Si `type="content"` (par défaut), `source` et `alt-text` sont requis.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-190">If `type="content"` (the default), both `source` and `alt-text` are required.</span></span>

### <a name="complex-images-with-long-descriptions"></a><span data-ttu-id="c0c8b-191">Images complexes avec des descriptions longues</span><span class="sxs-lookup"><span data-stu-id="c0c8b-191">Complex images with long descriptions</span></span>

<span data-ttu-id="c0c8b-192">Vous pouvez également utiliser cette extension pour ajouter une image avec une description longue qui est lue par les lecteurs d’écran, mais qui n’est pas affichée visuellement sur la page publiée.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-192">You can also use this extension to add an image with a long description that is read by screen readers but not rendered visually on the published page.</span></span> <span data-ttu-id="c0c8b-193">Les descriptions longues sont une exigence d’accessibilité pour les images complexes, telles que les graphiques.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-193">Long descriptions are an accessibility requirement for complex images, such as graphs.</span></span> <span data-ttu-id="c0c8b-194">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-194">The syntax is the following:</span></span>

```Markdown
:::image type="complex" source="<folderPath>" alt-text="<alt text>":::
   <long description here>
:::image-end:::
```

<span data-ttu-id="c0c8b-195">Si `type="complex"`, `source`, `alt-text`, une description longue et la balise `:::image-end:::` sont tous obligatoires.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-195">If `type="complex"`, `source`, `alt-text`, a long description, and the `:::image-end:::` tag are all required.</span></span>

### <a name="specifying-loc-scope"></a><span data-ttu-id="c0c8b-196">Spécification de loc-scope</span><span class="sxs-lookup"><span data-stu-id="c0c8b-196">Specifying loc-scope</span></span>

<span data-ttu-id="c0c8b-197">Parfois, l’étendue de localisation d’une image est différente de celle de l’article ou du module qui la contient.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-197">Sometimes the localization scope for an image is different from that of the article or module that contains it.</span></span> <span data-ttu-id="c0c8b-198">Cela peut entraîner une mauvaise expérience globale, par exemple, si une capture d’écran d’un produit est accidentellement localisée dans une langue dans laquelle le produit n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-198">This can cause a bad global experience: for example, if a screenshot of a product is accidentally localized into a language the product isn't available in.</span></span> <span data-ttu-id="c0c8b-199">Pour éviter cela, vous pouvez spécifier l’attribut `loc-scope` facultatif dans les images de types `content` et `complex`.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-199">To prevent this, you can specify the optional `loc-scope` attribute in images of types `content` and `complex`.</span></span>

### <a name="icons"></a><span data-ttu-id="c0c8b-200">Icônes</span><span class="sxs-lookup"><span data-stu-id="c0c8b-200">Icons</span></span>

<span data-ttu-id="c0c8b-201">L’extension d’image prend en charge les icônes, qui sont des images décoratives et qui ne doivent pas comporter de texte de remplacement.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-201">The image extension supports icons, which are decorative images and should not have alt text.</span></span> <span data-ttu-id="c0c8b-202">La syntaxe des icônes est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-202">The syntax for icons is:</span></span>

```Markdown
:::image type="icon" source="<folderPath>":::
```

<span data-ttu-id="c0c8b-203">Si `type="icon"`, seul `source` doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-203">If `type="icon"`, only `source` should be specified.</span></span>

## <a name="included-markdown-files"></a><span data-ttu-id="c0c8b-204">Fichiers Markdown inclus</span><span class="sxs-lookup"><span data-stu-id="c0c8b-204">Included Markdown files</span></span>

<span data-ttu-id="c0c8b-205">Quand des fichiers Markdown doivent être répétés dans plusieurs articles, vous pouvez utiliser un fichier include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-205">Where markdown files need to be repeated in multiple articles, you can use an include file.</span></span> <span data-ttu-id="c0c8b-206">La fonctionnalité d’includes indique à Docs de remplacer la référence par le contenu du fichier include au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-206">The includes feature instructs Docs to replace the reference with the contents of the include file at build time.</span></span> <span data-ttu-id="c0c8b-207">Vous pouvez utiliser des includes de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-207">You can use includes in the following ways:</span></span>

- <span data-ttu-id="c0c8b-208">Inline : pour réutiliser un extrait de texte commun au sein d’une phrase.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-208">Inline: Reuse a common text snippet inline with within a sentence.</span></span>
- <span data-ttu-id="c0c8b-209">Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-209">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>

<span data-ttu-id="c0c8b-210">Un fichier include de type inline ou bloc est un fichier Markdown (.md).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-210">An inline or block include file is a Markdown (.md) file.</span></span> <span data-ttu-id="c0c8b-211">Il peut contenir tout code Markdown valide.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-211">It can contain any valid Markdown.</span></span> <span data-ttu-id="c0c8b-212">Les fichiers include se trouvent généralement dans un sous-répertoire *includes* commun, à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-212">Include files are typically located in a common *includes* subdirectory, in the root of the repository.</span></span> <span data-ttu-id="c0c8b-213">Quand l’article est publié, le fichier inclus y est intégré de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-213">When the article is published, the included file is seamlessly integrated into it.</span></span>

### <a name="includes-syntax"></a><span data-ttu-id="c0c8b-214">Syntaxe des includes</span><span class="sxs-lookup"><span data-stu-id="c0c8b-214">Includes syntax</span></span>

<span data-ttu-id="c0c8b-215">Un include sous forme de bloc occupe une ligne à part :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-215">Block include is on its own line:</span></span>

```markdown
[!INCLUDE [<title>](<filepath>)]
```

<span data-ttu-id="c0c8b-216">Un include inline se trouve à l’intérieur d’une ligne :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-216">Inline include is within a line:</span></span>

```markdown
Text before [!INCLUDE [<title>](<filepath>)] and after.
```

<span data-ttu-id="c0c8b-217">Où `<title>` est le nom du fichier et `<filepath>` le chemin relatif du fichier.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-217">Where `<title>` is the name of the file and `<filepath>` is the relative path to the file.</span></span> <span data-ttu-id="c0c8b-218">`INCLUDE` doit être en majuscule et un espace doit figurer avant `<title>`.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-218">`INCLUDE` must be capitalized and there must be a space before the `<title>`.</span></span>

<span data-ttu-id="c0c8b-219">Voici les conditions requises et éléments à prendre en compte pour les fichiers include :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-219">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="c0c8b-220">Utilisez des includes de blocs pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-220">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="c0c8b-221">Ne l'utilisez pas pour des éléments plus petits qu'une phrase.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-221">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="c0c8b-222">Les includes ne s’afficheront pas dans la vue de votre article rendu par GitHub, car ils reposent sur des extensions Docs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-222">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Docs extensions.</span></span> <span data-ttu-id="c0c8b-223">Ils ne sont rendus qu’après publication.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-223">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="c0c8b-224">Vérifiez que tout le texte dans un fichier include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence l’include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-224">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="c0c8b-225">Le fait d’ignorer cette instruction crée une chaîne intraduisible dans l’article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-225">Ignoring this guidance creates an untranslatable string in the article.</span></span>
- <span data-ttu-id="c0c8b-226">N’incorporez pas de fichiers include dans d’autres fichiers include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-226">Don't embed include files within other include files.</span></span>
- <span data-ttu-id="c0c8b-227">Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>` */includes/media*.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-227">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`*/includes/media* folder.</span></span> <span data-ttu-id="c0c8b-228">Le répertoire *media* ne doit pas contenir d’images à sa racine.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-228">The *media* directory should not contain any images in its root.</span></span> <span data-ttu-id="c0c8b-229">Si l’include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire *media* correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-229">If the include does not have images, a corresponding *media* directory is not required.</span></span>
- <span data-ttu-id="c0c8b-230">Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-230">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="c0c8b-231">Utilisez un fichier distinct avec un nom unique pour chaque include et article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-231">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="c0c8b-232">Stockez le fichier multimédia dans le dossier multimédia associé à l’include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-232">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="c0c8b-233">N'utilisez pas un include comme seul contenu d'un article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-233">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="c0c8b-234">Les includes sont censés compléter le contenu du reste de l'article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-234">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

## <a name="links"></a><span data-ttu-id="c0c8b-235">Liens</span><span class="sxs-lookup"><span data-stu-id="c0c8b-235">Links</span></span>

<span data-ttu-id="c0c8b-236">Pour plus d’informations sur la syntaxe des liens, consultez [Utiliser des liens dans la documentation](how-to-write-links.md).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-236">For information on syntax for links, see [Use links in documentation](how-to-write-links.md).</span></span>

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="c0c8b-237">Listes (numérotées, à puces, liste de contrôle)</span><span class="sxs-lookup"><span data-stu-id="c0c8b-237">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="c0c8b-238">Liste numérotée</span><span class="sxs-lookup"><span data-stu-id="c0c8b-238">Numbered list</span></span>

<span data-ttu-id="c0c8b-239">Pour créer une liste numérotée, vous pouvez utiliser uniquement des 1.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-239">To create a numbered list, you can use all 1s.</span></span> <span data-ttu-id="c0c8b-240">Les nombres sont affichés dans l’ordre croissant sous la forme d’une liste séquentielle au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-240">The numbers are rendered in ascending order as a sequential list when published.</span></span> <span data-ttu-id="c0c8b-241">Pour accroître la lisibilité du texte source, vous pouvez incrémenter vos listes manuellement.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-241">For increased source readability, you can increment your lists manually.</span></span>

<span data-ttu-id="c0c8b-242">N’utilisez pas de lettres dans les listes, y compris dans les listes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-242">Don't use letters in lists, including nested lists.</span></span> <span data-ttu-id="c0c8b-243">Elles ne sont pas restituées correctement au moment de la publication sur Docs. Les listes imbriquées utilisant des nombres sont restituées avec des lettres minuscules au moment de la publication.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-243">They don't render correctly when published to Docs. Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="c0c8b-244">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-244">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="c0c8b-245">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-245">This renders as follows:</span></span>

1. <span data-ttu-id="c0c8b-246">This is</span><span class="sxs-lookup"><span data-stu-id="c0c8b-246">This is</span></span>
1. <span data-ttu-id="c0c8b-247">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="c0c8b-247">a parent numbered list</span></span>
   1. <span data-ttu-id="c0c8b-248">and this is</span><span class="sxs-lookup"><span data-stu-id="c0c8b-248">and this is</span></span>
   1. <span data-ttu-id="c0c8b-249">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="c0c8b-249">a nested numbered list</span></span>
1. <span data-ttu-id="c0c8b-250">(fin)</span><span class="sxs-lookup"><span data-stu-id="c0c8b-250">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="c0c8b-251">Liste à puces</span><span class="sxs-lookup"><span data-stu-id="c0c8b-251">Bulleted list</span></span>

<span data-ttu-id="c0c8b-252">Pour créer une liste à puces, utilisez `-` ou `*` suivi d’un espace au début de chaque ligne :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-252">To create a bulleted list, use `-` or `*` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="c0c8b-253">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-253">This renders as follows:</span></span>

- <span data-ttu-id="c0c8b-254">This is</span><span class="sxs-lookup"><span data-stu-id="c0c8b-254">This is</span></span>
- <span data-ttu-id="c0c8b-255">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="c0c8b-255">a parent bulleted list</span></span>
  - <span data-ttu-id="c0c8b-256">and this is</span><span class="sxs-lookup"><span data-stu-id="c0c8b-256">and this is</span></span>
  - <span data-ttu-id="c0c8b-257">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="c0c8b-257">a nested bulleted list</span></span>
- <span data-ttu-id="c0c8b-258">All done!</span><span class="sxs-lookup"><span data-stu-id="c0c8b-258">All done!</span></span>

<span data-ttu-id="c0c8b-259">Quelle que soit la syntaxe que vous utilisez, `-` ou `*`, utilisez-la de manière cohérente dans un article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-259">Whichever syntax you use, `-` or `*`, use it consistently within an article.</span></span>

### <a name="checklist"></a><span data-ttu-id="c0c8b-260">Liste de contrôle</span><span class="sxs-lookup"><span data-stu-id="c0c8b-260">Checklist</span></span>

<span data-ttu-id="c0c8b-261">Les listes de contrôle sont utilisables sur Docs par le biais d’une extension Markdown personnalisée :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-261">Checklists are available for use on Docs via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="c0c8b-262">Cet exemple s’affiche sur Docs ainsi :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-262">This example renders on Docs like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c0c8b-263">List item 1</span><span class="sxs-lookup"><span data-stu-id="c0c8b-263">List item 1</span></span>
> * <span data-ttu-id="c0c8b-264">List item 2</span><span class="sxs-lookup"><span data-stu-id="c0c8b-264">List item 2</span></span>
> * <span data-ttu-id="c0c8b-265">List item 3</span><span class="sxs-lookup"><span data-stu-id="c0c8b-265">List item 3</span></span>

<span data-ttu-id="c0c8b-266">Utilisez des listes de contrôle au début ou à la fin d’un article pour récapituler le contenu que l’utilisateur va étudier ou a étudié.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-266">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="c0c8b-267">N’ajoutez pas de listes de contrôle aléatoires dans vos articles.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-267">Do not add random checklists throughout your articles.</span></span>

## <a name="next-step-action"></a><span data-ttu-id="c0c8b-268">Action d’étape suivante</span><span class="sxs-lookup"><span data-stu-id="c0c8b-268">Next step action</span></span>

<span data-ttu-id="c0c8b-269">Vous pouvez utiliser une extension personnalisée pour ajouter un bouton d’action d’étape suivante à des pages Docs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-269">You can use a custom extension to add a next step action button to Docs pages.</span></span>

<span data-ttu-id="c0c8b-270">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-270">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="c0c8b-271">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-271">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about adding code to articles](code-in-docs.md)
```

<span data-ttu-id="c0c8b-272">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-272">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="c0c8b-273">Learn about adding code to articles</span><span class="sxs-lookup"><span data-stu-id="c0c8b-273">Learn about adding code to articles</span></span>](code-in-docs.md)

<span data-ttu-id="c0c8b-274">Vous pouvez utiliser n’importe quel lien pris en charge dans une action d’étape suivante, y compris un lien Markdown vers une autre page web.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-274">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="c0c8b-275">Dans la plupart des cas, le lien d’action suivante est un lien relatif vers un autre fichier de le même docset.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-275">In most cases, the next action link will be a relative link to another file in the same docset.</span></span>

## <a name="non-localized-strings"></a><span data-ttu-id="c0c8b-276">Chaînes non localisées</span><span class="sxs-lookup"><span data-stu-id="c0c8b-276">Non-localized strings</span></span>

<span data-ttu-id="c0c8b-277">Vous pouvez utiliser l’extension Markdown `no-loc` personnalisée pour identifier les chaînes de contenu que le processus de localisation doit ignorer.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-277">You can use the custom `no-loc` Markdown extension to identify strings of content that you would like the localization process to ignore.</span></span>

<span data-ttu-id="c0c8b-278">Toutes les chaînes appelées sont sensibles à la casse ; autrement dit, une chaîne doit correspondre exactement pour être ignorée au moment de la localisation.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-278">All strings called out will be case-sensitive; that is, the string must match exactly to be ignored for localization.</span></span>

<span data-ttu-id="c0c8b-279">Pour marquer une chaîne individuelle comme non localisable, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-279">To mark an individual string as non-localizable, use this syntax:</span></span>

```markdown
:::no-loc text="String":::
```

<span data-ttu-id="c0c8b-280">Par exemple, dans le code suivant, seule l’instance unique de `Document` est ignorée au cours du processus de localisation :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-280">For example, in the following, only the single instance of `Document` will be ignored during the localization process:</span></span>

```markdown
# Heading 1 of the Document

Markdown content within the :::no-loc text="Document":::.  The are multiple instances of Document, document, and documents.
```

> [!NOTE]
> <span data-ttu-id="c0c8b-281">Utilisez `\` pour placer les caractères spéciaux dans une séquence d’échappement:</span><span class="sxs-lookup"><span data-stu-id="c0c8b-281">Use `\` to escape special characters:</span></span>
> ```markdown
> Lorem :::no-loc text="Find a \"Quotation\""::: Ipsum.
> ```

<span data-ttu-id="c0c8b-282">Vous pouvez également utiliser des métadonnées dans l’en-tête YAML pour marquer toutes les instances d’une chaîne dans le fichier Markdown actuel comme non localisables :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-282">You can also use metadata in the YAML header to mark all instances of a string within the current Markdown file as non-localizable:</span></span>

```yml
author: cillroy
no-loc: [Global, Strings, to be, Ignored]
```

> [!NOTE]
> <span data-ttu-id="c0c8b-283">Les métadonnées no-loc ne sont pas prises en charge en tant que métadonnées globales dans le fichier *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-283">The no-loc metadata is not supported as global metadata in *docfx.json* file.</span></span> <span data-ttu-id="c0c8b-284">Le pipeline de localisation ne lit pas le fichier *docfx.json*. Ainsi, les métadonnées no-loc doivent être ajoutées à chaque fichier source individuel.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-284">The localization pipeline doesn't read the *docfx.json* file, so the no-loc metadata must be added into each individual source file.</span></span>

<span data-ttu-id="c0c8b-285">Dans l’exemple suivant, à la fois dans la métadonnée `title` et dans l’en-tête Markdown, le mot `Document` est ignoré au cours du processus de localisation.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-285">In the following example, both in the metadata `title` and the Markdown header the word `Document` will be ignored during the localization process.</span></span>

<span data-ttu-id="c0c8b-286">Dans la métadonnée `description` et le contenu principal de Markdown, le mot `document` est localisé, car il ne commence pas par un `D` majuscule.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-286">In the metadata `description` and the Markdown main content the word `document` is localized, because it does not start with a capital `D`.</span></span>

```markdown
---
title: Title of the Document
author: author-name
description: Description for the document
no-loc: [Title, Document]
---
# Heading 1 of the Document

Markdown content within the document.
```

<!-- commenting out for now because no one knows what this means
## Section definition

You might need to define a section. This syntax is mostly used for code tables.
See the following example:

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

The preceding blockquote Markdown text will be rendered as:
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
-->

## <a name="selectors"></a><span data-ttu-id="c0c8b-287">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="c0c8b-287">Selectors</span></span>

<span data-ttu-id="c0c8b-288">Les sélecteurs sont des éléments d’interface utilisateur qui permettent à l’utilisateur de basculer entre plusieurs versions du même article.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-288">Selectors are UI elements that let the user switch between multiple flavors of the same article.</span></span> <span data-ttu-id="c0c8b-289">Ils sont utilisés dans certains docsets pour résoudre les différences d’implémentation entre les technologies et les plateformes.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-289">They are used in some doc sets to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="c0c8b-290">Les sélecteurs s’appliquent particulièrement au contenu pour plateformes mobiles pour développeurs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-290">Selectors are typically most applicable to our mobile platform content for developers.</span></span>

<span data-ttu-id="c0c8b-291">Le même Markdown de sélecteur allant dans chaque fichier d’article qui utilise le sélecteur, nous vous recommandons de placer le sélecteur pour votre article dans un fichier include.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-291">Because the same selector Markdown goes in each article file that uses the selector, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="c0c8b-292">Vous pouvez ensuite référencer ce dernier dans tous vos fichiers d’article qui utilisent le même sélecteur.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-292">Then you can reference that include file in all your article files that use the same selector.</span></span>

<span data-ttu-id="c0c8b-293">Il existe deux types de sélecteurs : sélecteur unique et sélecteur multiple.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-293">There are two types of selectors: a single selector and a multi-selector.</span></span>

### <a name="single-selector"></a><span data-ttu-id="c0c8b-294">Sélecteur unique</span><span class="sxs-lookup"><span data-stu-id="c0c8b-294">Single selector</span></span>

```markdown
> [!div class="op_single_selector"]
> - [Universal Windows](../articles/notification-hubs-windows-store-dotnet-get-started/)
> - [Windows Phone](../articles/notification-hubs-windows-phone-get-started/)
> - [iOS](../articles/notification-hubs-ios-get-started/)
> - [Android](../articles/notification-hubs-android-get-started/)
> - [Kindle](../articles/notification-hubs-kindle-get-started/)
> - [Baidu](../articles/notification-hubs-baidu-get-started/)
> - [Xamarin.iOS](../articles/partner-xamarin-notification-hubs-ios-get-started/)
> - [Xamarin.Android](../articles/partner-xamarin-notification-hubs-android-get-started/)
```

<span data-ttu-id="c0c8b-295">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-295">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Windows universel](how-to-write-links.md)
> - [Windows Phone](how-to-write-links.md)
> - [iOS](how-to-write-links.md)
> - [Android](how-to-write-links.md)
> - [Kindle](how-to-write-links.md)
> - [Baidu](how-to-write-links.md)
> - [Xamarin.iOS](how-to-write-links.md)
> - [Xamarin.Android](how-to-write-links.md)

### <a name="multi-selector"></a><span data-ttu-id="c0c8b-304">Sélecteur multiple</span><span class="sxs-lookup"><span data-stu-id="c0c8b-304">Multi-selector</span></span>

```markdown
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](./mobile-services-dotnet-backend-ios-get-started-push.md)
> - [(iOS | JavaScript)](./mobile-services-javascript-backend-ios-get-started-push.md)
> - [(Windows universal C# | .NET)](./mobile-services-dotnet-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows universal C# | Javascript)](./mobile-services-javascript-backend-windows-universal-dotnet-get-started-push.md)
> - [(Windows Phone | .NET)](./mobile-services-dotnet-backend-windows-phone-get-started-push.md)
> - [(Windows Phone | Javascript)](./mobile-services-javascript-backend-windows-phone-get-started-push.md)
> - [(Android | .NET)](./mobile-services-dotnet-backend-android-get-started-push.md)
> - [(Android | Javascript)](./mobile-services-javascript-backend-android-get-started-push.md)
> - [(Xamarin iOS | Javascript)](./partner-xamarin-mobile-services-ios-get-started-push.md)
> - [(Xamarin Android | Javascript)](./partner-xamarin-mobile-services-android-get-started-push.md)
```

<span data-ttu-id="c0c8b-305">... s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-305">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Plateforme" title2="Back-end"]
> - [(iOS | .NET)](how-to-write-links.md)
> - [(iOS | JavaScript)](how-to-write-links.md)
> - [(Windows universel C# | .NET)](how-to-write-links.md)
> - [(Windows universel C# | Javascript)](how-to-write-links.md)
> - [(Windows Phone | .NET)](how-to-write-links.md)
> - [(Windows Phone | Javascript)](how-to-write-links.md)
> - [(Android | .NET)](how-to-write-links.md)
> - [(Android | Javascript)](how-to-write-links.md)
> - [(Xamarin iOS | Javascript)](how-to-write-links.md)
> - [(Xamarin Android | Javascript)](how-to-write-links.md)

## <a name="subscript-and-superscript"></a><span data-ttu-id="c0c8b-318">Indice et exposant</span><span class="sxs-lookup"><span data-stu-id="c0c8b-318">Subscript and superscript</span></span>

<span data-ttu-id="c0c8b-319">Vous devez uniquement utiliser un indice ou un exposant quand cela est nécessaire pour une précision technique, par exemple lors de l’écriture de formules mathématiques.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-319">You should only use subscript or superscript when necessary for technical accuracy, such as when writing about mathematical formulas.</span></span> <span data-ttu-id="c0c8b-320">Ne les utilisez pas pour les styles non standard, tels que les notes de bas de page.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-320">Don't use them for non-standard styles, such as footnotes.</span></span>

<span data-ttu-id="c0c8b-321">Pour exprimer du contenu sous forme d’indice ou d’exposant, utilisez HTML :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-321">For both subscript and superscript, use HTML:</span></span>

```html
Hello <sub>This is subscript!</sub>
```

<span data-ttu-id="c0c8b-322">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-322">This renders as follows:</span></span>

<span data-ttu-id="c0c8b-323">Hello <sub>This is subscript!</sub></span><span class="sxs-lookup"><span data-stu-id="c0c8b-323">Hello <sub>This is subscript!</sub></span></span>

```html
Goodbye <sup>This is superscript!</sup>
```

<span data-ttu-id="c0c8b-324">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-324">This renders as follows:</span></span>

<span data-ttu-id="c0c8b-325">Goodbye <sup>This is superscript!</sup></span><span class="sxs-lookup"><span data-stu-id="c0c8b-325">Goodbye <sup>This is superscript!</sup></span></span>

## <a name="tables"></a><span data-ttu-id="c0c8b-326">Les tableaux</span><span class="sxs-lookup"><span data-stu-id="c0c8b-326">Tables</span></span>

<span data-ttu-id="c0c8b-327">Le moyen le plus simple de créer un tableau en Markdown est d’utiliser des barres verticales et des lignes.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-327">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="c0c8b-328">Pour créer un tableau standard avec un en-tête, faites suivre la première ligne d’une ligne en pointillés :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-328">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="c0c8b-329">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-329">This renders as follows:</span></span>

|<span data-ttu-id="c0c8b-330">This is</span><span class="sxs-lookup"><span data-stu-id="c0c8b-330">This is</span></span>   |<span data-ttu-id="c0c8b-331">a simple</span><span class="sxs-lookup"><span data-stu-id="c0c8b-331">a simple</span></span>   |<span data-ttu-id="c0c8b-332">table header</span><span class="sxs-lookup"><span data-stu-id="c0c8b-332">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="c0c8b-333">table</span><span class="sxs-lookup"><span data-stu-id="c0c8b-333">table</span></span>     |<span data-ttu-id="c0c8b-334">data</span><span class="sxs-lookup"><span data-stu-id="c0c8b-334">data</span></span>       |<span data-ttu-id="c0c8b-335">here</span><span class="sxs-lookup"><span data-stu-id="c0c8b-335">here</span></span>        |
|<span data-ttu-id="c0c8b-336">it doesn't</span><span class="sxs-lookup"><span data-stu-id="c0c8b-336">it doesn't</span></span>|<span data-ttu-id="c0c8b-337">actually</span><span class="sxs-lookup"><span data-stu-id="c0c8b-337">actually</span></span>   |<span data-ttu-id="c0c8b-338">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="c0c8b-338">have to line up nicely!</span></span>||

<span data-ttu-id="c0c8b-339">Vous pouvez aligner les colonnes à l’aide de signes deux-points :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-339">You can align the columns by using colons:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="c0c8b-340">Ce code est restitué comme suit :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-340">Renders as follows:</span></span>

| <span data-ttu-id="c0c8b-341">Fun</span><span class="sxs-lookup"><span data-stu-id="c0c8b-341">Fun</span></span>                  | <span data-ttu-id="c0c8b-342">With</span><span class="sxs-lookup"><span data-stu-id="c0c8b-342">With</span></span>                 | <span data-ttu-id="c0c8b-343">Les tableaux</span><span class="sxs-lookup"><span data-stu-id="c0c8b-343">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="c0c8b-344">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="c0c8b-344">left-aligned column</span></span>  | <span data-ttu-id="c0c8b-345">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="c0c8b-345">right-aligned column</span></span> | <span data-ttu-id="c0c8b-346">centered column</span><span class="sxs-lookup"><span data-stu-id="c0c8b-346">centered column</span></span> |
| <span data-ttu-id="c0c8b-347">$100</span><span class="sxs-lookup"><span data-stu-id="c0c8b-347">$100</span></span>                 | <span data-ttu-id="c0c8b-348">$100</span><span class="sxs-lookup"><span data-stu-id="c0c8b-348">$100</span></span>                 | <span data-ttu-id="c0c8b-349">$100</span><span class="sxs-lookup"><span data-stu-id="c0c8b-349">$100</span></span>            |
| <span data-ttu-id="c0c8b-350">$10</span><span class="sxs-lookup"><span data-stu-id="c0c8b-350">$10</span></span>                  | <span data-ttu-id="c0c8b-351">$10</span><span class="sxs-lookup"><span data-stu-id="c0c8b-351">$10</span></span>                  | <span data-ttu-id="c0c8b-352">$10</span><span class="sxs-lookup"><span data-stu-id="c0c8b-352">$10</span></span>             |
| <span data-ttu-id="c0c8b-353">$1</span><span class="sxs-lookup"><span data-stu-id="c0c8b-353">$1</span></span>                   | <span data-ttu-id="c0c8b-354">$1</span><span class="sxs-lookup"><span data-stu-id="c0c8b-354">$1</span></span>                   | <span data-ttu-id="c0c8b-355">$1</span><span class="sxs-lookup"><span data-stu-id="c0c8b-355">$1</span></span>              |

> [!TIP]
> <span data-ttu-id="c0c8b-356">L’extension Docs Authoring pour VS Code facilite l’ajout de tableaux Markdown simples !</span><span class="sxs-lookup"><span data-stu-id="c0c8b-356">The Docs Authoring Extension for VS Code makes it easy to add basic Markdown tables!</span></span>
>
> <span data-ttu-id="c0c8b-357">Vous pouvez également utiliser un [ générateur de tableau en ligne](http://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="c0c8b-357">You can also use an [online table generator](http://www.tablesgenerator.com/markdown_tables).</span></span>

### <a name="line-breaks-within-words-in-any-table-cell"></a><span data-ttu-id="c0c8b-358">Sauts de ligne dans les mots d’une cellule de tableau</span><span class="sxs-lookup"><span data-stu-id="c0c8b-358">Line breaks within words in any table cell</span></span>

<span data-ttu-id="c0c8b-359">Les mots longs dans un tableau Markdown peuvent amener ce dernier à s’étendre sur la barre de navigation de droite au point de devenir illisible.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-359">Long words in a Markdown table might make the table expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="c0c8b-360">Vous pouvez résoudre cela en autorisant le rendu Docs à insérer automatiquement des sauts de ligne dans les mots, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-360">You can solve that by allowing Docs rendering to automatically insert line breaks within words when needed.</span></span> <span data-ttu-id="c0c8b-361">Pour cela, il vous suffit d’encapsuler le tableau avec la classe personnalisée `[!div class="mx-tdBreakAll"]`.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-361">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="c0c8b-362">Voici un exemple de code Markdown d’un tableau, avec trois lignes encapsulées par un `div`, avec le nom de classe `mx-tdBreakAll`.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-362">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="c0c8b-363">Cela s’affiche ainsi :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-363">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="c0c8b-364">Name</span><span class="sxs-lookup"><span data-stu-id="c0c8b-364">Name</span></span>|<span data-ttu-id="c0c8b-365">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0c8b-365">Syntax</span></span>|<span data-ttu-id="c0c8b-366">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="c0c8b-366">Mandatory for silent installation?</span></span>|<span data-ttu-id="c0c8b-367">Description</span><span class="sxs-lookup"><span data-stu-id="c0c8b-367">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="c0c8b-368">Quiet</span><span class="sxs-lookup"><span data-stu-id="c0c8b-368">Quiet</span></span>|<span data-ttu-id="c0c8b-369">/quiet</span><span class="sxs-lookup"><span data-stu-id="c0c8b-369">/quiet</span></span>|<span data-ttu-id="c0c8b-370">Yes</span><span class="sxs-lookup"><span data-stu-id="c0c8b-370">Yes</span></span>|<span data-ttu-id="c0c8b-371">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-371">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="c0c8b-372">NoRestart</span><span class="sxs-lookup"><span data-stu-id="c0c8b-372">NoRestart</span></span>|<span data-ttu-id="c0c8b-373">/norestart</span><span class="sxs-lookup"><span data-stu-id="c0c8b-373">/norestart</span></span>|<span data-ttu-id="c0c8b-374">No</span><span class="sxs-lookup"><span data-stu-id="c0c8b-374">No</span></span>|<span data-ttu-id="c0c8b-375">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-375">Suppresses any attempts to restart.</span></span> <span data-ttu-id="c0c8b-376">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-376">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="c0c8b-377">Help</span><span class="sxs-lookup"><span data-stu-id="c0c8b-377">Help</span></span>|<span data-ttu-id="c0c8b-378">/help</span><span class="sxs-lookup"><span data-stu-id="c0c8b-378">/help</span></span>|<span data-ttu-id="c0c8b-379">No</span><span class="sxs-lookup"><span data-stu-id="c0c8b-379">No</span></span>|<span data-ttu-id="c0c8b-380">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-380">Provides help and quick reference.</span></span> <span data-ttu-id="c0c8b-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-381">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="line-breaks-within-words-in-second-column-table-cells"></a><span data-ttu-id="c0c8b-382">Sauts de ligne dans les mots au sein des cellules de la deuxième colonne d’un tableau</span><span class="sxs-lookup"><span data-stu-id="c0c8b-382">Line breaks within words in second column table cells</span></span>

<span data-ttu-id="c0c8b-383">Vous souhaiterez peut-être insérer automatiquement des sauts de ligne dans les mots de la deuxième colonne d’un tableau uniquement.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-383">You might want line breaks to be automatically inserted within words only in the second column of a table.</span></span> <span data-ttu-id="c0c8b-384">Pour limiter les arrêts à la deuxième colonne, appliquez la classe `mx-tdCol2BreakAll` à l’aide de la syntaxe de wrapper `div`, comme indiqué plus haut.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-384">To limit the breaks to the second column, apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="data-matrix-tables"></a><span data-ttu-id="c0c8b-385">Tables de matrices de données</span><span class="sxs-lookup"><span data-stu-id="c0c8b-385">Data matrix tables</span></span>

<span data-ttu-id="c0c8b-386">Une table de matrice de données contient une en-tête et une première colonne pondérée. Une matrice avec une cellule vide est créée en haut à gauche.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-386">A data matrix table has both a header and a weighted first column, creating a matrix with an empty cell in the top left.</span></span> <span data-ttu-id="c0c8b-387">Docs contient Markdown personnalisé pour les tables de la matrice de données :</span><span class="sxs-lookup"><span data-stu-id="c0c8b-387">Docs has custom Markdown for data matrix tables:</span></span>

```md
|                  |Header 1 |Header 2|
|------------------|---------|--------|
|**First column A**|Cell 1A  |Cell 2A |
|**First column B**|Cell 1B  |Cell 2B |
```

<span data-ttu-id="c0c8b-388">Chaque entrée de la première colonne doit avoir le style gras (`**bold**`) ; sinon, les tables ne sont pas accessibles pour les lecteurs d’écran ou ne sont pas valides pour Docs.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-388">Every entry in the first column must be styled as bold (`**bold**`); otherwise the tables won't be accessible for screen readers or valid for Docs.</span></span>

### <a name="html-tables"></a><span data-ttu-id="c0c8b-389">Tableaux HTML</span><span class="sxs-lookup"><span data-stu-id="c0c8b-389">HTML Tables</span></span>

<span data-ttu-id="c0c8b-390">Les tableaux HTML ne sont pas recommandés dans docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-390">HTML tables aren't recommended for docs.microsoft.com.</span></span> <span data-ttu-id="c0c8b-391">Ils ne se présentent pas sous une forme conviviale dans le source, ce qui va à l’encontre d’un principe essentiel de Markdown.</span><span class="sxs-lookup"><span data-stu-id="c0c8b-391">They aren't human readable in the source - which is a key principle of Markdown.</span></span>
