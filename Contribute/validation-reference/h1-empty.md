---
title: h1-empty
description: Explication et résolution du problème de génération Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 691d72a3aee9204ba3fe55a398e954c7719f3680
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848551"
---
# <a name="h1-empty"></a><span data-ttu-id="5d4c5-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="5d4c5-103">h1-empty</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5d4c5-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5d4c5-104">Suggestion</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="5d4c5-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="5d4c5-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5d4c5-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="5d4c5-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5d4c5-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="5d4c5-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="5d4c5-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d4c5-108">Resolution</span></span>

<span data-ttu-id="5d4c5-109">Pour résoudre ce problème, vérifiez que votre titre H1 inclut du contenu, et pas seulement un dièse.</span><span class="sxs-lookup"><span data-stu-id="5d4c5-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="5d4c5-110">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="5d4c5-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="5d4c5-111">Correct :</span><span class="sxs-lookup"><span data-stu-id="5d4c5-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]