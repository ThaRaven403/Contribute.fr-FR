---
title: xref-not-found
description: Explication et résolution du problème de génération Docs issue xref-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427517"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>Avertissement

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

L’UID vers lequel vous avez établi un lien n’existe pas ou n’est pas disponible dans votre dépôt.

## <a name="resolution"></a>Résolution

Vérifiez que l’UID est correct et que le service Xref est correctement configuré sur votre dépôt, comme décrit dans la documentation [Service Xref](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) interne à Microsoft.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
