---
title: ms-date-too-late
description: Explication et résolution du problème de génération de documents ms-date-too-late
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: b38392e9f297e4ee4147ca7fc65f938b5cd53403
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431481"
---
# <a name="ms-date-too-late"></a>ms-date-too-late

**Bientôt disponible !**

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
