---
title: ms-date-missing
description: Explication et résolution du problème de génération de documents ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713243"
---
# <a name="ms-date-missing"></a><span data-ttu-id="a1bfa-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="a1bfa-103">ms-date-missing</span></span>

<span data-ttu-id="a1bfa-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="a1bfa-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a1bfa-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="a1bfa-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="a1bfa-106">La date est utilisée pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article.</span><span class="sxs-lookup"><span data-stu-id="a1bfa-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="a1bfa-107">Cela ne correspond pas à la dernière date à laquelle l’article a été *publié*, qui s’affiche sur la page si `ms.date` n’est pas explicitement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a1bfa-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1bfa-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="a1bfa-108">Resolution</span></span>

<span data-ttu-id="a1bfa-109">Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA.</span><span class="sxs-lookup"><span data-stu-id="a1bfa-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
