---
title: ms-prod-service-mismatch
description: Explication et résolution du problème de génération de documents ms-prod-service-mismatch
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987612"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

Utilisez `ms.prod` pour spécifier les produits sur site ; `ms.service` pour les services cloud. Pour spécifier des informations plus détaillées sur `ms.prod`, vous pouvez éventuellement spécifier `ms.technology`. Pour spécifier des informations plus détaillées sur `ms.service`, vous pouvez spécifier `ms.subservice`. Vous ne pouvez pas utiliser `ms.prod` avec `ms.subservice` ou `ms.service` avec `ms.technology`.

## <a name="resolution"></a>Résolution

Pour commencer, vérifiez que vous avez sélectionné l’attribut parent correct (`ms.prod` ou `ms.service`) pour votre article. Puis, ajoutez le champ enfant approprié avec une valeur associée valide. Supprimez les champs supplémentaires.

Vous trouverez les valeurs valides sur [ce site Microsoft interne](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
