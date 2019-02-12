---
title: ms-service-and-subservice-invalid
description: Explication et résolution du problème de génération de documents ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713128"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="ef5ef-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="ef5ef-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="ef5ef-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="ef5ef-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="ef5ef-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="ef5ef-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="ef5ef-106">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="ef5ef-107">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="ef5ef-108">Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="ef5ef-109">Soit votre valeur `ms.service` n’est pas valide, soit votre valeur `ms.subservice` ne forme pas une paire valide avec votre `ms.service`.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="ef5ef-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="ef5ef-110">Resolution</span></span>

<span data-ttu-id="ef5ef-111">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="ef5ef-112">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="ef5ef-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="ef5ef-113">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="ef5ef-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
