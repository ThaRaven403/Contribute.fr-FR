---
title: ms-prod-missing
description: Explication et résolution du problème de génération de documents ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636767"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="cca92-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="cca92-103">ms-prod-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="cca92-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="cca92-104">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="cca92-105">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="cca92-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="cca92-106">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`, mais si vous spécifiez `ms.technology`, vous devez aussi spécifier `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="cca92-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="cca92-107">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="cca92-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="cca92-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="cca92-108">Resolution</span></span>

<span data-ttu-id="cca92-109">Confirmez que la valeur `ms.technology` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="cca92-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="cca92-110">Puis, ajoutez la valeur `ms.prod` appropriée qui est un parent valide de `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="cca92-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="cca92-111">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="cca92-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
