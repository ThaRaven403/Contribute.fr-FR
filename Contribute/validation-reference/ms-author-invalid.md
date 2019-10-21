---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: 615d9f5978893196a24e3a043f3b71a22e1eb353
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246309"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="a2098-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="a2098-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="a2098-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a2098-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="a2098-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="a2098-105">Resolution</span></span>

<span data-ttu-id="a2098-106">Mettez à jour la valeur de `ms.author` avec l’alias Microsoft valide de l’auteur actuel.</span><span class="sxs-lookup"><span data-stu-id="a2098-106">Update the `ms.author` value with the current author's valid Microsoft alias.</span></span> <span data-ttu-id="a2098-107">Nous recommandons que l’auteur désigné soit un employé à plein temps ou une liste de distribution d’équipe, plutôt qu’un fournisseur à court terme.</span><span class="sxs-lookup"><span data-stu-id="a2098-107">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> <span data-ttu-id="a2098-108">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="a2098-108">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="a2098-109">Vous trouverez les valeurs valides des listes de distribution `ms.author` sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="a2098-109">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
