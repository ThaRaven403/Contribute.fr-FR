---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c10bf7936968f876d983c77e64c2a8cb809baae2
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236320"
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
