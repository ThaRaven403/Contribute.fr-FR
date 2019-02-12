---
title: ms-date-too-late
description: Explication et résolution du problème de génération de documents ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713105"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="7ce55-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="7ce55-103">ms-date-too-late</span></span>

<span data-ttu-id="7ce55-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="7ce55-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="7ce55-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="7ce55-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="7ce55-106">L’attribut `ms.date` est utilisé pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article.</span><span class="sxs-lookup"><span data-stu-id="7ce55-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="7ce55-107">La date ne peut donc pas être postérieure à la date du jour.</span><span class="sxs-lookup"><span data-stu-id="7ce55-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="7ce55-108">Cinq jours sont autorisés pour prendre en compte le délai de publication, comme quand le contenu est figé pour le QA en préparation d’un événement majeur.</span><span class="sxs-lookup"><span data-stu-id="7ce55-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ce55-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="7ce55-109">Resolution</span></span>

<span data-ttu-id="7ce55-110">Spécifiez `ms.date` qui ne se situe pas dans plus de cinq jour par rapport à aujourd’hui, au format MM/JJ/AAAA.</span><span class="sxs-lookup"><span data-stu-id="7ce55-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
