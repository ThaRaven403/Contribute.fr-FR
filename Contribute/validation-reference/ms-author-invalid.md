---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987764"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="0d35e-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="0d35e-103">ms-author-invalid</span></span>

<span data-ttu-id="0d35e-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="0d35e-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0d35e-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="0d35e-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="0d35e-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="0d35e-106">Resolution</span></span>

<span data-ttu-id="0d35e-107">Vérifiez que la valeur de `ms.author` est un alias Microsoft valide.</span><span class="sxs-lookup"><span data-stu-id="0d35e-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="0d35e-108">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte.</span><span class="sxs-lookup"><span data-stu-id="0d35e-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="0d35e-109">Vous trouverez les valeurs valides des listes de distribution sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="0d35e-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
