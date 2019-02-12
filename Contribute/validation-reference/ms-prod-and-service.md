---
title: ms-prod-and-service
description: Explication et résolution du problème de génération de documents ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 42e6f063c8b3d97386b2655b49a19a3e103d6b3b
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713197"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Résolution

`ms.prod` ou `ms.service` est requis, et les deux valeurs ne peuvent pas être présentes : `ms.prod` est utilisé pour les produits sur site ; `ms.service` est utilisé pour les services cloud. Déterminez la valeur appropriée pour votre article, vérifiez que la valeur est correcte et supprimez l’autre champ.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
