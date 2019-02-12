---
title: ms-prod-and-technology-invalid
description: Explication et résolution du problème de génération de documents ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713266"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="d0120-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="d0120-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="d0120-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="d0120-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="d0120-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="d0120-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="d0120-106">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="d0120-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="d0120-107">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="d0120-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="d0120-108">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="d0120-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="d0120-109">Soit votre valeur `ms.prod` n’est pas valide, soit votre valeur `ms.technology` ne forme pas une paire valide avec votre `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="d0120-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="d0120-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="d0120-110">Resolution</span></span>

<span data-ttu-id="d0120-111">Confirmez que votre valeur `ms.prod` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="d0120-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="d0120-112">Puis, choisissez une valeur `ms.technology` valide.</span><span class="sxs-lookup"><span data-stu-id="d0120-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="d0120-113">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="d0120-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
