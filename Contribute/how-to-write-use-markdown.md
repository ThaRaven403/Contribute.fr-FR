---
title: Guide pratique pour utiliser Markdown pour écrire du contenu Docs
description: Cet article fournit des informations de base et de référence sur le langage Markdown utilisé pour écrire des articles docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/26/2019
ms.openlocfilehash: ffc44f07929890ef17b3878ba389dfeea82691a6
ms.sourcegitcommit: 254c804bb0b451c262745fe8d87e2e8f9196440c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2019
ms.locfileid: "73592461"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="f704b-103">Guide pratique pour utiliser Markdown pour écrire du contenu Docs</span><span class="sxs-lookup"><span data-stu-id="f704b-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="f704b-104">Les articles [docs.microsoft.com](https://docs.microsoft.com) sont écrits dans un langage de balisage léger appelé [Markdown](https://daringfireball.net/projects/markdown/), à la fois facile à lire et facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="f704b-104">[Docs.microsoft.com](https://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="f704b-105">Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur.</span><span class="sxs-lookup"><span data-stu-id="f704b-105">Because of this, it has quickly become an industry standard.</span></span> <span data-ttu-id="f704b-106">Le site docs utilise le [type Markdig](#markdown-flavor) de Markdown.</span><span class="sxs-lookup"><span data-stu-id="f704b-106">The docs site uses the [Markdig flavor](#markdown-flavor) of Markdown.</span></span>


## <a name="markdown-basics"></a><span data-ttu-id="f704b-107">Les bases de Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-107">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="f704b-108">En-têtes</span><span class="sxs-lookup"><span data-stu-id="f704b-108">Headings</span></span>

