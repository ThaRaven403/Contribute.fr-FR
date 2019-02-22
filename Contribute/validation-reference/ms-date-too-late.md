---
title: ms-date-too-late
description: Explication et résolution du problème de génération de documents ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431481"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="a143c-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="a143c-103">ms-date-too-late</span></span>

<span data-ttu-id="a143c-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="a143c-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="a143c-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a143c-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="a143c-106">L’attribut `ms.date` est utilisé pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article.</span><span class="sxs-lookup"><span data-stu-id="a143c-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a143c-107">La date ne peut donc pas être postérieure à la date du jour.</span><span class="sxs-lookup"><span data-stu-id="a143c-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="a143c-108">Cinq jours sont autorisés pour prendre en compte le délai de publication, comme quand le contenu est figé pour le QA en préparation d’un événement majeur.</span><span class="sxs-lookup"><span data-stu-id="a143c-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="a143c-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="a143c-109">Resolution</span></span>

<span data-ttu-id="a143c-110">Spécifiez `ms.date` qui ne se situe pas dans plus de cinq jour par rapport à aujourd’hui, au format MM/JJ/AAAA :</span><span class="sxs-lookup"><span data-stu-id="a143c-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
