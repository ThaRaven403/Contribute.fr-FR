---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481698"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="75ab6-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="75ab6-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="75ab6-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="75ab6-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="75ab6-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="75ab6-105">Resolution</span></span>

<span data-ttu-id="75ab6-106">Vérifiez que la valeur `ms.author` est l’alias Microsoft valide de l’auteur actuel.</span><span class="sxs-lookup"><span data-stu-id="75ab6-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="75ab6-107">Nous recommandons que l’auteur désigné soit un employé à plein temps ou une liste de distribution d’équipe, plutôt qu’un fournisseur à court terme.</span><span class="sxs-lookup"><span data-stu-id="75ab6-107">We recommend that the designated author be a full-time employee or team distrubution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="75ab6-108">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="75ab6-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="75ab6-109">Vous trouverez les valeurs valides des listes de distribution `ms.author` sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="75ab6-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
