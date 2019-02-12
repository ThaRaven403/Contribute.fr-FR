---
title: ms-service-missing
description: Explication et résolution du problème de génération de documents ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713082"
---
# <a name="ms-service-missing"></a>ms-service-missing

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`, mais si vous spécifiez `ms.subservice`, vous devez aussi spécifier `ms.service`. Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.

## <a name="resolution"></a>Résolution

Confirmez que la valeur `ms.subservice` spécifiée est correcte pour votre article. Puis, ajoutez la valeur `ms.service` appropriée qui est un parent valide de `ms.subservice`.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
