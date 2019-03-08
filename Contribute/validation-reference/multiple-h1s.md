---
title: multiple-h1
description: Explication et résolution du problème de génération Docs multiple-h1.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 55ce6260cb4d1e09f63e0540528576ed3fa165f8
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427527"
---
# <a name="multiple-h1"></a>multiple-h1

## <a name="warning"></a>Avertissement

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre. Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier.

## <a name="resolution"></a>Résolution

Pour résoudre ce problème, changez le niveau des titres H1 suivants en H2 (`##`), ou bien réorganisez votre fichier. Notez que passer des niveaux de titre, comme faire suivre H1 de H3, n’est pas autorisé.

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1

Some content...

## This is an H2
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]