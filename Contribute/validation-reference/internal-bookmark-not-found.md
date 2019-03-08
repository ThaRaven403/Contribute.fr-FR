---
title: internal-bookmark-not-found
description: Explication et résolution du problème de génération Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427495"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Current file doesn't contain a bookmark named '{bookmark}'.`

Vous tentez d’établir un lien vers un titre du fichier actuel qui n’existe pas.

## <a name="resolution"></a>Résolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Vérifiez le titre vers lequel vous voulez établir un lien et mettez à jour le lien.

Pour établir un lien vers une section de l’article actuel, utilisez un symbole dièse, suivi des mots du titre. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets. Voici un exemple :

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
