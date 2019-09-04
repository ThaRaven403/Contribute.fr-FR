---
title: deprecated-attribute
description: Explication et résolution du problème de génération de documents deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 15d285159b361b7fb9dbc1774e6c4b2f5f5758ed
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236210"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

## <a name="warning"></a>Avertissement

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`. N’utilisez pas `ms.component` ; cela est déconseillé pour ce contenu.

## <a name="resolution"></a>Résolution

Confirmez que votre valeur `ms.service` est correcte pour votre article. Puis, choisissez une valeur `ms.subservice` valide.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
