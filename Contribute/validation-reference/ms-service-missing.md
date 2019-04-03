---
title: ms-service-missing
description: Explication et résolution du problème de génération de documents ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636698"
---
# <a name="ms-service-missing"></a><span data-ttu-id="f7269-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="f7269-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f7269-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="f7269-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="f7269-105">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="f7269-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="f7269-106">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`, mais si vous spécifiez `ms.subservice`, vous devez aussi spécifier `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="f7269-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="f7269-107">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="f7269-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7269-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="f7269-108">Resolution</span></span>

<span data-ttu-id="f7269-109">Confirmez que la valeur `ms.subservice` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="f7269-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="f7269-110">Puis, ajoutez la valeur `ms.service` appropriée qui est un parent valide de `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="f7269-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="f7269-111">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="f7269-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
