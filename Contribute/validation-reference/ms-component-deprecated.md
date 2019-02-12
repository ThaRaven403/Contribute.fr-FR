---
title: ms-component-deprecated
description: Explication et résolution du problème de génération de documents ms-component-deprecated
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713151"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="f947f-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="f947f-103">ms-component-deprecated</span></span>

<span data-ttu-id="f947f-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="f947f-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="f947f-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="f947f-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="f947f-106">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="f947f-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="f947f-107">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="f947f-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="f947f-108">N’utilisez pas `ms.component` ; cela est déconseillé pour ce contenu.</span><span class="sxs-lookup"><span data-stu-id="f947f-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="f947f-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="f947f-109">Resolution</span></span>

<span data-ttu-id="f947f-110">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="f947f-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="f947f-111">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="f947f-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="f947f-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="f947f-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
