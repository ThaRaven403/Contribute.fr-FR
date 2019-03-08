---
title: h1-empty
description: Explication et résolution du problème de génération Docs h1-empty.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427412"
---
# <a name="h1-empty"></a>h1-empty

## <a name="warning"></a>Avertissement

`H1 is required. Add content to your top-level heading.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.

## <a name="resolution"></a>Résolution

Pour résoudre ce problème, vérifiez que votre titre H1 inclut du contenu, et pas seulement un dièse.

Incorrect :

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

Correct :

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]