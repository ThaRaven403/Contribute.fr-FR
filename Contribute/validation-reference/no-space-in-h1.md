---
title: no-space-in-h1
description: Explication et résolution du problème de génération Docs no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427502"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="c0d29-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="c0d29-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="c0d29-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="c0d29-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="c0d29-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="c0d29-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="c0d29-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="c0d29-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="c0d29-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="c0d29-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="c0d29-108">Sans l’espace après le dièse, Docs ne reconnaît pas un titre H1.</span><span class="sxs-lookup"><span data-stu-id="c0d29-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="c0d29-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="c0d29-109">Resolution</span></span>

<span data-ttu-id="c0d29-110">Pour corriger cette erreur, ajoutez un espace après le dièse dans votre titre H1.</span><span class="sxs-lookup"><span data-stu-id="c0d29-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]