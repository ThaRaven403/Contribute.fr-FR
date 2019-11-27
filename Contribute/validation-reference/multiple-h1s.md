---
title: multiple-h1s
description: Explication et résolution du problème de génération de la documentation multiple-h1s.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: e2912066895494e221181f2de2bb117ff9ed1636
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528938"
---
# <a name="multiple-h1s"></a>multiple-h1s

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Multiple H1s are not allowed. You can only have one top-level heading.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre. Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier.

Vous pouvez également recevoir ce message si votre article contient une ligne de signe « égal » constituant un double soulignement, comme ceci : `=======`. Il s’agit d’une syntaxe Markdown alternative pour un titre H1. Il apparaît aussi souvent dans les conflits de fusion :

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

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

Si un titre H1 supplémentaire est en fait un double soulignement (`=======`), supprimez-le ou remplacez-le par un titre de mot-dièse, comme `##`, selon le cas. Si le double soulignement est impliqué dans un conflit de fusion, veillez également à supprimer les marqueurs de début et de fin du conflit de fusion, et le texte obsolète.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
