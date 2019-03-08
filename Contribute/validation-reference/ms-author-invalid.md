---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427507"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="e892e-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="e892e-103">ms-author-invalid</span></span>

<span data-ttu-id="e892e-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="e892e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e892e-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="e892e-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="e892e-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="e892e-106">Resolution</span></span>

<span data-ttu-id="e892e-107">Vérifiez que la valeur de `ms.author` est un alias Microsoft valide.</span><span class="sxs-lookup"><span data-stu-id="e892e-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="e892e-108">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte.</span><span class="sxs-lookup"><span data-stu-id="e892e-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="e892e-109">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="e892e-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
