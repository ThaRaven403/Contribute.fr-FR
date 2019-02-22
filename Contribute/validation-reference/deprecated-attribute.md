---
title: deprecated-attribute
description: Explication et résolution du problème de génération de documents deprecated-attribute
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322680"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Deprecated attribute: ms.component. Use ms.subservice instead.`

Utilisez `ms.service` pour spécifier les services cloud. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez éventuellement spécifier `ms.subservice`. N’utilisez pas `ms.component` ; cela est déconseillé pour ce contenu.

## <a name="resolution"></a>Résolution

Confirmez que votre valeur `ms.service` est correcte pour votre article. Puis, choisissez une valeur `ms.subservice` valide.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
