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
ms.lasthandoff: 05/23/2018
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="c8c41-103">Guide pratique pour utiliser Markdown pour écrire du contenu Docs</span><span class="sxs-lookup"><span data-stu-id="c8c41-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="c8c41-104">Les articles docs.microsoft.com sont écrits dans un langage de balisage léger appelé [Markdown](https://daringfireball.net/projects/markdown/), à la fois facile à lire et facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="c8c41-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="c8c41-105">Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur.</span><span class="sxs-lookup"><span data-stu-id="c8c41-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="c8c41-106">Le contenu Docs étant stocké dans GitHub, il peut utiliser un sur-ensemble de Markdown appelé [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), qui offre des fonctionnalités supplémentaires pour les besoins courants de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="c8c41-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="c8c41-107">De plus, OPS (Open Publishing Services) implémente l’analyseur Markdown Markdig.</span><span class="sxs-lookup"><span data-stu-id="c8c41-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="c8c41-108">Markdig est hautement compatible avec GFM (GitHub Flavored Markdown) et offre de nouvelles fonctions permettant d’utiliser des fonctionnalités propres à Docs.</span><span class="sxs-lookup"><span data-stu-id="c8c41-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="c8c41-109">Markdig est un processeur Markdown rapide, performant, compatible CommonMark et extensible pour .NET.</span><span class="sxs-lookup"><span data-stu-id="c8c41-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="c8c41-110">Meilleure prise en charge de la communauté</span><span class="sxs-lookup"><span data-stu-id="c8c41-110">Better community support</span></span>
* <span data-ttu-id="c8c41-111">Meilleure prise en charge des standards</span><span class="sxs-lookup"><span data-stu-id="c8c41-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="c8c41-112">Les bases de Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="c8c41-113">En-têtes</span><span class="sxs-lookup"><span data-stu-id="c8c41-113">Headings</span></span>

