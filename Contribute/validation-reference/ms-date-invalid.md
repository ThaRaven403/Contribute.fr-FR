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
# <a name="ms-date-invalid"></a>ms-date-invalid

## <a name="warning"></a>Avertissement

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a>Résolution

Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA :

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
