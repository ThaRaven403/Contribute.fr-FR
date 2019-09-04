---
title: ms-prod-and-service
description: Explication et résolution du problème de génération de documents ms-prod-and-service
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 25a5d2be7d6aad175d746e49e064728020a8ac93
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236356"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

## <a name="warning"></a>Avertissement
https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master `Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>Résolution

`ms.prod` ou `ms.service` est requis, et les deux valeurs ne peuvent pas être présentes : `ms.prod` est utilisé pour les produits sur site ; `ms.service` est utilisé pour les services cloud. Déterminez la valeur appropriée pour votre article, vérifiez que la valeur est correcte et supprimez l’autre champ.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists). Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/en-us/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
