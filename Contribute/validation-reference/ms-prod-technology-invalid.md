---
title: ms-prod-and-technology-invalid
description: Explication et résolution du problème de génération de documents ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 20706a44da0320c1a3fc85592a4636efba364dc7
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987580"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="f3be4-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="f3be4-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="f3be4-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="f3be4-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="f3be4-105">Avertissement</span><span class="sxs-lookup"><span data-stu-id="f3be4-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="f3be4-106">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="f3be4-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="f3be4-107">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="f3be4-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="f3be4-108">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="f3be4-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="f3be4-109">Soit votre valeur `ms.prod` n’est pas valide, soit votre valeur `ms.technology` ne forme pas une paire valide avec votre `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="f3be4-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="f3be4-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="f3be4-110">Resolution</span></span>

<span data-ttu-id="f3be4-111">Confirmez que votre valeur `ms.prod` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="f3be4-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="f3be4-112">Puis, choisissez une valeur `ms.technology` valide.</span><span class="sxs-lookup"><span data-stu-id="f3be4-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="f3be4-113">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="f3be4-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
