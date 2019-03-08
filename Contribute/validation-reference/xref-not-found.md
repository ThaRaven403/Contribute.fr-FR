---
title: xref-not-found
description: Explication et résolution du problème de génération Docs issue xref-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427517"
---
# <a name="xref-not-found"></a><span data-ttu-id="3dd78-103">xref-not-found</span><span class="sxs-lookup"><span data-stu-id="3dd78-103">xref-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="3dd78-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="3dd78-104">Warning</span></span>

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

<span data-ttu-id="3dd78-105">L’UID vers lequel vous avez établi un lien n’existe pas ou n’est pas disponible dans votre dépôt.</span><span class="sxs-lookup"><span data-stu-id="3dd78-105">The UID you linked to doesn't exist, or isn't available to your repo.</span></span>

## <a name="resolution"></a><span data-ttu-id="3dd78-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="3dd78-106">Resolution</span></span>

<span data-ttu-id="3dd78-107">Vérifiez que l’UID est correct et que le service Xref est correctement configuré sur votre dépôt, comme décrit dans la documentation [Service Xref](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) interne à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3dd78-107">Confirm that the UID is correct and that the Xref Service is properly configured on your repo, as described in the Microsoft-internal [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) documentation.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
