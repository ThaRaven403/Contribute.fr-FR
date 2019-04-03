---
title: ms-service-and-subservice-invalid
description: Explication et résolution du problème de génération de documents ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637296"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="a5b14-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="a5b14-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a5b14-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="a5b14-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="a5b14-105">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="a5b14-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="a5b14-106">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="a5b14-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="a5b14-107">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="a5b14-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="a5b14-108">Soit votre valeur `ms.service` n’est pas valide, soit votre valeur `ms.subservice` ne forme pas une paire valide avec votre `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="a5b14-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="a5b14-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="a5b14-109">Resolution</span></span>

<span data-ttu-id="a5b14-110">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="a5b14-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="a5b14-111">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="a5b14-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="a5b14-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="a5b14-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
