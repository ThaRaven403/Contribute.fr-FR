---
title: ms-prod-service-mismatch
description: Explication et résolution du problème de génération de documents ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987612"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="82cba-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="82cba-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="82cba-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="82cba-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="82cba-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="82cba-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="82cba-106">Utilisez `ms.prod` pour spécifier les produits sur site ; `ms.service` pour les services cloud.</span><span class="sxs-lookup"><span data-stu-id="82cba-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="82cba-107">Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="82cba-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="82cba-108">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="82cba-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="82cba-109">Vous ne pouvez pas utiliser `ms.prod` avec `ms.subservice` ou `ms.service` avec `ms.technology`.</span><span class="sxs-lookup"><span data-stu-id="82cba-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="82cba-110">Résolution</span><span class="sxs-lookup"><span data-stu-id="82cba-110">Resolution</span></span>

<span data-ttu-id="82cba-111">Pour commencer, vérifiez que vous avez sélectionné l’attribut parent correct (`ms.prod` ou `ms.service`) pour votre article.</span><span class="sxs-lookup"><span data-stu-id="82cba-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="82cba-112">Puis, ajoutez le champ enfant approprié avec une valeur associée valide.</span><span class="sxs-lookup"><span data-stu-id="82cba-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="82cba-113">Supprimez les champs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="82cba-113">Remove any extra fields.</span></span>

<span data-ttu-id="82cba-114">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="82cba-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
