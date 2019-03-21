---
title: ms-service-and-subservice-invalid
description: Explication et résolution du problème de génération de documents ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7dee18e7b902b660a8071bcb4a0dee21c19f4f7f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987635"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="8288d-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="8288d-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="8288d-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="8288d-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="8288d-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="8288d-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="8288d-106">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="8288d-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="8288d-107">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="8288d-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="8288d-108">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="8288d-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="8288d-109">Soit votre valeur `ms.service` n’est pas valide, soit votre valeur `ms.subservice` ne forme pas une paire valide avec votre `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="8288d-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="8288d-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="8288d-110">Resolution</span></span>

<span data-ttu-id="8288d-111">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="8288d-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="8288d-112">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="8288d-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="8288d-113">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8288d-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
