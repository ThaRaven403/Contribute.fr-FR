---
title: deprecated-attribute
description: Explication et résolution du problème de génération de documents deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322680"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="5b160-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="5b160-103">deprecated-attribute</span></span>

<span data-ttu-id="5b160-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="5b160-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5b160-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5b160-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="5b160-106">Utilisez `ms.service` pour spécifier les services cloud.</span><span class="sxs-lookup"><span data-stu-id="5b160-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="5b160-107">Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`.</span><span class="sxs-lookup"><span data-stu-id="5b160-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="5b160-108">N’utilisez pas `ms.component` ; cela est déconseillé pour ce contenu.</span><span class="sxs-lookup"><span data-stu-id="5b160-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b160-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="5b160-109">Resolution</span></span>

<span data-ttu-id="5b160-110">Confirmez que votre valeur `ms.service` est correcte pour votre article.</span><span class="sxs-lookup"><span data-stu-id="5b160-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="5b160-111">Puis, choisissez une valeur `ms.subservice` valide.</span><span class="sxs-lookup"><span data-stu-id="5b160-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="5b160-112">Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).</span><span class="sxs-lookup"><span data-stu-id="5b160-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
