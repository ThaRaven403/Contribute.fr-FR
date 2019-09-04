---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25428f93eaa7d36a5bbe35d77434ef33972e8944
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236538"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="d8fda-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="d8fda-103">ms-author-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="d8fda-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="d8fda-104">Warning</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="d8fda-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="d8fda-105">Resolution</span></span>

<span data-ttu-id="d8fda-106">Vérifiez que la valeur `ms.author` est l’alias Microsoft valide de l’auteur actuel.</span><span class="sxs-lookup"><span data-stu-id="d8fda-106">Verify that the `ms.author` value is the current author's valid Microsoft alias.</span></span> <span data-ttu-id="d8fda-107">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte.</span><span class="sxs-lookup"><span data-stu-id="d8fda-107">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="d8fda-108">Vous trouverez les valeurs valides des listes de distribution sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="d8fda-108">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
