---
title: ms-service-missing
description: Explication et résolution du problème de génération de documents ms-service-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: b50d9d6f57c953569a4e5dd873961b8c511a8bb1
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236495"
---
# <a name="ms-service-missing"></a>ms-service-missing

## <a name="warning"></a>Avertissement

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`, mais si vous spécifiez `ms.subservice`, vous devez aussi spécifier `ms.service`. Les valeurs pour `ms.service` et `ms.subservice` doivent être une paire valide.

## <a name="resolution"></a>Résolution

Confirmez que la valeur `ms.subservice` spécifiée est correcte pour votre article. Puis, ajoutez la valeur `ms.service` appropriée qui est un parent valide de `ms.subservice`.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists). Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
