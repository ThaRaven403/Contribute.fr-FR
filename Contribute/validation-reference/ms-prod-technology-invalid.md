---
title: ms-prod-and-technology-invalid
description: Explication et résolution du problème de génération de documents ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a2b6a5bcb63388c119863ea82fb932dda4eec8
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236340"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="88578-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="88578-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="88578-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="88578-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="88578-105">Utilisez `ms.prod` pour spécifier les produits sur site.</span><span class="sxs-lookup"><span data-stu-id="88578-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="88578-106">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="88578-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="88578-107">Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.</span><span class="sxs-lookup"><span data-stu-id="88578-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="88578-108">Soit votre valeur `ms.prod` n’est pas valide, soit votre valeur `ms.technology` ne forme pas une paire valide avec votre `ms.prod`.</span><span class="sxs-lookup"><span data-stu-id="88578-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="88578-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="88578-109">Resolution</span></span>

<span data-ttu-id="88578-110">Confirmez que votre valeur `ms.prod` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="88578-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="88578-111">Puis, choisissez une valeur `ms.technology` valide.</span><span class="sxs-lookup"><span data-stu-id="88578-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="88578-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="88578-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span> <span data-ttu-id="88578-113">Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span><span class="sxs-lookup"><span data-stu-id="88578-113">To request new values, follow [this process](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
