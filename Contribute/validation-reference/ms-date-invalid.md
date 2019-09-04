---
title: ms-date-invalid
description: Explication et résolution du problème de génération de documents ms-date-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2f34a0e510d7d006c598ae163217a117a72f1de2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236153"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="7015e-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="7015e-103">ms-date-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="7015e-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="7015e-104">Warning</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="7015e-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="7015e-105">Resolution</span></span>

<span data-ttu-id="7015e-106">Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA :</span><span class="sxs-lookup"><span data-stu-id="7015e-106">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
