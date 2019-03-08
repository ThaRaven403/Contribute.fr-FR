---
title: manager-missing
description: Explication et résolution du problème de génération Docs manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427490"
---
# <a name="manager-missing"></a><span data-ttu-id="9f510-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="9f510-103">manager-missing</span></span>

<span data-ttu-id="9f510-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="9f510-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9f510-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="9f510-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="9f510-106">Certains groupes de contenus nécessitent l’attribut `manager` pour identifier le responsable de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="9f510-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="9f510-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="9f510-107">Resolution</span></span>

<span data-ttu-id="9f510-108">Ajoutez un alias Microsoft valide pour `manager` :</span><span class="sxs-lookup"><span data-stu-id="9f510-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
