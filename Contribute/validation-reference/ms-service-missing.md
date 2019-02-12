---
title: ms-service-missing
description: Explication et résolution du problème de génération de documents ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713082"
---
# <a name="ms-service-missing"></a><span data-ttu-id="783f7-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="783f7-103">ms-service-missing</span></span>

<span data-ttu-id="783f7-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="783f7-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="783f7-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="783f7-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="783f7-106">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="783f7-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="783f7-107">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`, mais si vous spécifiez `ms.subservice`, vous devez aussi spécifier `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="783f7-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="783f7-108">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="783f7-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="783f7-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="783f7-109">Resolution</span></span>

<span data-ttu-id="783f7-110">Confirmez que la valeur `ms.subservice` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="783f7-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="783f7-111">Puis, ajoutez la valeur `ms.service` appropriée qui est un parent valide de `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="783f7-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="783f7-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="783f7-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