<span data-ttu-id="c8c41-114">Pour créer un en-tête, vous utilisez un dièse (#), comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8c41-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="c8c41-115">Texte en gras et italique</span><span class="sxs-lookup"><span data-stu-id="c8c41-115">Bold and italic text</span></span>

<span data-ttu-id="c8c41-116">Pour mettre le texte en **gras**, vous l’entourez de deux astérisques :</span><span class="sxs-lookup"><span data-stu-id="c8c41-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="c8c41-117">Pour mettre le texte en *italique*, vous l’entourez d’un seul astérisque :</span><span class="sxs-lookup"><span data-stu-id="c8c41-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="c8c41-118">Pour mettre le texte en ***gras et en italique***, vous l’entourez de trois astérisques :</span><span class="sxs-lookup"><span data-stu-id="c8c41-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="c8c41-119">Listes</span><span class="sxs-lookup"><span data-stu-id="c8c41-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="c8c41-120">Liste non ordonnée</span><span class="sxs-lookup"><span data-stu-id="c8c41-120">Unordered list</span></span>

<span data-ttu-id="c8c41-121">Pour mettre en forme une liste à puces/non ordonnée, vous pouvez utiliser des astérisques ou des tirets.</span><span class="sxs-lookup"><span data-stu-id="c8c41-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="c8c41-122">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="c8c41-123">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-123">will be rendered as:</span></span>

- <span data-ttu-id="c8c41-124">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="c8c41-124">List item 1</span></span>
- <span data-ttu-id="c8c41-125">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="c8c41-125">List item 2</span></span>
- <span data-ttu-id="c8c41-126">Élément de liste 3</span><span class="sxs-lookup"><span data-stu-id="c8c41-126">List item 3</span></span>

<span data-ttu-id="c8c41-127">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="c8c41-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="c8c41-128">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="c8c41-129">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-129">will be rendered as:</span></span>

- <span data-ttu-id="c8c41-130">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="c8c41-130">List item 1</span></span>
  - <span data-ttu-id="c8c41-131">Élément de liste A</span><span class="sxs-lookup"><span data-stu-id="c8c41-131">List item A</span></span>
  - <span data-ttu-id="c8c41-132">Élément de liste B</span><span class="sxs-lookup"><span data-stu-id="c8c41-132">List item B</span></span>
- <span data-ttu-id="c8c41-133">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="c8c41-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="c8c41-134">Liste ordonnée</span><span class="sxs-lookup"><span data-stu-id="c8c41-134">Ordered list</span></span>

<span data-ttu-id="c8c41-135">Pour mettre en forme une liste ordonnée/d'étapes, vous utilisez les numéros correspondants.</span><span class="sxs-lookup"><span data-stu-id="c8c41-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="c8c41-136">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="c8c41-137">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-137">will be rendered as:</span></span>

1. <span data-ttu-id="c8c41-138">Première instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-138">First instruction</span></span>
2. <span data-ttu-id="c8c41-139">Deuxième instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-139">Second instruction</span></span>
3. <span data-ttu-id="c8c41-140">Troisième instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-140">Third instruction</span></span>

<span data-ttu-id="c8c41-141">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="c8c41-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="c8c41-142">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="c8c41-143">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-143">will be rendered as:</span></span>

1. <span data-ttu-id="c8c41-144">Première instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-144">First instruction</span></span>
    1. <span data-ttu-id="c8c41-145">Sous-instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-145">Sub-instruction</span></span>
    2. <span data-ttu-id="c8c41-146">Sous-instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-146">Sub-instruction</span></span>
2. <span data-ttu-id="c8c41-147">Deuxième instruction</span><span class="sxs-lookup"><span data-stu-id="c8c41-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="c8c41-148">les tableaux</span><span class="sxs-lookup"><span data-stu-id="c8c41-148">Tables</span></span>

<span data-ttu-id="c8c41-149">Les tableaux ne sont pas pris en charge par la spécification Markdown principale, mais ils sont pris en charge par GFM.</span><span class="sxs-lookup"><span data-stu-id="c8c41-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="c8c41-150">Vous pouvez créer des tableaux avec la barre verticale (|) et le trait d’union (-).</span><span class="sxs-lookup"><span data-stu-id="c8c41-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="c8c41-151">Les traits d’union servent à créer l’en-tête de chaque colonne, tandis que les barres verticales séparent chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="c8c41-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="c8c41-152">Ajoutez une ligne vide avant votre tableau pour qu’il s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="c8c41-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="c8c41-153">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="c8c41-154">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-154">will be rendered as:</span></span>

| <span data-ttu-id="c8c41-155">Amusez-vous</span><span class="sxs-lookup"><span data-stu-id="c8c41-155">Fun</span></span>                  | <span data-ttu-id="c8c41-156">avec</span><span class="sxs-lookup"><span data-stu-id="c8c41-156">With</span></span>                 | <span data-ttu-id="c8c41-157">les tableaux</span><span class="sxs-lookup"><span data-stu-id="c8c41-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="c8c41-158">colonne alignée à gauche</span><span class="sxs-lookup"><span data-stu-id="c8c41-158">left-aligned column</span></span>  | <span data-ttu-id="c8c41-159">colonne alignée à droite</span><span class="sxs-lookup"><span data-stu-id="c8c41-159">right-aligned column</span></span> | <span data-ttu-id="c8c41-160">colonne centrée</span><span class="sxs-lookup"><span data-stu-id="c8c41-160">centered column</span></span> |
| <span data-ttu-id="c8c41-161">100 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-161">$100</span></span>                 | <span data-ttu-id="c8c41-162">100 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-162">$100</span></span>                 | <span data-ttu-id="c8c41-163">100 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-163">$100</span></span>            |
| <span data-ttu-id="c8c41-164">10 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-164">$10</span></span>                  | <span data-ttu-id="c8c41-165">10 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-165">$10</span></span>                  | <span data-ttu-id="c8c41-166">10 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-166">$10</span></span>             |
| <span data-ttu-id="c8c41-167">1 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-167">$1</span></span>                   | <span data-ttu-id="c8c41-168">1 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-168">$1</span></span>                   | <span data-ttu-id="c8c41-169">1 $</span><span class="sxs-lookup"><span data-stu-id="c8c41-169">$1</span></span>              |

<span data-ttu-id="c8c41-170">Pour plus d'informations sur la création de tableaux, consultez :</span><span class="sxs-lookup"><span data-stu-id="c8c41-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="c8c41-171">La [fonctionnalité de wrapping de tableaux](#table-wrapping) Markdig, qui peut vous aider à mettre en forme les tableaux larges</span><span class="sxs-lookup"><span data-stu-id="c8c41-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="c8c41-172">[Organisation des informations avec des tableaux](https://help.github.com/articles/organizing-information-with-tables/), de GitHub</span><span class="sxs-lookup"><span data-stu-id="c8c41-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="c8c41-173">L'application Web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)</span><span class="sxs-lookup"><span data-stu-id="c8c41-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- [<span data-ttu-id="c8c41-174">« Markdown Cheatsheet » d'Adam Pritchard</span><span class="sxs-lookup"><span data-stu-id="c8c41-174">Adam Pritchard's Markdown Cheatsheet</span></span>](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)
- [<span data-ttu-id="c8c41-175">« Markdown Extra » de Michel Fortin</span><span class="sxs-lookup"><span data-stu-id="c8c41-175">Michel Fortin's Markdown Extra</span></span>](https://michelf.ca/projects/php-markdown/extra/#table)
- [<span data-ttu-id="c8c41-176">Convertir les tableaux HTML en Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="c8c41-177">Liens</span><span class="sxs-lookup"><span data-stu-id="c8c41-177">Links</span></span>

<span data-ttu-id="c8c41-178">La syntaxe Markdown pour un lien inline est composée d’une partie `[link text]`, qui est le texte du lien, suivie de la partie `(file-name.md)`, qui est l’URL ou le nom du fichier cible du lien :</span><span class="sxs-lookup"><span data-stu-id="c8c41-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="c8c41-179">Pour plus d’informations sur la liaison, consultez :</span><span class="sxs-lookup"><span data-stu-id="c8c41-179">For more information on linking, see:</span></span>

- <span data-ttu-id="c8c41-180">Le [Guide de syntaxe Markdown](https://daringfireball.net/projects/markdown/syntax#link) pour plus de détails sur la prise en charge des liens de base avec Markdown.</span><span class="sxs-lookup"><span data-stu-id="c8c41-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="c8c41-181">La section [Liens](how-to-write-links.md) de ce guide pour plus de détails sur la syntaxe de liaison supplémentaire fournie par Markdig.</span><span class="sxs-lookup"><span data-stu-id="c8c41-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="c8c41-182">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="c8c41-182">Code snippets</span></span>

<span data-ttu-id="c8c41-183">Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases.</span><span class="sxs-lookup"><span data-stu-id="c8c41-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="c8c41-184">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="c8c41-184">For details, see:</span></span>

- [<span data-ttu-id="c8c41-185">Prise en charge native des blocs de code par Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="c8c41-186">Prise en charge du cloisonnement de code et du surlignage de la syntaxe par GFM</span><span class="sxs-lookup"><span data-stu-id="c8c41-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="c8c41-187">Les blocs de code cloisonnés sont un moyen facile de permettre le surlignage de la syntaxe de vos extraits de code.</span><span class="sxs-lookup"><span data-stu-id="c8c41-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="c8c41-188">Le format général des blocs de code cloisonnés est le suivant :</span><span class="sxs-lookup"><span data-stu-id="c8c41-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="c8c41-189">L’alias après les trois caractères accent grave (\`) initiaux définit le surlignage de syntaxe à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c8c41-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="c8c41-190">Vous trouverez ci-après une liste de langages de programmation couramment utilisés dans le contenu Docs et l’étiquette correspondante :</span><span class="sxs-lookup"><span data-stu-id="c8c41-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="c8c41-191">Ces langages prennent en charge les noms conviviaux, et pour la plupart d’entre eux, la mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="c8c41-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="c8c41-192">Nom</span><span class="sxs-lookup"><span data-stu-id="c8c41-192">Name</span></span>|<span data-ttu-id="c8c41-193">Étiquette Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="c8c41-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="c8c41-194">.NET Console</span></span>|<span data-ttu-id="c8c41-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="c8c41-195">dotnetcli</span></span>|
|<span data-ttu-id="c8c41-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="c8c41-196">ASP.NET (C#)</span></span>|<span data-ttu-id="c8c41-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="c8c41-197">aspx-csharp</span></span>|
|<span data-ttu-id="c8c41-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="c8c41-198">ASP.NET (VB)</span></span>|<span data-ttu-id="c8c41-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="c8c41-199">aspx-vb</span></span>|
|<span data-ttu-id="c8c41-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="c8c41-200">AzCopy</span></span>|<span data-ttu-id="c8c41-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="c8c41-201">azcopy</span></span>|
|<span data-ttu-id="c8c41-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="c8c41-202">Azure CLI</span></span>|<span data-ttu-id="c8c41-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="c8c41-203">azurecli</span></span>|
|<span data-ttu-id="c8c41-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8c41-204">Azure PowerShell</span></span>|<span data-ttu-id="c8c41-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="c8c41-205">azurepowershell</span></span>|
|<span data-ttu-id="c8c41-206">C++</span><span class="sxs-lookup"><span data-stu-id="c8c41-206">C++</span></span>|<span data-ttu-id="c8c41-207">cpp</span><span class="sxs-lookup"><span data-stu-id="c8c41-207">cpp</span></span>|
|<span data-ttu-id="c8c41-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="c8c41-208">C++/CX</span></span>|<span data-ttu-id="c8c41-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="c8c41-209">cppcx</span></span>|
|<span data-ttu-id="c8c41-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="c8c41-210">C++/WinRT</span></span>|<span data-ttu-id="c8c41-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="c8c41-211">cppwinrt</span></span>|
|<span data-ttu-id="c8c41-212">C#</span><span class="sxs-lookup"><span data-stu-id="c8c41-212">C#</span></span>|<span data-ttu-id="c8c41-213">csharp</span><span class="sxs-lookup"><span data-stu-id="c8c41-213">csharp</span></span>|
|<span data-ttu-id="c8c41-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="c8c41-214">CSHTML</span></span>|<span data-ttu-id="c8c41-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="c8c41-215">cshtml</span></span>|
|<span data-ttu-id="c8c41-216">DAX</span><span class="sxs-lookup"><span data-stu-id="c8c41-216">DAX</span></span>|<span data-ttu-id="c8c41-217">dax</span><span class="sxs-lookup"><span data-stu-id="c8c41-217">dax</span></span>|
|<span data-ttu-id="c8c41-218">F#</span><span class="sxs-lookup"><span data-stu-id="c8c41-218">F#</span></span>|<span data-ttu-id="c8c41-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="c8c41-219">fsharp</span></span>|
|<span data-ttu-id="c8c41-220">Go</span><span class="sxs-lookup"><span data-stu-id="c8c41-220">Go</span></span>|<span data-ttu-id="c8c41-221">go</span><span class="sxs-lookup"><span data-stu-id="c8c41-221">go</span></span>|
|<span data-ttu-id="c8c41-222">HTML</span><span class="sxs-lookup"><span data-stu-id="c8c41-222">HTML</span></span>|<span data-ttu-id="c8c41-223">html</span><span class="sxs-lookup"><span data-stu-id="c8c41-223">html</span></span>|
|<span data-ttu-id="c8c41-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="c8c41-224">HTTP</span></span>|<span data-ttu-id="c8c41-225">http</span><span class="sxs-lookup"><span data-stu-id="c8c41-225">http</span></span>|
|<span data-ttu-id="c8c41-226">Java</span><span class="sxs-lookup"><span data-stu-id="c8c41-226">Java</span></span>|<span data-ttu-id="c8c41-227">java</span><span class="sxs-lookup"><span data-stu-id="c8c41-227">java</span></span>|
|<span data-ttu-id="c8c41-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="c8c41-228">JavaScript</span></span>|<span data-ttu-id="c8c41-229">javascript</span><span class="sxs-lookup"><span data-stu-id="c8c41-229">javascript</span></span>|
|<span data-ttu-id="c8c41-230">JSON</span><span class="sxs-lookup"><span data-stu-id="c8c41-230">JSON</span></span>|<span data-ttu-id="c8c41-231">json</span><span class="sxs-lookup"><span data-stu-id="c8c41-231">json</span></span>|
|<span data-ttu-id="c8c41-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-232">Markdown</span></span>|<span data-ttu-id="c8c41-233">md</span><span class="sxs-lookup"><span data-stu-id="c8c41-233">md</span></span>|
|<span data-ttu-id="c8c41-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="c8c41-234">NodeJS</span></span>|<span data-ttu-id="c8c41-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="c8c41-235">nodejs</span></span>|
|<span data-ttu-id="c8c41-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="c8c41-236">Objective-C</span></span>|<span data-ttu-id="c8c41-237">objc</span><span class="sxs-lookup"><span data-stu-id="c8c41-237">objc</span></span>|
|<span data-ttu-id="c8c41-238">OData</span><span class="sxs-lookup"><span data-stu-id="c8c41-238">OData</span></span>|<span data-ttu-id="c8c41-239">odata</span><span class="sxs-lookup"><span data-stu-id="c8c41-239">odata</span></span>|
|<span data-ttu-id="c8c41-240">PHP</span><span class="sxs-lookup"><span data-stu-id="c8c41-240">PHP</span></span>|<span data-ttu-id="c8c41-241">php</span><span class="sxs-lookup"><span data-stu-id="c8c41-241">php</span></span>|
|<span data-ttu-id="c8c41-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="c8c41-242">Power Apps Formula</span></span>|<span data-ttu-id="c8c41-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="c8c41-243">powerappsfl</span></span>|
|<span data-ttu-id="c8c41-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8c41-244">PowerShell</span></span>|<span data-ttu-id="c8c41-245">powershell</span><span class="sxs-lookup"><span data-stu-id="c8c41-245">powershell</span></span>|
|<span data-ttu-id="c8c41-246">Python</span><span class="sxs-lookup"><span data-stu-id="c8c41-246">Python</span></span>|<span data-ttu-id="c8c41-247">python</span><span class="sxs-lookup"><span data-stu-id="c8c41-247">python</span></span>|
|<span data-ttu-id="c8c41-248">Q#</span><span class="sxs-lookup"><span data-stu-id="c8c41-248">Q#</span></span>|<span data-ttu-id="c8c41-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="c8c41-249">qsharp</span></span>|
|<span data-ttu-id="c8c41-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="c8c41-250">Ruby</span></span>|<span data-ttu-id="c8c41-251">ruby</span><span class="sxs-lookup"><span data-stu-id="c8c41-251">ruby</span></span>|
|<span data-ttu-id="c8c41-252">SQL</span><span class="sxs-lookup"><span data-stu-id="c8c41-252">SQL</span></span>|<span data-ttu-id="c8c41-253">sql</span><span class="sxs-lookup"><span data-stu-id="c8c41-253">sql</span></span>|
|<span data-ttu-id="c8c41-254">Swift</span><span class="sxs-lookup"><span data-stu-id="c8c41-254">Swift</span></span>|<span data-ttu-id="c8c41-255">swift</span><span class="sxs-lookup"><span data-stu-id="c8c41-255">swift</span></span>|
|<span data-ttu-id="c8c41-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="c8c41-256">TypeScript</span></span>|<span data-ttu-id="c8c41-257">typescript</span><span class="sxs-lookup"><span data-stu-id="c8c41-257">typescript</span></span>|
|<span data-ttu-id="c8c41-258">VB</span><span class="sxs-lookup"><span data-stu-id="c8c41-258">VB</span></span>|<span data-ttu-id="c8c41-259">vb</span><span class="sxs-lookup"><span data-stu-id="c8c41-259">vb</span></span>|
|<span data-ttu-id="c8c41-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="c8c41-260">VSTS CLI</span></span>|<span data-ttu-id="c8c41-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="c8c41-261">vstscli</span></span>|
|<span data-ttu-id="c8c41-262">XAML</span><span class="sxs-lookup"><span data-stu-id="c8c41-262">XAML</span></span>|<span data-ttu-id="c8c41-263">xaml</span><span class="sxs-lookup"><span data-stu-id="c8c41-263">xaml</span></span>|
|<span data-ttu-id="c8c41-264">XML</span><span class="sxs-lookup"><span data-stu-id="c8c41-264">XML</span></span>|<span data-ttu-id="c8c41-265">xml</span><span class="sxs-lookup"><span data-stu-id="c8c41-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="c8c41-266">Exemple : C\#</span><span class="sxs-lookup"><span data-stu-id="c8c41-266">Example: C\#</span></span>

<span data-ttu-id="c8c41-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="c8c41-267">__Markdown__</span></span>

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

<span data-ttu-id="c8c41-268">__Render__</span><span class="sxs-lookup"><span data-stu-id="c8c41-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="c8c41-269">Exemple : SQL</span><span class="sxs-lookup"><span data-stu-id="c8c41-269">Example: SQL</span></span>

<span data-ttu-id="c8c41-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="c8c41-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="c8c41-271">__Render__</span><span class="sxs-lookup"><span data-stu-id="c8c41-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="c8c41-272">Extensions Markdown personnalisées OPS</span><span class="sxs-lookup"><span data-stu-id="c8c41-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="c8c41-273">OPS (Open Publishing Services) implémente un analyseur Markdig pour Markdown, qui est hautement compatible avec GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="c8c41-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="c8c41-274">Markdig ajoute des fonctionnalités via des extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="c8c41-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="c8c41-275">À ce titre, des articles sélectionnés du Guide de création OPS complet sont inclus dans ce guide pour référence.</span><span class="sxs-lookup"><span data-stu-id="c8c41-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="c8c41-276">(Par exemple, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.)</span><span class="sxs-lookup"><span data-stu-id="c8c41-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="c8c41-277">Les articles Docs utilisent GFM pour la majeure partie de la mise en forme des articles, comme les paragraphes, les liens, les listes et les en-têtes.</span><span class="sxs-lookup"><span data-stu-id="c8c41-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="c8c41-278">Pour une mise en forme plus riche, les articles peuvent utiliser des fonctionnalités Markdig comme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="c8c41-279">Des blocs de notes</span><span class="sxs-lookup"><span data-stu-id="c8c41-279">Note blocks</span></span>
- <span data-ttu-id="c8c41-280">Des includes</span><span class="sxs-lookup"><span data-stu-id="c8c41-280">Includes</span></span>
- <span data-ttu-id="c8c41-281">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="c8c41-281">Selectors</span></span>
- <span data-ttu-id="c8c41-282">Des vidéos intégrées</span><span class="sxs-lookup"><span data-stu-id="c8c41-282">Embedded videos</span></span>
- <span data-ttu-id="c8c41-283">Des exemples/extraits de code</span><span class="sxs-lookup"><span data-stu-id="c8c41-283">Code snippets/samples</span></span>

<span data-ttu-id="c8c41-284">Pour obtenir la liste complète, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.</span><span class="sxs-lookup"><span data-stu-id="c8c41-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="c8c41-285">Blocs de notes</span><span class="sxs-lookup"><span data-stu-id="c8c41-285">Note blocks</span></span>

<span data-ttu-id="c8c41-286">Vous pouvez choisir parmi quatre types de blocs de notes pour attirer l’attention sur du contenu spécifique :</span><span class="sxs-lookup"><span data-stu-id="c8c41-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="c8c41-287">REMARQUE</span><span class="sxs-lookup"><span data-stu-id="c8c41-287">NOTE</span></span>
- <span data-ttu-id="c8c41-288">AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="c8c41-288">WARNING</span></span>
- <span data-ttu-id="c8c41-289">CONSEIL</span><span class="sxs-lookup"><span data-stu-id="c8c41-289">TIP</span></span>
- <span data-ttu-id="c8c41-290">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="c8c41-290">IMPORTANT</span></span>

<span data-ttu-id="c8c41-291">En général, les blocs de notes doivent être utilisés avec parcimonie, car ils peuvent perturber la lecture.</span><span class="sxs-lookup"><span data-stu-id="c8c41-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="c8c41-292">Même s’ils prennent également en charge les blocs de code, les images, les listes et les liens, essayez de vous limiter à des blocs de notes simples et directs.</span><span class="sxs-lookup"><span data-stu-id="c8c41-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="c8c41-293">Includes</span><span class="sxs-lookup"><span data-stu-id="c8c41-293">Includes</span></span>

<span data-ttu-id="c8c41-294">Quand vous avez du texte ou des fichiers image réutilisables qui doivent être inclus dans des fichiers d’article, vous pouvez utiliser une référence vers le fichier « include » via la fonctionnalité d’inclusion de fichier de Markdig.</span><span class="sxs-lookup"><span data-stu-id="c8c41-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="c8c41-295">Cette fonctionnalité demande à OPS d’inclure le fichier dans votre fichier d’article lors de sa génération, ce qui en fait une partie de votre article publié.</span><span class="sxs-lookup"><span data-stu-id="c8c41-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="c8c41-296">Trois types d’includes sont disponibles pour vous aider à réutiliser du contenu :</span><span class="sxs-lookup"><span data-stu-id="c8c41-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="c8c41-297">Inline : pour réutiliser un extrait de texte commun au sein d’une autre phrase.</span><span class="sxs-lookup"><span data-stu-id="c8c41-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="c8c41-298">Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.</span><span class="sxs-lookup"><span data-stu-id="c8c41-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="c8c41-299">Image : il s’agit de la façon dont l’inclusion d’images standard est implémentée dans Docs.</span><span class="sxs-lookup"><span data-stu-id="c8c41-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="c8c41-300">Un include de type inline ou bloc est un simple fichier Markdown (.md).</span><span class="sxs-lookup"><span data-stu-id="c8c41-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="c8c41-301">Il peut contenir tout code Markdown valide.</span><span class="sxs-lookup"><span data-stu-id="c8c41-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="c8c41-302">Tous les fichiers Markdown include doivent être placés dans un [sous-répertoire `/includes` commun ](git-github-fundamentals.md#includes-subdirectory), à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="c8c41-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="c8c41-303">Quand l’article est publié, le fichier inclus y est intégré de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="c8c41-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="c8c41-304">Voici les conditions requises et éléments à prendre en compte pour les includes :</span><span class="sxs-lookup"><span data-stu-id="c8c41-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="c8c41-305">Utilisez les includes lorsque vous souhaitez que le même texte s'affiche dans plusieurs articles.</span><span class="sxs-lookup"><span data-stu-id="c8c41-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="c8c41-306">Utilisez des includes de blocs pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée.</span><span class="sxs-lookup"><span data-stu-id="c8c41-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="c8c41-307">Ne l'utilisez pas pour des éléments plus petits qu'une phrase.</span><span class="sxs-lookup"><span data-stu-id="c8c41-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="c8c41-308">Les includes ne s’afficheront pas dans la vue de votre article rendu par GitHub, car ils reposent sur des extensions Markdig.</span><span class="sxs-lookup"><span data-stu-id="c8c41-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="c8c41-309">Ils ne sont rendus qu’après publication.</span><span class="sxs-lookup"><span data-stu-id="c8c41-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="c8c41-310">Vérifiez que tout le texte dans un include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence l’include.</span><span class="sxs-lookup"><span data-stu-id="c8c41-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="c8c41-311">Ignorer cette instruction crée une chaîne intraduisible dans l'article, ce qui nuit à l'expérience localisée.</span><span class="sxs-lookup"><span data-stu-id="c8c41-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="c8c41-312">N'imbriquez pas d'includes dans d'autres includes.</span><span class="sxs-lookup"><span data-stu-id="c8c41-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="c8c41-313">Les groupes ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c8c41-313">They are not supported.</span></span>
- <span data-ttu-id="c8c41-314">Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="c8c41-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="c8c41-315">Le répertoire multimédia ne doit pas contenir d'images à sa racine.</span><span class="sxs-lookup"><span data-stu-id="c8c41-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="c8c41-316">Si l’include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire multimédia correspondant.</span><span class="sxs-lookup"><span data-stu-id="c8c41-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="c8c41-317">Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include.</span><span class="sxs-lookup"><span data-stu-id="c8c41-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="c8c41-318">Utilisez un fichier distinct avec un nom unique pour chaque include et article.</span><span class="sxs-lookup"><span data-stu-id="c8c41-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="c8c41-319">Stockez le fichier multimédia dans le dossier multimédia associé à l’include.</span><span class="sxs-lookup"><span data-stu-id="c8c41-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="c8c41-320">N'utilisez pas un include comme seul contenu d'un article.</span><span class="sxs-lookup"><span data-stu-id="c8c41-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="c8c41-321">Les includes sont censés compléter le contenu du reste de l'article.</span><span class="sxs-lookup"><span data-stu-id="c8c41-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="c8c41-322">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="c8c41-322">Selectors</span></span>

<span data-ttu-id="c8c41-323">Utilisez des sélecteurs dans les articles techniques lorsque vous créez plusieurs versions d'un même article, pour répondre aux différences d'implémentation à travers les technologies et plateformes.</span><span class="sxs-lookup"><span data-stu-id="c8c41-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="c8c41-324">Cela s'applique particulièrement au contenu pour plateformes mobiles pour développeurs.</span><span class="sxs-lookup"><span data-stu-id="c8c41-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="c8c41-325">Il existe actuellement deux types différents de sélecteurs dans Markdig, un sélecteur unique et un multi-sélecteur.</span><span class="sxs-lookup"><span data-stu-id="c8c41-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="c8c41-326">Le même Markdown de sélecteur allant dans chaque article de la sélection, nous vous recommandons de placer le sélecteur pour votre article dans un include.</span><span class="sxs-lookup"><span data-stu-id="c8c41-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="c8c41-327">Vous pouvez ensuite référencer ce dernier dans tous vos articles qui utilisent le même sélecteur.</span><span class="sxs-lookup"><span data-stu-id="c8c41-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="c8c41-328">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="c8c41-328">Code snippets</span></span>

<span data-ttu-id="c8c41-329">Markdig prend en charge l’inclusion avancée de code dans un article, via son extension d’extraits de code.</span><span class="sxs-lookup"><span data-stu-id="c8c41-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="c8c41-330">Elle fournit un rendu avancé qui se base sur les fonctionnalités de GFM comme la sélection du langage de programmation et la coloration de la syntaxe, plus des fonctionnalités intéressantes comme :</span><span class="sxs-lookup"><span data-stu-id="c8c41-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="c8c41-331">l’inclusion d’exemples/extraits de code centralisés depuis un dépôt externe ;</span><span class="sxs-lookup"><span data-stu-id="c8c41-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="c8c41-332">une interface à onglets pour présenter différentes versions des exemples de code dans différents langages.</span><span class="sxs-lookup"><span data-stu-id="c8c41-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="c8c41-333">Pièges et résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="c8c41-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="c8c41-334">Texte de remplacement</span><span class="sxs-lookup"><span data-stu-id="c8c41-334">Alt text</span></span>

<span data-ttu-id="c8c41-335">Le texte de remplacement qui contient des traits de soulignement ne s’affiche pas correctement.</span><span class="sxs-lookup"><span data-stu-id="c8c41-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="c8c41-336">Par exemple, au lieu d’utiliser ceci :</span><span class="sxs-lookup"><span data-stu-id="c8c41-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="c8c41-337">Placez les traits de soulignement dans une séquence d’échappement comme ceci :</span><span class="sxs-lookup"><span data-stu-id="c8c41-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="c8c41-338">Apostrophes et guillemets</span><span class="sxs-lookup"><span data-stu-id="c8c41-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="c8c41-339">Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes.</span><span class="sxs-lookup"><span data-stu-id="c8c41-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="c8c41-340">Vous devez les encoder ou les changer en apostrophes/guillemets de base.</span><span class="sxs-lookup"><span data-stu-id="c8c41-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="c8c41-341">Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="c8c41-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="c8c41-342">Voici les encodages pour les versions courbes de ces signes de ponctuation :</span><span class="sxs-lookup"><span data-stu-id="c8c41-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="c8c41-343">Guillemet gauche (ouvrant) : `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="c8c41-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="c8c41-344">Guillemet droit (fermant) : `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="c8c41-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="c8c41-345">Guillemet simple droit (fermant) ou apostrophe : `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="c8c41-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="c8c41-346">Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="c8c41-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="c8c41-347">Crochets pointus</span><span class="sxs-lookup"><span data-stu-id="c8c41-347">Angle brackets</span></span>

<span data-ttu-id="c8c41-348">Si vous utilisez des crochets pointus dans le texte (et non le code) de votre fichier, par exemple pour signaler un espace réservé, vous devez manuellement encoder les crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="c8c41-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="c8c41-349">Sinon, Markdown considère qu’il s’agit d’une balise HTML.</span><span class="sxs-lookup"><span data-stu-id="c8c41-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="c8c41-350">Par exemple, encodez `<script name>` en `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="c8c41-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="c8c41-351">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8c41-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="c8c41-352">Ressources Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-352">Markdown resources</span></span>

- [<span data-ttu-id="c8c41-353">Introduction à Markdown</span><span class="sxs-lookup"><span data-stu-id="c8c41-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="c8c41-354">Fiche récapitulative de Markdown pour Docs</span><span class="sxs-lookup"><span data-stu-id="c8c41-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="c8c41-355">Les bases du Markdown GitHub</span><span class="sxs-lookup"><span data-stu-id="c8c41-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
