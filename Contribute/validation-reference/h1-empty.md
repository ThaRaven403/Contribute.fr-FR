---
title: h1-empty
description: Explication et résolution du problème de génération Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: d0b3ab2206d66ff68a967d7868353b5b399da80a
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528808"
---
# <a name="h1-empty"></a><span data-ttu-id="a2d80-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="a2d80-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="a2d80-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a2d80-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="a2d80-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="a2d80-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a2d80-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="a2d80-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="a2d80-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="a2d80-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2d80-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="a2d80-108">Resolution</span></span>

<span data-ttu-id="a2d80-109">Pour résoudre ce problème, vérifiez que votre titre H1 inclut du contenu, et pas seulement un dièse.</span><span class="sxs-lookup"><span data-stu-id="a2d80-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="a2d80-110">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="a2d80-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="a2d80-111">Correct :</span><span class="sxs-lookup"><span data-stu-id="a2d80-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
