---
title: ms-service-and-subservice-invalid
description: Explication et résolution du problème de génération de documents ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713128"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

**Bientôt disponible !**

## <a name="warning"></a>Avertissement

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`. Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide. Soit votre valeur `ms.service` n’est pas valide, soit votre valeur `ms.subservice` ne forme pas une paire valide avec votre `ms.service`.

## <a name="resolution"></a>Résolution

Confirmez que votre valeur `ms.service` est correcte pour votre article. Puis, choisissez une valeur `ms.subservice` valide.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
