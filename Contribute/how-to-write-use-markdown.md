---
title: Guide pratique pour utiliser Markdown pour écrire du contenu Docs
description: Cet article fournit des informations de base et de référence sur le langage Markdown utilisé pour écrire des articles docs.microsoft.com.
ms.date: 07/13/2017
ms.openlocfilehash: 6bb8a1fa20957512addb07dda0e68abec4b0a83f
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805722"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="3f0f3-103">Guide pratique pour utiliser Markdown pour écrire du contenu Docs</span><span class="sxs-lookup"><span data-stu-id="3f0f3-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="3f0f3-104">Les articles [docs.microsoft.com](http://docs.microsoft.com) sont écrits dans un langage de balisage léger appelé [Markdown](https://daringfireball.net/projects/markdown/), à la fois facile à lire et facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="3f0f3-105">Ces qualités lui ont permis de s’établir rapidement comme une norme du secteur.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="3f0f3-106">Le contenu Docs étant stocké dans GitHub, il peut utiliser un sur-ensemble de Markdown appelé [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), qui offre des fonctionnalités supplémentaires pour les besoins de mise en forme courants.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="3f0f3-107">De plus, OPS (Open Publishing Services) implémente l’analyseur Markdown Markdig.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="3f0f3-108">Markdig est hautement compatible avec GFM et offre de nouvelles fonctions permettant d’utiliser des fonctionnalités propres à Docs.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="3f0f3-109">Markdig est un processeur Markdown rapide, performant, compatible CommonMark et extensible pour .NET.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="3f0f3-110">Meilleure prise en charge de la communauté</span><span class="sxs-lookup"><span data-stu-id="3f0f3-110">Better community support</span></span>
* <span data-ttu-id="3f0f3-111">Meilleure prise en charge des standards</span><span class="sxs-lookup"><span data-stu-id="3f0f3-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="3f0f3-112">Les bases de Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="3f0f3-113">En-têtes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-113">Headings</span></span>

<span data-ttu-id="3f0f3-114">Pour créer un en-tête, vous utilisez un dièse (#), comme suit :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="3f0f3-115">Texte en gras et italique</span><span class="sxs-lookup"><span data-stu-id="3f0f3-115">Bold and italic text</span></span>

<span data-ttu-id="3f0f3-116">Pour formater le texte en **gras**, vous l’entourez de deux astérisques :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="3f0f3-117">Pour formater le texte en *italique*, vous l’entourez d’un seul astérisque :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="3f0f3-118">Pour formater le texte en ***gras et en italique***, vous l’entourez de trois astérisques :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="3f0f3-119">Listes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="3f0f3-120">Liste non ordonnée</span><span class="sxs-lookup"><span data-stu-id="3f0f3-120">Unordered list</span></span>

<span data-ttu-id="3f0f3-121">Pour formater une liste à puces/non ordonnée, vous pouvez utiliser des astérisques ou des tirets.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="3f0f3-122">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="3f0f3-123">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-123">will be rendered as:</span></span>

- <span data-ttu-id="3f0f3-124">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="3f0f3-124">List item 1</span></span>
- <span data-ttu-id="3f0f3-125">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="3f0f3-125">List item 2</span></span>
- <span data-ttu-id="3f0f3-126">Élément de liste 3</span><span class="sxs-lookup"><span data-stu-id="3f0f3-126">List item 3</span></span>

<span data-ttu-id="3f0f3-127">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3f0f3-128">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="3f0f3-129">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-129">will be rendered as:</span></span>

- <span data-ttu-id="3f0f3-130">Élément de liste 1</span><span class="sxs-lookup"><span data-stu-id="3f0f3-130">List item 1</span></span>
  - <span data-ttu-id="3f0f3-131">Élément de liste A</span><span class="sxs-lookup"><span data-stu-id="3f0f3-131">List item A</span></span>
  - <span data-ttu-id="3f0f3-132">Élément de liste B</span><span class="sxs-lookup"><span data-stu-id="3f0f3-132">List item B</span></span>
- <span data-ttu-id="3f0f3-133">Élément de liste 2</span><span class="sxs-lookup"><span data-stu-id="3f0f3-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="3f0f3-134">Liste ordonnée</span><span class="sxs-lookup"><span data-stu-id="3f0f3-134">Ordered list</span></span>

<span data-ttu-id="3f0f3-135">Pour formater une liste ordonnée/d'étapes, vous utilisez les numéros correspondants.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="3f0f3-136">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="3f0f3-137">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-137">will be rendered as:</span></span>

1. <span data-ttu-id="3f0f3-138">Première instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-138">First instruction</span></span>
2. <span data-ttu-id="3f0f3-139">Deuxième instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-139">Second instruction</span></span>
3. <span data-ttu-id="3f0f3-140">Troisième instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-140">Third instruction</span></span>

<span data-ttu-id="3f0f3-141">Pour imbriquer une liste dans une autre, indentez les éléments de liste enfants.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="3f0f3-142">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="3f0f3-143">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-143">will be rendered as:</span></span>

1. <span data-ttu-id="3f0f3-144">Première instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-144">First instruction</span></span>
   1. <span data-ttu-id="3f0f3-145">Sous-instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-145">Sub-instruction</span></span>
   2. <span data-ttu-id="3f0f3-146">Sous-instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-146">Sub-instruction</span></span>
2. <span data-ttu-id="3f0f3-147">Deuxième instruction</span><span class="sxs-lookup"><span data-stu-id="3f0f3-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="3f0f3-148">les tableaux</span><span class="sxs-lookup"><span data-stu-id="3f0f3-148">Tables</span></span>

<span data-ttu-id="3f0f3-149">Les tableaux ne sont pas pris en charge par la spécification Markdown principale, mais ils sont pris en charge par GFM.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="3f0f3-150">Vous pouvez créer des tableaux avec la barre verticale (|) et le trait d’union (-).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="3f0f3-151">Les traits d’union servent à créer l’en-tête de chaque colonne, tandis que les barres verticales séparent chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="3f0f3-152">Ajoutez une ligne vide avant votre tableau pour qu’il s’affiche correctement.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="3f0f3-153">Par exemple, le code Markdown suivant :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="3f0f3-154">s’affichera sous la forme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-154">will be rendered as:</span></span>

| <span data-ttu-id="3f0f3-155">Amusez-vous</span><span class="sxs-lookup"><span data-stu-id="3f0f3-155">Fun</span></span>                  | <span data-ttu-id="3f0f3-156">avec</span><span class="sxs-lookup"><span data-stu-id="3f0f3-156">With</span></span>                 | <span data-ttu-id="3f0f3-157">les tableaux</span><span class="sxs-lookup"><span data-stu-id="3f0f3-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="3f0f3-158">colonne alignée à gauche</span><span class="sxs-lookup"><span data-stu-id="3f0f3-158">left-aligned column</span></span>  | <span data-ttu-id="3f0f3-159">colonne alignée à droite</span><span class="sxs-lookup"><span data-stu-id="3f0f3-159">right-aligned column</span></span> | <span data-ttu-id="3f0f3-160">colonne centrée</span><span class="sxs-lookup"><span data-stu-id="3f0f3-160">centered column</span></span> |
| <span data-ttu-id="3f0f3-161">100 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-161">$100</span></span>                 | <span data-ttu-id="3f0f3-162">100 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-162">$100</span></span>                 | <span data-ttu-id="3f0f3-163">100 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-163">$100</span></span>            |
| <span data-ttu-id="3f0f3-164">10 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-164">$10</span></span>                  | <span data-ttu-id="3f0f3-165">10 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-165">$10</span></span>                  | <span data-ttu-id="3f0f3-166">10 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-166">$10</span></span>             |
| <span data-ttu-id="3f0f3-167">1 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-167">$1</span></span>                   | <span data-ttu-id="3f0f3-168">1 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-168">$1</span></span>                   | <span data-ttu-id="3f0f3-169">1 $</span><span class="sxs-lookup"><span data-stu-id="3f0f3-169">$1</span></span>              |

<span data-ttu-id="3f0f3-170">Pour plus d'informations sur la création de tableaux, consultez :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="3f0f3-171">La [fonctionnalité de wrapping de tableaux](#table-wrapping) Markdig, qui peut vous aider à mettre en forme les tableaux larges.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="3f0f3-172">[Organisation des informations avec des tableaux](https://help.github.com/articles/organizing-information-with-tables/), de GitHub.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="3f0f3-173">L’application web [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="3f0f3-174">[« Markdown Cheatsheet » d’Adam Pritchard](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="3f0f3-175">[« Markdown Extra » de Michel Fortin](https://michelf.ca/projects/php-markdown/extra/#table).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="3f0f3-176">[Convertir les tableaux HTML en Markdown](https://jmalarcon.github.io/markdowntables/).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-176">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="3f0f3-177">Liens</span><span class="sxs-lookup"><span data-stu-id="3f0f3-177">Links</span></span>

<span data-ttu-id="3f0f3-178">La syntaxe Markdown pour un lien inline est composée d’une partie `[link text]`, qui est le texte du lien, suivie de la partie `(file-name.md)`, qui est l’URL ou le nom du fichier cible du lien :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="3f0f3-179">Pour plus d’informations sur la liaison, consultez :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-179">For more information on linking, see:</span></span>

- <span data-ttu-id="3f0f3-180">Le [Guide de syntaxe Markdown](https://daringfireball.net/projects/markdown/syntax#link) pour plus de détails sur la prise en charge des liens de base avec Markdown.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="3f0f3-181">La section [Liens](how-to-write-links.md) de ce guide pour plus de détails sur la syntaxe de liaison supplémentaire fournie par Markdig.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-181">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="3f0f3-182">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="3f0f3-182">Code snippets</span></span>

<span data-ttu-id="3f0f3-183">Markdown prend en charge le placement d’extraits de code à la fois inline dans une phrase et en tant que bloc « cloisonné » distinct entre les phrases.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="3f0f3-184">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-184">For details, see:</span></span>

- [<span data-ttu-id="3f0f3-185">Prise en charge native des blocs de code par Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-185">Markdown's native support for code blocks</span></span>](https://daringfireball.net/projects/markdown/syntax#precode)
- [<span data-ttu-id="3f0f3-186">Prise en charge du cloisonnement de code et du surlignage de la syntaxe par GFM</span><span class="sxs-lookup"><span data-stu-id="3f0f3-186">GFM support for code fencing and syntax highlighting</span></span>](https://help.github.com/articles/creating-and-highlighting-code-blocks/)

<span data-ttu-id="3f0f3-187">Les blocs de code cloisonnés sont un moyen facile de permettre le surlignage de la syntaxe de vos extraits de code.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="3f0f3-188">Le format général des blocs de code cloisonnés est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="3f0f3-189">L’alias après les trois caractères accent grave (\`) initiaux définit le surlignage de syntaxe à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="3f0f3-190">Vous trouverez ci-après une liste de langages de programmation couramment utilisés dans le contenu Docs et l’étiquette correspondante :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="3f0f3-191">Ces langages prennent en charge les noms conviviaux, et pour la plupart d’entre eux, la mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="3f0f3-192">Nom</span><span class="sxs-lookup"><span data-stu-id="3f0f3-192">Name</span></span>|<span data-ttu-id="3f0f3-193">Étiquette Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="3f0f3-194">.NET Console</span><span class="sxs-lookup"><span data-stu-id="3f0f3-194">.NET Console</span></span>|<span data-ttu-id="3f0f3-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="3f0f3-195">dotnetcli</span></span>|
|<span data-ttu-id="3f0f3-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="3f0f3-196">ASP.NET (C#)</span></span>|<span data-ttu-id="3f0f3-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="3f0f3-197">aspx-csharp</span></span>|
|<span data-ttu-id="3f0f3-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="3f0f3-198">ASP.NET (VB)</span></span>|<span data-ttu-id="3f0f3-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="3f0f3-199">aspx-vb</span></span>|
|<span data-ttu-id="3f0f3-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="3f0f3-200">AzCopy</span></span>|<span data-ttu-id="3f0f3-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="3f0f3-201">azcopy</span></span>|
|<span data-ttu-id="3f0f3-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="3f0f3-202">Azure CLI</span></span>|<span data-ttu-id="3f0f3-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="3f0f3-203">azurecli</span></span>|
|<span data-ttu-id="3f0f3-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3f0f3-204">Azure PowerShell</span></span>|<span data-ttu-id="3f0f3-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="3f0f3-205">azurepowershell</span></span>|
|<span data-ttu-id="3f0f3-206">C++</span><span class="sxs-lookup"><span data-stu-id="3f0f3-206">C++</span></span>|<span data-ttu-id="3f0f3-207">cpp</span><span class="sxs-lookup"><span data-stu-id="3f0f3-207">cpp</span></span>|
|<span data-ttu-id="3f0f3-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="3f0f3-208">C++/CX</span></span>|<span data-ttu-id="3f0f3-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="3f0f3-209">cppcx</span></span>|
|<span data-ttu-id="3f0f3-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="3f0f3-210">C++/WinRT</span></span>|<span data-ttu-id="3f0f3-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="3f0f3-211">cppwinrt</span></span>|
|<span data-ttu-id="3f0f3-212">C#</span><span class="sxs-lookup"><span data-stu-id="3f0f3-212">C#</span></span>|<span data-ttu-id="3f0f3-213">csharp</span><span class="sxs-lookup"><span data-stu-id="3f0f3-213">csharp</span></span>|
|<span data-ttu-id="3f0f3-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="3f0f3-214">CSHTML</span></span>|<span data-ttu-id="3f0f3-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="3f0f3-215">cshtml</span></span>|
|<span data-ttu-id="3f0f3-216">DAX</span><span class="sxs-lookup"><span data-stu-id="3f0f3-216">DAX</span></span>|<span data-ttu-id="3f0f3-217">dax</span><span class="sxs-lookup"><span data-stu-id="3f0f3-217">dax</span></span>|
|<span data-ttu-id="3f0f3-218">F#</span><span class="sxs-lookup"><span data-stu-id="3f0f3-218">F#</span></span>|<span data-ttu-id="3f0f3-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="3f0f3-219">fsharp</span></span>|
|<span data-ttu-id="3f0f3-220">Go</span><span class="sxs-lookup"><span data-stu-id="3f0f3-220">Go</span></span>|<span data-ttu-id="3f0f3-221">go</span><span class="sxs-lookup"><span data-stu-id="3f0f3-221">go</span></span>|
|<span data-ttu-id="3f0f3-222">HTML</span><span class="sxs-lookup"><span data-stu-id="3f0f3-222">HTML</span></span>|<span data-ttu-id="3f0f3-223">html</span><span class="sxs-lookup"><span data-stu-id="3f0f3-223">html</span></span>|
|<span data-ttu-id="3f0f3-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="3f0f3-224">HTTP</span></span>|<span data-ttu-id="3f0f3-225">http</span><span class="sxs-lookup"><span data-stu-id="3f0f3-225">http</span></span>|
|<span data-ttu-id="3f0f3-226">Java</span><span class="sxs-lookup"><span data-stu-id="3f0f3-226">Java</span></span>|<span data-ttu-id="3f0f3-227">java</span><span class="sxs-lookup"><span data-stu-id="3f0f3-227">java</span></span>|
|<span data-ttu-id="3f0f3-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="3f0f3-228">JavaScript</span></span>|<span data-ttu-id="3f0f3-229">javascript</span><span class="sxs-lookup"><span data-stu-id="3f0f3-229">javascript</span></span>|
|<span data-ttu-id="3f0f3-230">JSON</span><span class="sxs-lookup"><span data-stu-id="3f0f3-230">JSON</span></span>|<span data-ttu-id="3f0f3-231">json</span><span class="sxs-lookup"><span data-stu-id="3f0f3-231">json</span></span>|
|<span data-ttu-id="3f0f3-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-232">Markdown</span></span>|<span data-ttu-id="3f0f3-233">md</span><span class="sxs-lookup"><span data-stu-id="3f0f3-233">md</span></span>|
|<span data-ttu-id="3f0f3-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="3f0f3-234">NodeJS</span></span>|<span data-ttu-id="3f0f3-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="3f0f3-235">nodejs</span></span>|
|<span data-ttu-id="3f0f3-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="3f0f3-236">Objective-C</span></span>|<span data-ttu-id="3f0f3-237">objc</span><span class="sxs-lookup"><span data-stu-id="3f0f3-237">objc</span></span>|
|<span data-ttu-id="3f0f3-238">OData</span><span class="sxs-lookup"><span data-stu-id="3f0f3-238">OData</span></span>|<span data-ttu-id="3f0f3-239">odata</span><span class="sxs-lookup"><span data-stu-id="3f0f3-239">odata</span></span>|
|<span data-ttu-id="3f0f3-240">PHP</span><span class="sxs-lookup"><span data-stu-id="3f0f3-240">PHP</span></span>|<span data-ttu-id="3f0f3-241">php</span><span class="sxs-lookup"><span data-stu-id="3f0f3-241">php</span></span>|
|<span data-ttu-id="3f0f3-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="3f0f3-242">Power Apps Formula</span></span>|<span data-ttu-id="3f0f3-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="3f0f3-243">powerappsfl</span></span>|
|<span data-ttu-id="3f0f3-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="3f0f3-244">PowerShell</span></span>|<span data-ttu-id="3f0f3-245">powershell</span><span class="sxs-lookup"><span data-stu-id="3f0f3-245">powershell</span></span>|
|<span data-ttu-id="3f0f3-246">Python</span><span class="sxs-lookup"><span data-stu-id="3f0f3-246">Python</span></span>|<span data-ttu-id="3f0f3-247">python</span><span class="sxs-lookup"><span data-stu-id="3f0f3-247">python</span></span>|
|<span data-ttu-id="3f0f3-248">Q#</span><span class="sxs-lookup"><span data-stu-id="3f0f3-248">Q#</span></span>|<span data-ttu-id="3f0f3-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="3f0f3-249">qsharp</span></span>|
|<span data-ttu-id="3f0f3-250">R</span><span class="sxs-lookup"><span data-stu-id="3f0f3-250">R</span></span>|<span data-ttu-id="3f0f3-251">r</span><span class="sxs-lookup"><span data-stu-id="3f0f3-251">r</span></span>|
|<span data-ttu-id="3f0f3-252">Ruby</span><span class="sxs-lookup"><span data-stu-id="3f0f3-252">Ruby</span></span>|<span data-ttu-id="3f0f3-253">ruby</span><span class="sxs-lookup"><span data-stu-id="3f0f3-253">ruby</span></span>|
|<span data-ttu-id="3f0f3-254">SQL</span><span class="sxs-lookup"><span data-stu-id="3f0f3-254">SQL</span></span>|<span data-ttu-id="3f0f3-255">sql</span><span class="sxs-lookup"><span data-stu-id="3f0f3-255">sql</span></span>|
|<span data-ttu-id="3f0f3-256">Swift</span><span class="sxs-lookup"><span data-stu-id="3f0f3-256">Swift</span></span>|<span data-ttu-id="3f0f3-257">swift</span><span class="sxs-lookup"><span data-stu-id="3f0f3-257">swift</span></span>|
|<span data-ttu-id="3f0f3-258">TypeScript</span><span class="sxs-lookup"><span data-stu-id="3f0f3-258">TypeScript</span></span>|<span data-ttu-id="3f0f3-259">typescript</span><span class="sxs-lookup"><span data-stu-id="3f0f3-259">typescript</span></span>|
|<span data-ttu-id="3f0f3-260">VB</span><span class="sxs-lookup"><span data-stu-id="3f0f3-260">VB</span></span>|<span data-ttu-id="3f0f3-261">vb</span><span class="sxs-lookup"><span data-stu-id="3f0f3-261">vb</span></span>|
|<span data-ttu-id="3f0f3-262">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="3f0f3-262">VSTS CLI</span></span>|<span data-ttu-id="3f0f3-263">vstscli</span><span class="sxs-lookup"><span data-stu-id="3f0f3-263">vstscli</span></span>|
|<span data-ttu-id="3f0f3-264">XAML</span><span class="sxs-lookup"><span data-stu-id="3f0f3-264">XAML</span></span>|<span data-ttu-id="3f0f3-265">xaml</span><span class="sxs-lookup"><span data-stu-id="3f0f3-265">xaml</span></span>|
|<span data-ttu-id="3f0f3-266">XML</span><span class="sxs-lookup"><span data-stu-id="3f0f3-266">XML</span></span>|<span data-ttu-id="3f0f3-267">xml</span><span class="sxs-lookup"><span data-stu-id="3f0f3-267">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="3f0f3-268">Exemple : C\#</span><span class="sxs-lookup"><span data-stu-id="3f0f3-268">Example: C\#</span></span>

<span data-ttu-id="3f0f3-269">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3f0f3-269">__Markdown__</span></span>

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

<span data-ttu-id="3f0f3-270">__Render__</span><span class="sxs-lookup"><span data-stu-id="3f0f3-270">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="3f0f3-271">Exemple : SQL</span><span class="sxs-lookup"><span data-stu-id="3f0f3-271">Example: SQL</span></span>

<span data-ttu-id="3f0f3-272">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="3f0f3-272">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="3f0f3-273">__Render__</span><span class="sxs-lookup"><span data-stu-id="3f0f3-273">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="3f0f3-274">Extensions Markdown personnalisées OPS</span><span class="sxs-lookup"><span data-stu-id="3f0f3-274">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="3f0f3-275">OPS (Open Publishing Services) implémente un analyseur Markdig pour Markdown, qui est hautement compatible avec GFM (GitHub Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-275">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="3f0f3-276">Markdig ajoute des fonctionnalités via des extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-276">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="3f0f3-277">À ce titre, des articles sélectionnés du Guide de création OPS complet sont inclus dans ce guide pour référence.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-277">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="3f0f3-278">(Par exemple, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.)</span><span class="sxs-lookup"><span data-stu-id="3f0f3-278">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="3f0f3-279">Les articles Docs utilisent GFM pour la majeure partie de la mise en forme des articles, comme les paragraphes, les liens, les listes et les en-têtes.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-279">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="3f0f3-280">Pour une mise en forme plus riche, les articles peuvent utiliser des fonctionnalités Markdig comme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-280">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="3f0f3-281">Blocs de notes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-281">Note blocks</span></span>
- <span data-ttu-id="3f0f3-282">Des includes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-282">Includes</span></span>
- <span data-ttu-id="3f0f3-283">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="3f0f3-283">Selectors</span></span>
- <span data-ttu-id="3f0f3-284">Des vidéos intégrées</span><span class="sxs-lookup"><span data-stu-id="3f0f3-284">Embedded videos</span></span>
- <span data-ttu-id="3f0f3-285">Des exemples/extraits de code</span><span class="sxs-lookup"><span data-stu-id="3f0f3-285">Code snippets/samples</span></span>

<span data-ttu-id="3f0f3-286">Pour obtenir la liste complète, consultez « Extensions Markdown et Markdig » et « Extraits de code » dans la table des matières.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-286">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="3f0f3-287">Blocs de notes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-287">Note blocks</span></span>

<span data-ttu-id="3f0f3-288">Vous pouvez choisir parmi quatre types de blocs de notes pour attirer l’attention sur du contenu spécifique :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-288">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="3f0f3-289">REMARQUE</span><span class="sxs-lookup"><span data-stu-id="3f0f3-289">NOTE</span></span>
- <span data-ttu-id="3f0f3-290">AVERTISSEMENT</span><span class="sxs-lookup"><span data-stu-id="3f0f3-290">WARNING</span></span>
- <span data-ttu-id="3f0f3-291">CONSEIL</span><span class="sxs-lookup"><span data-stu-id="3f0f3-291">TIP</span></span>
- <span data-ttu-id="3f0f3-292">IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="3f0f3-292">IMPORTANT</span></span>

<span data-ttu-id="3f0f3-293">En général, les blocs de notes doivent être utilisés avec parcimonie, car ils peuvent perturber la lecture.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-293">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="3f0f3-294">Même s’ils prennent également en charge les blocs de code, les images, les listes et les liens, essayez de vous limiter à des blocs de notes simples et directs.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-294">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="3f0f3-295">Includes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-295">Includes</span></span>

<span data-ttu-id="3f0f3-296">Quand vous avez du texte ou des fichiers image réutilisables qui doivent être inclus dans des fichiers d’article, vous pouvez utiliser une référence vers le fichier « include » via la fonctionnalité d’inclusion de fichier de Markdig.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-296">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="3f0f3-297">Cette fonctionnalité demande à OPS d’inclure le fichier dans votre fichier d’article lors de sa génération, ce qui en fait une partie de votre article publié.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-297">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="3f0f3-298">Trois types d’includes sont disponibles pour vous aider à réutiliser du contenu :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-298">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="3f0f3-299">Inline : pour réutiliser un extrait de texte commun au sein d’une autre phrase.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-299">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="3f0f3-300">Bloc : pour réutiliser un fichier Markdown entier en tant que bloc, imbriqué dans une section d’un article.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-300">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="3f0f3-301">Image : il s’agit de la façon dont l’inclusion d’images standard est implémentée dans Docs.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-301">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="3f0f3-302">Un include de type inline ou bloc est un simple fichier Markdown (.md).</span><span class="sxs-lookup"><span data-stu-id="3f0f3-302">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="3f0f3-303">Il peut contenir tout code Markdown valide.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-303">It can contain any valid Markdown.</span></span> <span data-ttu-id="3f0f3-304">Tous les fichiers Markdown include doivent être placés dans un [sous-répertoire `/includes` commun ](git-github-fundamentals.md#includes-subdirectory), à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-304">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="3f0f3-305">Quand l’article est publié, le fichier inclus y est intégré de façon transparente.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-305">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="3f0f3-306">Voici les conditions requises et éléments à prendre en compte pour les includes :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-306">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="3f0f3-307">Utilisez les includes lorsque vous souhaitez que le même texte s'affiche dans plusieurs articles.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-307">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="3f0f3-308">Utilisez des includes de blocs pour les quantités significatives de contenu : un paragraphe ou deux, une procédure partagée ou une section partagée.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-308">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="3f0f3-309">Ne l'utilisez pas pour des éléments plus petits qu'une phrase.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-309">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="3f0f3-310">Les includes ne s’afficheront pas dans la vue de votre article rendu par GitHub, car ils reposent sur des extensions Markdig.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-310">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="3f0f3-311">Ils ne sont rendus qu’après publication.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-311">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="3f0f3-312">Vérifiez que tout le texte dans un include est écrit par phrases complètes ne dépendant pas du texte précédent ni suivant dans l’article qui référence l’include.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-312">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="3f0f3-313">Ignorer cette instruction crée une chaîne intraduisible dans l'article, ce qui nuit à l'expérience localisée.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-313">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="3f0f3-314">N'imbriquez pas d'includes dans d'autres includes.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-314">Don't embed includes within other includes.</span></span> <span data-ttu-id="3f0f3-315">Les groupes ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-315">They are not supported.</span></span>
- <span data-ttu-id="3f0f3-316">Placez les fichiers multimédias dans un dossier multimédia propre au sous-répertoire d’includes, par exemple le dossier `<repo>`/includes/media.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-316">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="3f0f3-317">Le répertoire multimédia ne doit pas contenir d'images à sa racine.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-317">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="3f0f3-318">Si l’include ne contient pas d’images, il n’est pas nécessaire d’utiliser un répertoire multimédia correspondant.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-318">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="3f0f3-319">Comme pour les articles ordinaires, ne partagez pas de fichiers multimédias entre fichiers include.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-319">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="3f0f3-320">Utilisez un fichier distinct avec un nom unique pour chaque include et article.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-320">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="3f0f3-321">Stockez le fichier multimédia dans le dossier multimédia associé à l’include.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-321">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="3f0f3-322">N'utilisez pas un include comme seul contenu d'un article.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-322">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="3f0f3-323">Les includes sont censés compléter le contenu du reste de l'article.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-323">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="3f0f3-324">Des sélecteurs</span><span class="sxs-lookup"><span data-stu-id="3f0f3-324">Selectors</span></span>

<span data-ttu-id="3f0f3-325">Utilisez des sélecteurs dans les articles techniques lorsque vous créez plusieurs versions d'un même article, pour répondre aux différences d'implémentation à travers les technologies et plateformes.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-325">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="3f0f3-326">Cela s'applique particulièrement au contenu pour plateformes mobiles pour développeurs.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-326">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="3f0f3-327">Il existe actuellement deux types différents de sélecteurs dans Markdig, un sélecteur unique et un multi-sélecteur.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-327">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="3f0f3-328">Le même Markdown de sélecteur allant dans chaque article de la sélection, nous vous recommandons de placer le sélecteur pour votre article dans un include.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-328">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="3f0f3-329">Vous pouvez ensuite référencer ce dernier dans tous vos articles qui utilisent le même sélecteur.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-329">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="3f0f3-330">Extraits de code</span><span class="sxs-lookup"><span data-stu-id="3f0f3-330">Code snippets</span></span>

<span data-ttu-id="3f0f3-331">Markdig prend en charge l’inclusion avancée de code dans un article, via son extension d’extraits de code.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-331">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="3f0f3-332">Elle fournit un rendu avancé qui se base sur les fonctionnalités de GFM comme la sélection du langage de programmation et la coloration de la syntaxe, plus des fonctionnalités intéressantes comme :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-332">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="3f0f3-333">l’inclusion d’exemples/extraits de code centralisés depuis un dépôt externe ;</span><span class="sxs-lookup"><span data-stu-id="3f0f3-333">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="3f0f3-334">une interface à onglets pour présenter différentes versions des exemples de code dans différents langages.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-334">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="3f0f3-335">Pièges et résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="3f0f3-335">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="3f0f3-336">Texte de remplacement</span><span class="sxs-lookup"><span data-stu-id="3f0f3-336">Alt text</span></span>

<span data-ttu-id="3f0f3-337">Le texte de remplacement qui contient des traits de soulignement ne s’affiche pas correctement.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-337">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="3f0f3-338">Par exemple, au lieu d’utiliser ceci :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-338">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="3f0f3-339">Placez les traits de soulignement dans une séquence d’échappement comme ceci :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-339">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="3f0f3-340">Apostrophes et guillemets</span><span class="sxs-lookup"><span data-stu-id="3f0f3-340">Apostrophes and quotation marks</span></span>

<span data-ttu-id="3f0f3-341">Si vous copiez de Word dans un éditeur Markdown, le texte peut contenir des apostrophes ou guillemets courbes.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-341">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="3f0f3-342">Vous devez les encoder ou les changer en apostrophes/guillemets de base.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-342">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span>
<span data-ttu-id="3f0f3-343">Sinon, vous verrez des choses semblables à ceci une fois le fichier publié : Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="3f0f3-343">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="3f0f3-344">Voici les encodages pour les versions courbes de ces signes de ponctuation :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-344">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="3f0f3-345">Guillemet gauche (ouvrant) : `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="3f0f3-345">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="3f0f3-346">Guillemet droit (fermant) : `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="3f0f3-346">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="3f0f3-347">Guillemet simple droit (fermant) ou apostrophe : `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="3f0f3-347">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="3f0f3-348">Guillemet simple gauche (ouvrant), rarement utilisé : `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="3f0f3-348">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="3f0f3-349">Crochets pointus</span><span class="sxs-lookup"><span data-stu-id="3f0f3-349">Angle brackets</span></span>

<span data-ttu-id="3f0f3-350">Il est courant d’utiliser des crochets pointus pour indiquer un espace réservé.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-350">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="3f0f3-351">Quand vous effectuez cette opération dans un texte (pas dans du code), vous devez encoder les crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-351">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="3f0f3-352">Sinon, Markdown considère qu’il s’agit d’une balise HTML.</span><span class="sxs-lookup"><span data-stu-id="3f0f3-352">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="3f0f3-353">Par exemple, encodez `<script name>` en `&lt;script name&gt;`</span><span class="sxs-lookup"><span data-stu-id="3f0f3-353">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="3f0f3-354">Voir aussi :</span><span class="sxs-lookup"><span data-stu-id="3f0f3-354">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="3f0f3-355">Ressources Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-355">Markdown resources</span></span>

- [<span data-ttu-id="3f0f3-356">Introduction à Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-356">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="3f0f3-357">Fiche récapitulative de Markdown pour Docs</span><span class="sxs-lookup"><span data-stu-id="3f0f3-357">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="3f0f3-358">Les bases du Markdown GitHub</span><span class="sxs-lookup"><span data-stu-id="3f0f3-358">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="3f0f3-359">Guide de Markdown</span><span class="sxs-lookup"><span data-stu-id="3f0f3-359">The Markdown Guide</span></span>](https://www.markdownguide.org/)
