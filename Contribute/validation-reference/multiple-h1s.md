---
title: multiple-h1
description: Explication et résolution du problème de génération Docs multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: a1006d9d75ebd53751c9ab81aa016d67d6e5df57
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848611"
---
# <a name="multiple-h1"></a><span data-ttu-id="b61a5-103">multiple-h1</span><span class="sxs-lookup"><span data-stu-id="b61a5-103">multiple-h1</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b61a5-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="b61a5-104">Suggestion</span></span>

`Multiple H1s are not allowed. You can only have one top-level heading.`

<span data-ttu-id="b61a5-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="b61a5-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="b61a5-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="b61a5-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="b61a5-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="b61a5-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="b61a5-108">Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="b61a5-108">You can only have one H1 in each file.</span></span>

## <a name="resolution"></a><span data-ttu-id="b61a5-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="b61a5-109">Resolution</span></span>

<span data-ttu-id="b61a5-110">Pour résoudre ce problème, changez le niveau des titres H1 suivants en H2 (`##`), ou bien réorganisez votre fichier.</span><span class="sxs-lookup"><span data-stu-id="b61a5-110">To fix this issue, change the heading level of subsequent H1s to H2 (`##`), or otherwise reorganize your file.</span></span> <span data-ttu-id="b61a5-111">Notez que passer des niveaux de titre, comme faire suivre H1 de H3, n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="b61a5-111">Note that skipping heading levels, such as following H1 with H3, is not allowed.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]