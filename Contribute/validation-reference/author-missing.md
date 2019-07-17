---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791512"
---
# <a name="author-missing"></a>author-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

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
