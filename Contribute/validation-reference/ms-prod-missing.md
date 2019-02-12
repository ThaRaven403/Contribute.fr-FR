---
title: ms-prod-missing
description: Explication et résolution du problème de génération de documents ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713220"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="a68eb-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="a68eb-103">ms-prod-missing</span></span>

<span data-ttu-id="a68eb-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="a68eb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="a68eb-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="a68eb-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="a68eb-106">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="a68eb-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="a68eb-107">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`, mais si vous spécifiez `ms.technology`, vous devez aussi spécifier `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="a68eb-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="a68eb-108">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="a68eb-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="a68eb-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="a68eb-109">Resolution</span></span>

<span data-ttu-id="a68eb-110">Confirmez que la valeur `ms.technology` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="a68eb-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="a68eb-111">Puis, ajoutez la valeur `ms.prod` appropriée qui est un parent valide de `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="a68eb-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="a68eb-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="a68eb-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
