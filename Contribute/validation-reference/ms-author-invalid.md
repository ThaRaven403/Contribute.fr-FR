---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/27/2019
ms.prod: non-product-specific
ms.openlocfilehash: b3100b4a304356aee3c50f805628890b8c738fe1
ms.sourcegitcommit: d2f5b68b6a6d1ac902dba5063482ff5955a5b1f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2019
ms.locfileid: "71481698"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

## <a name="warning"></a>Avertissement

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Résolution

Vérifiez que la valeur `ms.author` est l’alias Microsoft valide de l’auteur actuel. Nous recommandons que l’auteur désigné soit un employé à plein temps ou une liste de distribution d’équipe, plutôt qu’un fournisseur à court terme. Si l’alias est une liste de distribution, il doit également figurer dans la liste verte `ms.author`.

Vous trouverez les valeurs valides des listes de distribution `ms.author` sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
