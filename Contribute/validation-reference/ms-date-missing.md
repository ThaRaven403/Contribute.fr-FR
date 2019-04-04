---
title: ms-date-missing
description: Explication et résolution du problème de génération de documents ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637273"
---
# <a name="ms-date-missing"></a><span data-ttu-id="891c7-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="891c7-103">ms-date-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="891c7-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="891c7-104">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="891c7-105">Certains groupes de contenus nécessitent une `ms.date` pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article.</span><span class="sxs-lookup"><span data-stu-id="891c7-105">Some content groups require `ms.date` to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="891c7-106">Cela ne correspond pas à la dernière date à laquelle l’article a été *publié*, qui s’affiche sur la page si `ms.date` n’est pas explicitement spécifié.</span><span class="sxs-lookup"><span data-stu-id="891c7-106">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="891c7-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="891c7-107">Resolution</span></span>

<span data-ttu-id="891c7-108">Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA :</span><span class="sxs-lookup"><span data-stu-id="891c7-108">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
