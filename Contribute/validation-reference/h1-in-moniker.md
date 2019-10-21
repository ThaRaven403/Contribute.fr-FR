---
title: h1-in-moniker
description: Explication et résolution du problème de génération Docs h1-in-moniker.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/09/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3730385cfaf86c3a2a6165f1958d644e71ad7b56
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246357"
---
# <a name="h1-in-moniker"></a>h1-in-moniker

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre. Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier. Les titres H1 ne sont pas autorisés dans les sections de moniker, car ils peuvent facilement provoquer des titres H1 en doublon ou manquants, selon la configuration de la gestion de versions.

Vous pouvez également obtenir ce message si une section de moniker contient une ligne de signe « égal » constituant un double soulignement, comme ceci : `=======`. Il s’agit d’une syntaxe Markdown alternative pour un titre H1. Il apparaît aussi souvent dans les conflits de fusion :

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a>Résolution

Pour résoudre ce problème, supprimez les titres H1 de toutes les sections de moniker et vérifiez que le titre H1 en haut de l’article est approprié pour toutes les sections de moniker. Notez que passer des niveaux de titre, comme faire suivre H1 de H3, n’est pas autorisé.

Si un titre H1 dans une section de moniker est en fait un double soulignement (`=======`), supprimez-le ou remplacez-le par un titre de mot-dièse, comme `##`, selon le cas. Si le double soulignement est impliqué dans un conflit de fusion, veillez également à supprimer les marqueurs de début et de fin du conflit de fusion, et le texte obsolète.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
