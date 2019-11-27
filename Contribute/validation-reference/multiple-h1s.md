---
title: multiple-h1s
description: Explication et résolution du problème de génération de la documentation multiple-h1s.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528938"
---
# <a name="multiple-h1s"></a><span data-ttu-id="512c1-103">multiple-h1s</span><span class="sxs-lookup"><span data-stu-id="512c1-103">multiple-h1s</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="512c1-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="512c1-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="512c1-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="512c1-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="512c1-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="512c1-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="512c1-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="512c1-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="512c1-108">Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="512c1-108">You can only have one H1 in each file.</span></span>

<span data-ttu-id="512c1-109">Vous pouvez également recevoir ce message si votre article contient une ligne de signe « égal » constituant un double soulignement, comme ceci : `=======`.</span><span class="sxs-lookup"><span data-stu-id="512c1-109">You might also get this message if your article contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="512c1-110">Il s’agit d’une syntaxe Markdown alternative pour un titre H1.</span><span class="sxs-lookup"><span data-stu-id="512c1-110">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="512c1-111">Il apparaît aussi souvent dans les conflits de fusion :</span><span class="sxs-lookup"><span data-stu-id="512c1-111">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="512c1-112">Résolution</span><span class="sxs-lookup"><span data-stu-id="512c1-112">Resolution</span></span>

<span data-ttu-id="512c1-113">Pour résoudre ce problème, changez le niveau des titres H1 suivants en H2 (`##`), ou bien réorganisez votre fichier.</span><span class="sxs-lookup"><span data-stu-id="512c1-113">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="512c1-114">Notez que passer des niveaux de titre, comme faire suivre H1 de H3, n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="512c1-114">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<span data-ttu-id="512c1-115">Si un titre H1 supplémentaire est en fait un double soulignement (`=======`), supprimez-le ou remplacez-le par un titre de mot-dièse, comme `##`, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="512c1-115">If an additional H1 is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="512c1-116">Si le double soulignement est impliqué dans un conflit de fusion, veillez également à supprimer les marqueurs de début et de fin du conflit de fusion, et le texte obsolète.</span><span class="sxs-lookup"><span data-stu-id="512c1-116">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
