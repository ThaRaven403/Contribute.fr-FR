---
title: ms-service-missing
description: Explication et résolution du problème de génération de documents ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236495"
---
# <a name="ms-service-missing"></a><span data-ttu-id="8b12e-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="8b12e-103">ms-service-missing</span></span>

## <a name="warning"></a><span data-ttu-id="8b12e-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="8b12e-104">Warning</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="8b12e-105">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="8b12e-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="8b12e-106">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`, mais si vous spécifiez `ms.subservice`, vous devez aussi spécifier `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="8b12e-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="8b12e-107">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="8b12e-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="8b12e-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="8b12e-108">Resolution</span></span>

<span data-ttu-id="8b12e-109">Confirmez que la valeur `ms.subservice` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="8b12e-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="8b12e-110">Puis, ajoutez la valeur `ms.service` appropriée qui est un parent valide de `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8b12e-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="8b12e-111">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8b12e-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="8b12e-112">Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="8b12e-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
