---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.prod: non-product-specific
ms.date: 09/10/2019
ms.openlocfilehash: e31c39ac9915b096e0b0745bf6d9d3ed6efb5412
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288502"
---
# <a name="author-missing"></a>author-missing

## <a name="warning"></a>Avertissement

`Missing attribute: author. Add the current author's GitHub ID.`

L’attribut `author` identifie l’auteur de l’article par ID GitHub. 

## <a name="resolution"></a>Résolution

Ajoutez l’ID GitHub de l’auteur actuel à l’en-tête YML :

```yml
---
author: meganbradley
ms.author: mbradley
---
```

Notez que ce doit être le propriétaire *actuel* de l’article, pas l’auteur d’origine si l’appartenance a changé.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
