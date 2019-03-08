---
title: manager-missing
description: Explication et résolution du problème de génération Docs manager-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427490"
---
# <a name="manager-missing"></a>manager-missing

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

Certains groupes de contenus nécessitent l’attribut `manager` pour identifier le responsable de l’auteur.

## <a name="resolution"></a>Résolution

Ajoutez un alias Microsoft valide pour `manager` :

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
