---
title: h1-empty
description: Explication et résolution du problème de génération Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427412"
---
# <a name="h1-empty"></a><span data-ttu-id="a7761-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="a7761-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="a7761-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a7761-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="a7761-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="a7761-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a7761-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="a7761-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="a7761-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="a7761-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="a7761-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="a7761-108">Resolution</span></span>

<span data-ttu-id="a7761-109">Pour résoudre ce problème, vérifiez que votre titre H1 inclut du contenu, et pas seulement un dièse.</span><span class="sxs-lookup"><span data-stu-id="a7761-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="a7761-110">Incorrect :</span><span class="sxs-lookup"><span data-stu-id="a7761-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="a7761-111">Correct :</span><span class="sxs-lookup"><span data-stu-id="a7761-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]