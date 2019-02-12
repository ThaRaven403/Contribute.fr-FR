---
title: ms-prod-and-technology-invalid
description: Explication et résolution du problème de génération de documents ms-prod-and-technology-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713266"
---
# <a name="ms-prod-and-technology-invalid"></a>ms-prod-and-technology-invalid

**Bientôt disponible !**

## <a name="warning"></a>Avertissement

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

Utilisez `ms.prod` pour spécifier les produits sur site. Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`. Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide. Soit votre valeur `ms.prod` n’est pas valide, soit votre valeur `ms.technology` ne forme pas une paire valide avec votre `ms.prod`.

## <a name="resolution"></a>Résolution

Confirmez que votre valeur `ms.prod` est correcte pour votre article. Puis, choisissez une valeur `ms.technology` valide.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
