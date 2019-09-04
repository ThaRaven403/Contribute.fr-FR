---
title: ms-prod-missing
description: Explication et résolution du problème de génération de documents ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5f0b5964dd66946f87d4535e134905db731743f2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236325"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

## <a name="warning"></a>Avertissement

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Utilisez `ms.prod` pour spécifier les produits sur site. Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`, mais si vous spécifiez `ms.technology`, vous devez aussi spécifier `ms.prod`. Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.

## <a name="resolution"></a>Résolution

Confirmez que la valeur `ms.technology` spécifiée est correcte pour votre article. Puis, ajoutez la valeur `ms.prod` appropriée qui est un parent valide de `ms.technology`.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists). Pour demander de nouvelles valeurs, suivez cette [procédure](https://review.docs.microsoft.com/help/contribute/metadata-changes?branch=master).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
