---
title: ms-author-missing
description: Explication et résolution du problème de génération de documents ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246253"
---
# <a name="ms-author-missing"></a><span data-ttu-id="150a4-103">ms-author-missing</span><span class="sxs-lookup"><span data-stu-id="150a4-103">ms-author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="150a4-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="150a4-104">Warning</span></span>

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a><span data-ttu-id="150a4-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="150a4-105">Resolution</span></span>

<span data-ttu-id="150a4-106">Ajoutez l’alias Microsoft de l’auteur actuel pour `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="150a4-106">Add the current author's Microsoft alias for `ms.author`.</span></span> <span data-ttu-id="150a4-107">Notez que ce doit être le propriétaire *actuel* de l’article, pas l’auteur d’origine si l’appartenance a changé.</span><span class="sxs-lookup"><span data-stu-id="150a4-107">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span> <span data-ttu-id="150a4-108">Nous recommandons que l’auteur désigné soit un employé à plein temps ou une liste de distribution d’équipe, plutôt qu’un fournisseur à court terme.</span><span class="sxs-lookup"><span data-stu-id="150a4-108">We recommend that the designated author be a full-time employee or team distribution list (DL), rather than a short-term vendor.</span></span> 

<span data-ttu-id="150a4-109">Si l’alias est une liste de distribution, il doit également figurer dans la liste verte `ms.author`.</span><span class="sxs-lookup"><span data-stu-id="150a4-109">If the alias is a DL, it must also be on the `ms.author` allow list.</span></span>

<span data-ttu-id="150a4-110">Vous trouverez les valeurs valides des listes de distribution `ms.author` sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).</span><span class="sxs-lookup"><span data-stu-id="150a4-110">Valid values for `ms.author` DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
