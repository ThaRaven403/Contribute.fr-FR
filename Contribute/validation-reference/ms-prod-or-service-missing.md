---
title: ms-prod-or-service-missing
description: Explication et résolution du problème de génération de documents ms-prod-or-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: f4d5bc7537ec851ce7ac1de3be2208fd74cbe37f
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713542"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="9764c-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="9764c-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="9764c-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="9764c-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9764c-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="9764c-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="9764c-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="9764c-106">Resolution</span></span>

<span data-ttu-id="9764c-107">`ms.prod` ou `ms.service` est requis, et les deux valeurs ne peuvent pas être présentes : `ms.prod` est utilisé pour les produits sur site ; `ms.service` est utilisé pour les services cloud.</span><span class="sxs-lookup"><span data-stu-id="9764c-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="9764c-108">Déterminez la valeur appropriée pour votre article, vérifiez que la valeur est correcte et supprimez l’autre champ.</span><span class="sxs-lookup"><span data-stu-id="9764c-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="9764c-109">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="9764c-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]