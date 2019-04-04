---
title: ms-date-missing
description: Explication et résolution du problème de génération de documents ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: ae2a28993671255a9ffd4503eebdbee404e52373
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637273"
---
# <a name="ms-date-missing"></a>ms-date-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

Certains groupes de contenus nécessitent une `ms.date` pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article. Cela ne correspond pas à la dernière date à laquelle l’article a été *publié*, qui s’affiche sur la page si `ms.date` n’est pas explicitement spécifié.

## <a name="resolution"></a>Résolution

Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA :

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
