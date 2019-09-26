---
title: h1-missing
description: Explication et résolution du problème de génération Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 2d0b766bba5b5ba32bff68f7ac185ab639fc7557
ms.sourcegitcommit: 7e73bef8bcdca39fd54cd79fbe8cb22da5566411
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71247413"
---
# <a name="h1-missing"></a>h1-missing

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.

## <a name="resolution"></a>Résolution

Pour résoudre ce problème, ajoutez un titre H1 comme premier contenu après le bloc de métadonnées YML dans votre fichier :

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Cette règle ne s’applique pas aux fichiers inclus. Si vous recevez des résultats H1 sur des fichiers inclus, vous devez plus probablement déplacer vos fichiers inclus dans un dossier `includes`. Le dossier `includes` peut être à n’importe quel niveau dans le chemin du fichier. En fonction du chemin, la génération Docs reconnaît le fichier comme fichier inclus et les validations H1 ne sont pas exécutées.
>
> Une cause courante de l’absence de validations H1 dans les fichiers parents est l’utilisation incorrecte des fichiers inclus : H1 se trouve dans le fichier inclus et non dans le fichier parent. Cela n’est pas autorisé, car l’utilisation de H1 dans un fichier inclus signifie qu’il existe des doublons de H1 dans des fichiers parents ou que le fichier inclus n’est utilisé qu’une seule fois. Les validations H1 doivent être uniques au sein d’un jeu de contenu et les fichiers inclus ne doivent être utilisés que pour partager du contenu entre plusieurs fichiers. Si vous recevez des résultats `h1-missing` parce que H1 se trouve dans un fichier inclus, la solution consiste à déplacer H1 – et tout le contenu inclus si le fichier inclus est utilisé une seule fois – dans le fichier parent. Pour plus d’informations sur les fichiers inclus dans docs, consultez l’article interne de Microsoft [Inclure du contenu réutilisable dans des articles.](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
