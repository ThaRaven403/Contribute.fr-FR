---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 904ec2ad495945d882e581a240f6a72ca650c37e
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70848588"
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
