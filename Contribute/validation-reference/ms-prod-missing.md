---
title: ms-prod-missing
description: Explication et résolution du problème de génération de documents ms-prod-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: ee29396a20345f6884a5bbc94aa25f48dafaff52
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713220"
---
# <a name="ms-prod-missing"></a>ms-prod-missing

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

Utilisez `ms.prod` pour spécifier les produits sur site. Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`, mais si vous spécifiez `ms.technology`, vous devez aussi spécifier `ms.prod`. Les valeurs pour `ms.prod` et `ms.technology` doivent être une paire valide.

## <a name="resolution"></a>Résolution

Confirmez que la valeur `ms.technology` spécifiée est correcte pour votre article. Puis, ajoutez la valeur `ms.prod` appropriée qui est un parent valide de `ms.technology`.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/whitelists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
