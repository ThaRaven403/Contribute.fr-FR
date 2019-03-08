---
title: no-space-in-h1
description: Explication et résolution du problème de génération Docs no-space-in-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427502"
---
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>Avertissement

`A space is required after the hash (#) in H1.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre. Sans l’espace après le dièse, Docs ne reconnaît pas un titre H1.

## <a name="resolution"></a>Résolution

Pour corriger cette erreur, ajoutez un espace après le dièse dans votre titre H1.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]