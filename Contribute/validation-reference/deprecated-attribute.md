---
title: deprecated-attribute
description: Explication et résolution du problème de génération de documents deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636882"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="9ea63-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="9ea63-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9ea63-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="9ea63-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="9ea63-105">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="9ea63-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="9ea63-106">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="9ea63-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="9ea63-107">N’utilisez pas `ms.component` ; cela est déconseillé pour ce contenu.</span><span class="sxs-lookup"><span data-stu-id="9ea63-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="9ea63-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="9ea63-108">Resolution</span></span>

<span data-ttu-id="9ea63-109">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="9ea63-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="9ea63-110">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="9ea63-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="9ea63-111">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="9ea63-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
