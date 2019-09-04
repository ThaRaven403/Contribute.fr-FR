---
title: ms-service-and-subservice-invalid
description: Explication et résolution du problème de génération de documents ms-service-and-subservice-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a6059d592212b271780344a086ee68c7133e15cd
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236512"
---
# <a name="ms-service-and-subservice-invalid"></a>ms-service-and-subservice-invalid

## <a name="warning"></a>Avertissement

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`. Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide. Soit votre valeur `ms.service` n’est pas valide, soit votre valeur `ms.subservice` ne forme pas une paire valide avec votre `ms.service`.

## <a name="resolution"></a>Résolution

Confirmez que votre valeur `ms.service` est correcte pour votre article. Puis, choisissez une valeur `ms.subservice` valide.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists). Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