<span data-ttu-id="f704b-109">Pour créer un en-tête, vous utilisez un dièse (#), comme suit :</span><span class="sxs-lookup"><span data-stu-id="f704b-109">To create a heading, you use a hash mark (#), as follows:</span></span>

```md
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="f704b-110">Les en-têtes doivent être de style atx, autrement dit vous devez placer de 1 à 6 caractères dièse (#) au début de la ligne pour indiquer qu’il s’agit d’un en-tête, correspondant aux niveaux d’en-têtes HTML H1 à H6.</span><span class="sxs-lookup"><span data-stu-id="f704b-110">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="f704b-111">Des exemples d’en-têtes du premier au quatrième niveau sont utilisés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f704b-111">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="f704b-112">Il ne doit y avoir qu’**un seul** en-tête de premier niveau dans votre rubrique, qui sera affiché comme titre de page.</span><span class="sxs-lookup"><span data-stu-id="f704b-112">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="f704b-113">Si votre en-tête se termine par un caractère `#`, vous devez ajouter un caractère `#` supplémentaire à la fin pour que le titre soit affiché correctement.</span><span class="sxs-lookup"><span data-stu-id="f704b-113">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="f704b-114">Par exemple, `# Async Programming in F# #`.</span><span class="sxs-lookup"><span data-stu-id="f704b-114">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="f704b-115">Les en-têtes de second niveau génèreront la table des matières de la page affichée dans la section « Dans cet article » sous le titre de page.</span><span class="sxs-lookup"><span data-stu-id="f704b-115">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="f704b-116">Texte en gras et italique</span><span class="sxs-lookup"><span data-stu-id="f704b-116">Bold and italic text</span></span>

<span data-ttu-id="f704b-117">Pour formater le texte en **gras**, vous l’entourez de deux astérisques :</span><span class="sxs-lookup"><span data-stu-id="f704b-117">To format text as **bold**, you enclose it in two asterisks:</span></span>

```md
This text is **bold**.
```

<span data-ttu-id="f704b-118">Pour formater le texte en *italique*, vous l’entourez d’un seul astérisque :</span><span class="sxs-lookup"><span data-stu-id="f704b-118">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```md
This text is *italic*.
```

<span data-ttu-id="f704b-119">Pour formater le texte en ***gras et en italique***, vous l’entourez de trois astérisques :</span><span class="sxs-lookup"><span data-stu-id="f704b-119">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```md
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="f704b-120">Éléments blockquote</span><span class="sxs-lookup"><span data-stu-id="f704b-120">Blockquotes</span></span>

<span data-ttu-id="f704b-121">Pour créer un élément blockquote, vous utilisez le caractère `>` :</span><span class="sxs-lookup"><span data-stu-id="f704b-121">Blockquotes are created using the `>` character:</span></span>

```md
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="f704b-122">L’exemple précédent s’affiche comme suit :</span><span class="sxs-lookup"><span data-stu-id="f704b-122">The preceding example renders as follows:</span></span>

> <span data-ttu-id="f704b-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="f704b-123">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="f704b-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="f704b-124">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="f704b-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="f704b-125">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="f704b-126">Listes</span><span class="sxs-lookup"><span data-stu-id="f704b-126">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="f704b-127">Liste non ordonnée</span><span class="sxs-lookup"><span data-stu-id="f704b-127">Unordered list</span></span>

<span data-ttu-id="f704b-128">Pour formater une liste à puces/non ordonnée, vous pouvez utiliser des astérisques ou des tirets.</span><span class="sxs-lookup"><span data-stu-id="f704b-128">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="f704b-129">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="f704b-129">For example, the following Markdown:</span></span>

```md
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="f704b-130">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="f704b-130">will be rendered as:</span></span>

- <span data-ttu-id="f704b-131">List item 1</span><span class="sxs-lookup"><span data-stu-id="f704b-131">List item 1</span></span>
- <span data-ttu-id="f704b-132">List item 2</span><span class="sxs-lookup"><span data-stu-id="f704b-132">List item 2</span></span>
- <span data-ttu-id="f704b-133">List item 3</span><span class="sxs-lookup"><span data-stu-id="f704b-133">List item 3</span></span>

<span data-ttu-id="f704b-134">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="f704b-134">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f704b-135">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="f704b-135">For example, the following Markdown:</span></span>

```md
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="f704b-136">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="f704b-136">will be rendered as:</span></span>

- <span data-ttu-id="f704b-137">List item 1</span><span class="sxs-lookup"><span data-stu-id="f704b-137">List item 1</span></span>
  - <span data-ttu-id="f704b-138">List item A</span><span class="sxs-lookup"><span data-stu-id="f704b-138">List item A</span></span>
  - <span data-ttu-id="f704b-139">List item B</span><span class="sxs-lookup"><span data-stu-id="f704b-139">List item B</span></span>
- <span data-ttu-id="f704b-140">List item 2</span><span class="sxs-lookup"><span data-stu-id="f704b-140">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="f704b-141">Liste ordonnée</span><span class="sxs-lookup"><span data-stu-id="f704b-141">Ordered list</span></span>

<span data-ttu-id="f704b-142">Pour formater une liste ordonnée/d'étapes, vous utilisez les numéros correspondants.</span><span class="sxs-lookup"><span data-stu-id="f704b-142">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="f704b-143">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="f704b-143">For example, the following Markdown:</span></span>

```md
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="f704b-144">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="f704b-144">will be rendered as:</span></span>

1. <span data-ttu-id="f704b-145">First instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-145">First instruction</span></span>
2. <span data-ttu-id="f704b-146">Second instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-146">Second instruction</span></span>
3. <span data-ttu-id="f704b-147">Third instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-147">Third instruction</span></span>

<span data-ttu-id="f704b-148">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="f704b-148">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="f704b-149">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="f704b-149">For example, the following Markdown:</span></span>

```md
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="f704b-150">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="f704b-150">will be rendered as:</span></span>

1. <span data-ttu-id="f704b-151">First instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-151">First instruction</span></span>
   1. <span data-ttu-id="f704b-152">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-152">Sub-instruction</span></span>
   2. <span data-ttu-id="f704b-153">Sub-instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-153">Sub-instruction</span></span>
2. <span data-ttu-id="f704b-154">Second instruction</span><span class="sxs-lookup"><span data-stu-id="f704b-154">Second instruction</span></span>

<span data-ttu-id="f704b-155">Notez que nous utilisons « 1. »</span><span class="sxs-lookup"><span data-stu-id="f704b-155">Note that we use '1.'</span></span> <span data-ttu-id="f704b-156">pour toutes les entrées.</span><span class="sxs-lookup"><span data-stu-id="f704b-156">for all entries.</span></span> <span data-ttu-id="f704b-157">Cela facilite la révision des différences quand des mises à jour ultérieures comprennent de nouvelles étapes ou suppriment des étapes existantes.</span><span class="sxs-lookup"><span data-stu-id="f704b-157">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="f704b-158">Les tableaux</span><span class="sxs-lookup"><span data-stu-id="f704b-158">Tables</span></span>

<span data-ttu-id="f704b-159">Les tableaux ne sont pas pris en charge par la spécification Markdown principale, mais ils sont pris en charge par GFM.</span><span class="sxs-lookup"><span data-stu-id="f704b-159">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="f704b-160">Vous pouvez créer des tableaux avec la barre verticale (|) et le trait d’union (-).</span><span class="sxs-lookup"><span data-stu-id="f704b-160">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="f704b-161">Les traits d’union servent à créer l’en-tête de chaque colonne, tandis que les barres verticales séparent chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="f704b-161">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="f704b-162">Ajoutez une ligne vide avant votre tableau pour qu’il s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="f704b-162">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="f704b-163">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="f704b-163">For example, the following Markdown:</span></span>

```md
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="f704b-164">sera restitué comme ceci :</span><span class="sxs-lookup"><span data-stu-id="f704b-164">Will be rendered as:</span></span>

| <span data-ttu-id="f704b-165">Fun</span><span class="sxs-lookup"><span data-stu-id="f704b-165">Fun</span></span>                  | <span data-ttu-id="f704b-166">With</span><span class="sxs-lookup"><span data-stu-id="f704b-166">With</span></span>                 | <span data-ttu-id="f704b-167">Les tableaux</span><span class="sxs-lookup"><span data-stu-id="f704b-167">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="f704b-168">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="f704b-168">left-aligned column</span></span>  | <span data-ttu-id="f704b-169">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="f704b-169">right-aligned column</span></span> | <span data-ttu-id="f704b-170">centered column</span><span class="sxs-lookup"><span data-stu-id="f704b-170">centered column</span></span> |
| <span data-ttu-id="f704b-171">$100</span><span class="sxs-lookup"><span data-stu-id="f704b-171">$100</span></span>                 | <span data-ttu-id="f704b-172">$100</span><span class="sxs-lookup"><span data-stu-id="f704b-172">$100</span></span>                 | <span data-ttu-id="f704b-173">$100</span><span class="sxs-lookup"><span data-stu-id="f704b-173">$100</span></span>            |
| <span data-ttu-id="f704b-174">$10</span><span class="sxs-lookup"><span data-stu-id="f704b-174">$10</span></span>                  | <span data-ttu-id="f704b-175">$10</span><span class="sxs-lookup"><span data-stu-id="f704b-175">$10</span></span>                  | <span data-ttu-id="f704b-176">$10</span><span class="sxs-lookup"><span data-stu-id="f704b-176">$10</span></span>             |
| <span data-ttu-id="f704b-177">$1</span><span class="sxs-lookup"><span data-stu-id="f704b-177">$1</span></span>                   | <span data-ttu-id="f704b-178">$1</span><span class="sxs-lookup"><span data-stu-id="f704b-178">$1</span></span>                   | <span data-ttu-id="f704b-179">$1</span><span class="sxs-lookup"><span data-stu-id="f704b-179">$1</span></span>              |

<span data-ttu-id="f704b-180">Pour plus d'informations sur la création de tableaux, consultez :</span><span class="sxs-lookup"><span data-stu-id="f704b-180">For more information on creating tables, see:</span></span>

- <span data-ttu-id="f704b-181">[Organisation des informations avec des tableaux](https://help.github.com/articles/organizing-information-with-tables/), de GitHub.</span><span class="sxs-lookup"><span data-stu-id="f704b-181">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="f704b-182">L’application web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="f704b-182">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="f704b-183">[« Markdown Cheatsheet » d’Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="f704b-183">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="f704b-184">[« Markdown Extra » de Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="f704b-184">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="f704b-185">[Convertir les tableaux HTML en Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="f704b-185">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="f704b-186">Liens</span><span class="sxs-lookup"><span data-stu-id="f704b-186">Links</span></span>

<span data-ttu-id="f704b-187">La syntaxe Markdown pour un lien inline est composée d’une partie `[link text]`, qui est le texte du lien, suivie de la partie `(file-name.md)`, qui est l’URL ou le nom du fichier cible du lien :</span><span class="sxs-lookup"><span data-stu-id="f704b-187">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="f704b-188">Pour plus d’informations sur la liaison, consultez :</span><span class="sxs-lookup"><span data-stu-id="f704b-188">For more information on linking, see:</span></span>

- <span data-ttu-id="f704b-189">Le [Guide de syntaxe Markdown](https://daringfireball.net/projects/markdown/syntax#link) pour plus de détails sur la prise en charge des liens de base avec Markdown.</span><span class="sxs-lookup"><span data-stu-id="f704b-189">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="f704b-190">La section [Liens](how-to-write-links.md) de ce guide pour plus de détails sur la syntaxe de liaison supplémentaire fournie par Markdig.</span><span class="sxs-lookup"><span data-stu-id="f704b-190">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="f704b-191">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="f704b-191">Code snippets</span></span>

<span data-ttu-id="f704b-192">Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases.</span><span class="sxs-lookup"><span data-stu-id="f704b-192">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="f704b-193">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="f704b-193">For details, see:</span></span>

- [<span data-ttu-id="f704b-194">Prise en charge native des blocs de code par Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-194">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="f704b-195">Prise en charge du cloisonnement de code et du surlignage de la syntaxe par GFM</span><span class="sxs-lookup"><span data-stu-id="f704b-195">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="f704b-196">Les blocs de code cloisonnés sont un moyen facile de permettre le surlignage de la syntaxe de vos extraits de code.</span><span class="sxs-lookup"><span data-stu-id="f704b-196">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="f704b-197">Le format général des blocs de code cloisonnés est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f704b-197">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="f704b-198">L’alias après les trois caractères accent grave (\`) initiaux définit le surlignage de syntaxe à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f704b-198">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="f704b-199">Vous trouverez ci-après une liste de langages de programmation couramment utilisés dans le contenu Docs et l’étiquette correspondante :</span><span class="sxs-lookup"><span data-stu-id="f704b-199">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="f704b-200">Ces langages prennent en charge les noms conviviaux, et pour la plupart d’entre eux, la mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="f704b-200">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="f704b-201">Name</span><span class="sxs-lookup"><span data-stu-id="f704b-201">Name</span></span>|<span data-ttu-id="f704b-202">Étiquette Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-202">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="f704b-203">.NET Console</span><span class="sxs-lookup"><span data-stu-id="f704b-203">.NET Console</span></span>|<span data-ttu-id="f704b-204">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="f704b-204">dotnetcli</span></span>|
|<span data-ttu-id="f704b-205">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="f704b-205">ASP.NET (C#)</span></span>|<span data-ttu-id="f704b-206">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="f704b-206">aspx-csharp</span></span>|
|<span data-ttu-id="f704b-207">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="f704b-207">ASP.NET (VB)</span></span>|<span data-ttu-id="f704b-208">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="f704b-208">aspx-vb</span></span>|
|<span data-ttu-id="f704b-209">AzCopy</span><span class="sxs-lookup"><span data-stu-id="f704b-209">AzCopy</span></span>|<span data-ttu-id="f704b-210">azcopy</span><span class="sxs-lookup"><span data-stu-id="f704b-210">azcopy</span></span>|
|<span data-ttu-id="f704b-211">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f704b-211">Azure CLI</span></span>|<span data-ttu-id="f704b-212">azurecli</span><span class="sxs-lookup"><span data-stu-id="f704b-212">azurecli</span></span>|
|<span data-ttu-id="f704b-213">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f704b-213">Azure PowerShell</span></span>|<span data-ttu-id="f704b-214">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="f704b-214">azurepowershell</span></span>|
|<span data-ttu-id="f704b-215">Bash</span><span class="sxs-lookup"><span data-stu-id="f704b-215">Bash</span></span>|<span data-ttu-id="f704b-216">bash</span><span class="sxs-lookup"><span data-stu-id="f704b-216">bash</span></span>|
|<span data-ttu-id="f704b-217">C++</span><span class="sxs-lookup"><span data-stu-id="f704b-217">C++</span></span>|<span data-ttu-id="f704b-218">cpp</span><span class="sxs-lookup"><span data-stu-id="f704b-218">cpp</span></span>|
|<span data-ttu-id="f704b-219">C++/CX</span><span class="sxs-lookup"><span data-stu-id="f704b-219">C++/CX</span></span>|<span data-ttu-id="f704b-220">cppcx</span><span class="sxs-lookup"><span data-stu-id="f704b-220">cppcx</span></span>|
|<span data-ttu-id="f704b-221">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="f704b-221">C++/WinRT</span></span>|<span data-ttu-id="f704b-222">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="f704b-222">cppwinrt</span></span>|
|<span data-ttu-id="f704b-223">C#</span><span class="sxs-lookup"><span data-stu-id="f704b-223">C#</span></span>|<span data-ttu-id="f704b-224">csharp</span><span class="sxs-lookup"><span data-stu-id="f704b-224">csharp</span></span>|
|<span data-ttu-id="f704b-225">C# dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="f704b-225">C# in browser</span></span>|<span data-ttu-id="f704b-226">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="f704b-226">csharp-interactive</span></span>|
|<span data-ttu-id="f704b-227">Console</span><span class="sxs-lookup"><span data-stu-id="f704b-227">Console</span></span>|<span data-ttu-id="f704b-228">console</span><span class="sxs-lookup"><span data-stu-id="f704b-228">console</span></span>|
|<span data-ttu-id="f704b-229">CSHTML</span><span class="sxs-lookup"><span data-stu-id="f704b-229">CSHTML</span></span>|<span data-ttu-id="f704b-230">cshtml</span><span class="sxs-lookup"><span data-stu-id="f704b-230">cshtml</span></span>|
|<span data-ttu-id="f704b-231">DAX</span><span class="sxs-lookup"><span data-stu-id="f704b-231">DAX</span></span>|<span data-ttu-id="f704b-232">dax</span><span class="sxs-lookup"><span data-stu-id="f704b-232">dax</span></span>|
|<span data-ttu-id="f704b-233">Docker</span><span class="sxs-lookup"><span data-stu-id="f704b-233">Docker</span></span>|<span data-ttu-id="f704b-234">dockerfile</span><span class="sxs-lookup"><span data-stu-id="f704b-234">dockerfile</span></span>|
|<span data-ttu-id="f704b-235">F#</span><span class="sxs-lookup"><span data-stu-id="f704b-235">F#</span></span>|<span data-ttu-id="f704b-236">fsharp</span><span class="sxs-lookup"><span data-stu-id="f704b-236">fsharp</span></span>|
|<span data-ttu-id="f704b-237">Go</span><span class="sxs-lookup"><span data-stu-id="f704b-237">Go</span></span>|<span data-ttu-id="f704b-238">go</span><span class="sxs-lookup"><span data-stu-id="f704b-238">go</span></span>|
|<span data-ttu-id="f704b-239">HTML</span><span class="sxs-lookup"><span data-stu-id="f704b-239">HTML</span></span>|<span data-ttu-id="f704b-240">html</span><span class="sxs-lookup"><span data-stu-id="f704b-240">html</span></span>|
|<span data-ttu-id="f704b-241">HTTP</span><span class="sxs-lookup"><span data-stu-id="f704b-241">HTTP</span></span>|<span data-ttu-id="f704b-242">http</span><span class="sxs-lookup"><span data-stu-id="f704b-242">http</span></span>|
|<span data-ttu-id="f704b-243">Java</span><span class="sxs-lookup"><span data-stu-id="f704b-243">Java</span></span>|<span data-ttu-id="f704b-244">java</span><span class="sxs-lookup"><span data-stu-id="f704b-244">java</span></span>|
|<span data-ttu-id="f704b-245">JavaScript</span><span class="sxs-lookup"><span data-stu-id="f704b-245">JavaScript</span></span>|<span data-ttu-id="f704b-246">javascript</span><span class="sxs-lookup"><span data-stu-id="f704b-246">javascript</span></span>|
|<span data-ttu-id="f704b-247">JSON</span><span class="sxs-lookup"><span data-stu-id="f704b-247">JSON</span></span>|<span data-ttu-id="f704b-248">json</span><span class="sxs-lookup"><span data-stu-id="f704b-248">json</span></span>|
|<span data-ttu-id="f704b-249">Langage de requête Kusto</span><span class="sxs-lookup"><span data-stu-id="f704b-249">Kusto Query Language</span></span>|<span data-ttu-id="f704b-250">kusto</span><span class="sxs-lookup"><span data-stu-id="f704b-250">kusto</span></span>|
|<span data-ttu-id="f704b-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-251">Markdown</span></span>|<span data-ttu-id="f704b-252">md</span><span class="sxs-lookup"><span data-stu-id="f704b-252">md</span></span>|
|<span data-ttu-id="f704b-253">Objective-C</span><span class="sxs-lookup"><span data-stu-id="f704b-253">Objective-C</span></span>|<span data-ttu-id="f704b-254">objc</span><span class="sxs-lookup"><span data-stu-id="f704b-254">objc</span></span>|
|<span data-ttu-id="f704b-255">OData</span><span class="sxs-lookup"><span data-stu-id="f704b-255">OData</span></span>|<span data-ttu-id="f704b-256">odata</span><span class="sxs-lookup"><span data-stu-id="f704b-256">odata</span></span>|
|<span data-ttu-id="f704b-257">PHP</span><span class="sxs-lookup"><span data-stu-id="f704b-257">PHP</span></span>|<span data-ttu-id="f704b-258">php</span><span class="sxs-lookup"><span data-stu-id="f704b-258">php</span></span>|
|<span data-ttu-id="f704b-259">PowerApps (séparateur décimal point)</span><span class="sxs-lookup"><span data-stu-id="f704b-259">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="f704b-260">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="f704b-260">powerapps-dot</span></span>|
|<span data-ttu-id="f704b-261">PowerApps (séparateur décimal virgule)</span><span class="sxs-lookup"><span data-stu-id="f704b-261">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="f704b-262">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="f704b-262">powerapps-comma</span></span>|
|<span data-ttu-id="f704b-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f704b-263">PowerShell</span></span>|<span data-ttu-id="f704b-264">powershell</span><span class="sxs-lookup"><span data-stu-id="f704b-264">powershell</span></span>|
|<span data-ttu-id="f704b-265">Python</span><span class="sxs-lookup"><span data-stu-id="f704b-265">Python</span></span>|<span data-ttu-id="f704b-266">python</span><span class="sxs-lookup"><span data-stu-id="f704b-266">python</span></span>|
|<span data-ttu-id="f704b-267">Q#</span><span class="sxs-lookup"><span data-stu-id="f704b-267">Q#</span></span>|<span data-ttu-id="f704b-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="f704b-268">qsharp</span></span>|
|<span data-ttu-id="f704b-269">R</span><span class="sxs-lookup"><span data-stu-id="f704b-269">R</span></span>|<span data-ttu-id="f704b-270">r</span><span class="sxs-lookup"><span data-stu-id="f704b-270">r</span></span>|
|<span data-ttu-id="f704b-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="f704b-271">Ruby</span></span>|<span data-ttu-id="f704b-272">ruby</span><span class="sxs-lookup"><span data-stu-id="f704b-272">ruby</span></span>|
|<span data-ttu-id="f704b-273">SQL</span><span class="sxs-lookup"><span data-stu-id="f704b-273">SQL</span></span>|<span data-ttu-id="f704b-274">sql</span><span class="sxs-lookup"><span data-stu-id="f704b-274">sql</span></span>|
|<span data-ttu-id="f704b-275">Swift</span><span class="sxs-lookup"><span data-stu-id="f704b-275">Swift</span></span>|<span data-ttu-id="f704b-276">swift</span><span class="sxs-lookup"><span data-stu-id="f704b-276">swift</span></span>|
|<span data-ttu-id="f704b-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="f704b-277">TypeScript</span></span>|<span data-ttu-id="f704b-278">typescript</span><span class="sxs-lookup"><span data-stu-id="f704b-278">typescript</span></span>|
|<span data-ttu-id="f704b-279">VB</span><span class="sxs-lookup"><span data-stu-id="f704b-279">VB</span></span>|<span data-ttu-id="f704b-280">vb</span><span class="sxs-lookup"><span data-stu-id="f704b-280">vb</span></span>|
|<span data-ttu-id="f704b-281">XAML</span><span class="sxs-lookup"><span data-stu-id="f704b-281">XAML</span></span>|<span data-ttu-id="f704b-282">xaml</span><span class="sxs-lookup"><span data-stu-id="f704b-282">xaml</span></span>|
|<span data-ttu-id="f704b-283">XML</span><span class="sxs-lookup"><span data-stu-id="f704b-283">XML</span></span>|<span data-ttu-id="f704b-284">xml</span><span class="sxs-lookup"><span data-stu-id="f704b-284">xml</span></span>|

<span data-ttu-id="f704b-285">Le nom `csharp-interactive` spécifie le langage C# et la capacité à exécuter les exemples à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f704b-285">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="f704b-286">Ces extraits sont compilés et exécutés dans un conteneur Docker, et les résultats de cette exécution de programme sont affichés dans la fenêtre de navigateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f704b-286">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="f704b-287">Exemple : C\#</span><span class="sxs-lookup"><span data-stu-id="f704b-287">Example: C\#</span></span>

<span data-ttu-id="f704b-288">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f704b-288">__Markdown__</span></span>

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

<span data-ttu-id="f704b-289">__Render__</span><span class="sxs-lookup"><span data-stu-id="f704b-289">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="f704b-290">Exemple : SQL</span><span class="sxs-lookup"><span data-stu-id="f704b-290">Example: SQL</span></span>

<span data-ttu-id="f704b-291">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="f704b-291">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="f704b-292">__Render__</span><span class="sxs-lookup"><span data-stu-id="f704b-292">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="docs-custom-markdown-extensions"></a><span data-ttu-id="f704b-293">Extensions Markdown personnalisées Docs</span><span class="sxs-lookup"><span data-stu-id="f704b-293">Docs custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="f704b-294">Docs.Microsoft.com (Docs) implémente un analyseur Markdig pour Markdown, qui est hautement compatible avec GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="f704b-294">Docs.Microsoft.com (Docs) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="f704b-295">Markdig ajoute des fonctionnalités via des extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="f704b-295">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="f704b-296">À ce titre, des articles sélectionnés du Guide de création OPS complet sont inclus dans ce guide pour référence.</span><span class="sxs-lookup"><span data-stu-id="f704b-296">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="f704b-297">(Par exemple, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.)</span><span class="sxs-lookup"><span data-stu-id="f704b-297">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="f704b-298">Les articles Docs utilisent GFM pour la majeure partie de la mise en forme des articles, comme les paragraphes, les liens, les listes et les en-têtes.</span><span class="sxs-lookup"><span data-stu-id="f704b-298">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="f704b-299">Pour une mise en forme plus riche, les articles peuvent utiliser des fonctionnalités Markdig comme :</span><span class="sxs-lookup"><span data-stu-id="f704b-299">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="f704b-300">Blocs de notes</span><span class="sxs-lookup"><span data-stu-id="f704b-300">Note blocks</span></span>
- <span data-ttu-id="f704b-301">Fichiers Include</span><span class="sxs-lookup"><span data-stu-id="f704b-301">Include files</span></span>
- <span data-ttu-id="f704b-302">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="f704b-302">Selectors</span></span>
- <span data-ttu-id="f704b-303">Des vidéos intégrées</span><span class="sxs-lookup"><span data-stu-id="f704b-303">Embedded videos</span></span>
- <span data-ttu-id="f704b-304">Des exemples/extraits de code</span><span class="sxs-lookup"><span data-stu-id="f704b-304">Code snippets/samples</span></span>

<span data-ttu-id="f704b-305">Pour obtenir la liste complète, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.</span><span class="sxs-lookup"><span data-stu-id="f704b-305">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="f704b-306">Blocs de notes</span><span class="sxs-lookup"><span data-stu-id="f704b-306">Note blocks</span></span>

<span data-ttu-id="f704b-307">Vous pouvez choisir parmi quatre types de blocs de notes pour attirer l’attention sur du contenu spécifique :</span><span class="sxs-lookup"><span data-stu-id="f704b-307">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="f704b-308">REMARQUE</span><span class="sxs-lookup"><span data-stu-id="f704b-308">NOTE</span></span>
- <span data-ttu-id="f704b-309">AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="f704b-309">WARNING</span></span>
- <span data-ttu-id="f704b-310">CONSEIL</span><span class="sxs-lookup"><span data-stu-id="f704b-310">TIP</span></span>
- <span data-ttu-id="f704b-311">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="f704b-311">IMPORTANT</span></span>

<span data-ttu-id="f704b-312">En général, les blocs de notes doivent être utilisés avec parcimonie, car ils peuvent perturber la lecture.</span><span class="sxs-lookup"><span data-stu-id="f704b-312">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="f704b-313">Même s’ils prennent également en charge les blocs de code, les images, les listes et les liens, essayez de vous limiter à des blocs de notes simples et directs.</span><span class="sxs-lookup"><span data-stu-id="f704b-313">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="f704b-314">Exemples :</span><span class="sxs-lookup"><span data-stu-id="f704b-314">Examples:</span></span>

```md
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

<span data-ttu-id="f704b-315">Ces alertes ressemblent à ceci sur docs.microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="f704b-315">These alerts look like this on docs.microsoft.com:</span></span>

![montre comment les alertes de l’exemple précédent apparaissent sur la page Documentation publiée avec les différentes icônes et couleurs](media/alerts-rendering.png)

### <a name="include-files"></a><span data-ttu-id="f704b-317">Fichiers Include</span><span class="sxs-lookup"><span data-stu-id="f704b-317">Include files</span></span>

<span data-ttu-id="f704b-318">Quand vous avez du texte ou des fichiers image réutilisables qui doivent être inclus dans des fichiers d’article, vous pouvez utiliser une référence vers le fichier « include » via la fonctionnalité d’inclusion de fichier de Markdig.</span><span class="sxs-lookup"><span data-stu-id="f704b-318">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="f704b-319">Cette fonctionnalité demande à OPS d’inclure le fichier dans votre fichier d’article lors de sa génération, ce qui en fait une partie de votre article publié.</span><span class="sxs-lookup"><span data-stu-id="f704b-319">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="f704b-320">Trois types de références include sont disponibles pour vous aider à réutiliser du contenu :</span><span class="sxs-lookup"><span data-stu-id="f704b-320">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="f704b-321">Inline : pour réutiliser un extrait de texte commun au sein d’une autre phrase.</span><span class="sxs-lookup"><span data-stu-id="f704b-321">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="f704b-322">Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.</span><span class="sxs-lookup"><span data-stu-id="f704b-322">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="f704b-323">Image : il s’agit de la façon dont l’inclusion d’images standard est implémentée dans Docs.</span><span class="sxs-lookup"><span data-stu-id="f704b-323">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="f704b-324">Un fichier include de type inline ou bloc est un simple fichier Markdown (.md).</span><span class="sxs-lookup"><span data-stu-id="f704b-324">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="f704b-325">Il peut contenir tout code Markdown valide.</span><span class="sxs-lookup"><span data-stu-id="f704b-325">It can contain any valid Markdown.</span></span> <span data-ttu-id="f704b-326">Tous les fichiers Markdown include doivent être placés dans un [sous-répertoire `/includes` commun ](git-github-fundamentals.md#includes-subdirectory), à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="f704b-326">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="f704b-327">Quand l’article est publié, le fichier inclus y est intégré de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="f704b-327">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="f704b-328">Voici les conditions requises et éléments à prendre en compte pour les fichiers include :</span><span class="sxs-lookup"><span data-stu-id="f704b-328">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="f704b-329">Utilisez un fichier include quand vous souhaitez que le même texte s’affiche dans plusieurs articles.</span><span class="sxs-lookup"><span data-stu-id="f704b-329">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="f704b-330">Utilisez une référence include de type bloc pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée.</span><span class="sxs-lookup"><span data-stu-id="f704b-330">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="f704b-331">Ne l'utilisez pas pour des éléments plus petits qu'une phrase.</span><span class="sxs-lookup"><span data-stu-id="f704b-331">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="f704b-332">Les références include ne seront pas restituées dans la vue de votre article rendu par GitHub, car elles reposent sur des extensions Markdig.</span><span class="sxs-lookup"><span data-stu-id="f704b-332">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="f704b-333">Ils ne sont rendus qu’après publication.</span><span class="sxs-lookup"><span data-stu-id="f704b-333">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="f704b-334">Vérifiez que tout le texte dans un fichier include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence le fichier include.</span><span class="sxs-lookup"><span data-stu-id="f704b-334">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="f704b-335">Ignorer cette instruction crée une chaîne intraduisible dans l'article, ce qui nuit à l'expérience localisée.</span><span class="sxs-lookup"><span data-stu-id="f704b-335">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="f704b-336">N’incorporez pas de références include dans d’autres fichiers include.</span><span class="sxs-lookup"><span data-stu-id="f704b-336">Don't embed include references within other include files.</span></span> <span data-ttu-id="f704b-337">Les groupes ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f704b-337">They are not supported.</span></span>
- <span data-ttu-id="f704b-338">Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="f704b-338">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="f704b-339">Le répertoire multimédia ne doit pas contenir d'images à sa racine.</span><span class="sxs-lookup"><span data-stu-id="f704b-339">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="f704b-340">Si le fichier include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire multimédia correspondant.</span><span class="sxs-lookup"><span data-stu-id="f704b-340">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="f704b-341">Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include.</span><span class="sxs-lookup"><span data-stu-id="f704b-341">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="f704b-342">Utilisez un fichier distinct avec un nom unique pour chaque fichier include et article.</span><span class="sxs-lookup"><span data-stu-id="f704b-342">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="f704b-343">Stockez le fichier multimédia dans le dossier multimédia associé au fichier include.</span><span class="sxs-lookup"><span data-stu-id="f704b-343">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="f704b-344">N’utilisez pas un fichier include comme seul contenu d’un article.</span><span class="sxs-lookup"><span data-stu-id="f704b-344">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="f704b-345">Les fichiers include sont censés compléter le contenu du reste de l’article.</span><span class="sxs-lookup"><span data-stu-id="f704b-345">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="f704b-346">Exemple :</span><span class="sxs-lookup"><span data-stu-id="f704b-346">Example:</span></span>

```md
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="f704b-347">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="f704b-347">Selectors</span></span>

<span data-ttu-id="f704b-348">Utilisez des sélecteurs dans les articles techniques quand vous créez plusieurs versions d’un même article, afin de répondre aux différences d’implémentation entre les technologies et plateformes.</span><span class="sxs-lookup"><span data-stu-id="f704b-348">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="f704b-349">Cela s'applique particulièrement au contenu pour plateformes mobiles pour développeurs.</span><span class="sxs-lookup"><span data-stu-id="f704b-349">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="f704b-350">Il existe actuellement deux types différents de sélecteurs dans Markdig, un sélecteur unique et un multi-sélecteur.</span><span class="sxs-lookup"><span data-stu-id="f704b-350">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="f704b-351">Le même Markdown de sélecteur allant dans chaque article de la sélection, nous vous recommandons de placer le sélecteur pour votre article dans un fichier include.</span><span class="sxs-lookup"><span data-stu-id="f704b-351">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="f704b-352">Vous pouvez ensuite référencer ce dernier dans tous vos articles qui utilisent le même sélecteur.</span><span class="sxs-lookup"><span data-stu-id="f704b-352">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="f704b-353">Voici un exemple de sélecteur :</span><span class="sxs-lookup"><span data-stu-id="f704b-353">The following shows an example selector:</span></span>

```md
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="f704b-354">Vous pouvez obtenir un exemple de sélecteurs en action dans la [Documentation Azure](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span><span class="sxs-lookup"><span data-stu-id="f704b-354">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="f704b-355">Références include de code</span><span class="sxs-lookup"><span data-stu-id="f704b-355">Code include references</span></span>

<span data-ttu-id="f704b-356">Markdig prend en charge l’inclusion avancée de code dans un article, via son extension d’extraits de code.</span><span class="sxs-lookup"><span data-stu-id="f704b-356">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="f704b-357">Elle fournit un rendu avancé qui se base sur les fonctionnalités de GFM comme la sélection du langage de programmation et la coloration de la syntaxe, plus des fonctionnalités intéressantes comme :</span><span class="sxs-lookup"><span data-stu-id="f704b-357">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="f704b-358">l’inclusion d’exemples/extraits de code centralisés depuis un dépôt externe ;</span><span class="sxs-lookup"><span data-stu-id="f704b-358">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="f704b-359">une interface à onglets pour présenter différentes versions des exemples de code dans différents langages.</span><span class="sxs-lookup"><span data-stu-id="f704b-359">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="f704b-360">Pièges et résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="f704b-360">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="f704b-361">Texte de remplacement</span><span class="sxs-lookup"><span data-stu-id="f704b-361">Alt text</span></span>

<span data-ttu-id="f704b-362">Le texte de remplacement qui contient des traits de soulignement ne s’affiche pas correctement.</span><span class="sxs-lookup"><span data-stu-id="f704b-362">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="f704b-363">Par exemple, au lieu d’utiliser ceci :</span><span class="sxs-lookup"><span data-stu-id="f704b-363">For example, instead of using this:</span></span>

```md
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="f704b-364">Placez les traits de soulignement dans une séquence d’échappement comme ceci :</span><span class="sxs-lookup"><span data-stu-id="f704b-364">Escape the underscores like this:</span></span>

```md
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="f704b-365">Apostrophes et guillemets</span><span class="sxs-lookup"><span data-stu-id="f704b-365">Apostrophes and quotation marks</span></span>

<span data-ttu-id="f704b-366">Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes.</span><span class="sxs-lookup"><span data-stu-id="f704b-366">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="f704b-367">Vous devez les encoder ou les changer en apostrophes/guillemets de base.</span><span class="sxs-lookup"><span data-stu-id="f704b-367">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="f704b-368">Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="f704b-368">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="f704b-369">Voici les encodages pour les versions courbes de ces signes de ponctuation :</span><span class="sxs-lookup"><span data-stu-id="f704b-369">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="f704b-370">Guillemet gauche (ouvrant) : `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="f704b-370">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="f704b-371">Guillemet droit (fermant) : `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="f704b-371">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="f704b-372">Guillemet simple droit (fermant) ou apostrophe : `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="f704b-372">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="f704b-373">Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="f704b-373">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="f704b-374">Crochets pointus</span><span class="sxs-lookup"><span data-stu-id="f704b-374">Angle brackets</span></span>

<span data-ttu-id="f704b-375">Il est courant d’utiliser des crochets pointus pour indiquer un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="f704b-375">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="f704b-376">Quand vous effectuez cette opération dans un texte (pas dans du code), vous devez encoder les crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="f704b-376">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="f704b-377">Sinon, Markdown considère qu’il s’agit d’une balise HTML.</span><span class="sxs-lookup"><span data-stu-id="f704b-377">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="f704b-378">Par exemple, encodez `<script name>` en `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="f704b-378">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="markdown-flavor"></a><span data-ttu-id="f704b-379">Type de markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-379">Markdown flavor</span></span>

<span data-ttu-id="f704b-380">Le back-end du site docs.microsoft.com prend en charge le Markdown conforme à [CommonMark](https://commonmark.org/) analysé via le moteur d’analyse [Markdig](https://github.com/lunet-io/markdig).</span><span class="sxs-lookup"><span data-stu-id="f704b-380">The docs.microsoft.com site backend supports [CommonMark](https://commonmark.org/) compliant Markdown parsed through the [Markdig](https://github.com/lunet-io/markdig) parsing engine.</span></span> <span data-ttu-id="f704b-381">Ce type Markdown est essentiellement compatible avec [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), car la plupart des documents sont stockés dans GitHub et peuvent être modifiés à cet endroit.</span><span class="sxs-lookup"><span data-stu-id="f704b-381">This markdown flavor is mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="f704b-382">Des fonctionnalités sont ajoutées via des extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="f704b-382">Additional functionality is added through Markdown extensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="f704b-383">Voir aussi :</span><span class="sxs-lookup"><span data-stu-id="f704b-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="f704b-384">Ressources Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-384">Markdown resources</span></span>

- [<span data-ttu-id="f704b-385">Introduction à Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="f704b-386">Fiche récapitulative de Markdown pour Docs</span><span class="sxs-lookup"><span data-stu-id="f704b-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="f704b-387">Les bases du Markdown GitHub</span><span class="sxs-lookup"><span data-stu-id="f704b-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="f704b-388">Guide de Markdown</span><span class="sxs-lookup"><span data-stu-id="f704b-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
