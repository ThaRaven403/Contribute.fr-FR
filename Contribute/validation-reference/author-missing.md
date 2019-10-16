---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288502"
---
# <a name="author-missing"></a><span data-ttu-id="1f53e-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="1f53e-103">author-missing</span></span>

## <a name="warning"></a><span data-ttu-id="1f53e-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="1f53e-104">Warning</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="1f53e-105">L’attribut `author` identifie l’auteur de l’article par ID GitHub.</span><span class="sxs-lookup"><span data-stu-id="1f53e-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="1f53e-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="1f53e-106">Resolution</span></span>

<span data-ttu-id="1f53e-107">Ajoutez l’ID GitHub de l’auteur actuel à l’en-tête YML :</span><span class="sxs-lookup"><span data-stu-id="1f53e-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="1f53e-108">Notez que ce doit être le propriétaire *actuel* de l’article, pas l’auteur d’origine si l’appartenance a changé.</span><span class="sxs-lookup"><span data-stu-id="1f53e-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
