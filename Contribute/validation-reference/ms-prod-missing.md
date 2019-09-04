---
title: ms-prod-missing
description: Explication et résolution du problème de génération de documents ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236325"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="8ce3c-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="8ce3c-103">ms-prod-missing</span></span>

## <a name="warning"></a><span data-ttu-id="8ce3c-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="8ce3c-104">Warning</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="8ce3c-105">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="8ce3c-106">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`, mais si vous spécifiez `ms.technology`, vous devez aussi spécifier `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="8ce3c-107">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="8ce3c-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="8ce3c-108">Resolution</span></span>

<span data-ttu-id="8ce3c-109">Confirmez que la valeur `ms.technology` spécifiée est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="8ce3c-110">Puis, ajoutez la valeur `ms.prod` appropriée qui est un parent valide de `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="8ce3c-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="8ce3c-111">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="8ce3c-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="8ce3c-112">Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="8ce3c-112">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
