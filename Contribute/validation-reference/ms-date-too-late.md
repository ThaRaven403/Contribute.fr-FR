---
title: ms-date-too-late
description: Explication et résolution du problème de génération de documents ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637388"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>Avertissement

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

L’attribut `ms.date` est utilisé pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article. La date ne peut donc pas être postérieure à la date du jour. Cinq jours sont autorisés pour prendre en compte le délai de publication, comme quand le contenu est figé pour le QA en préparation d’un événement majeur.

## <a name="resolution"></a>Résolution

Spécifiez `ms.date` qui ne se situe pas dans plus de cinq jour par rapport à aujourd’hui, au format MM/JJ/AAAA :

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
