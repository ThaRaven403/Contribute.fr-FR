---
title: internal-bookmark-not-found
description: Explication et résolution du problème de génération Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856217"
---
# <a name="bookmark-not-found"></a>bookmark-not-found

## <a name="warning"></a>Avertissement

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

Vous tentez d’établir un lien vers un titre du fichier actuel ou un autre fichier qui n’existe pas.

## <a name="resolution"></a>Résolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Vérifiez le titre vers lequel vous voulez établir un lien et mettez à jour le lien.

Pour établir un lien vers une section de l’article actuel, utilisez un symbole dièse, suivi des mots du titre. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets. Voici un exemple :

```markdown
[Managed Disks](#managed-disks)
```

Pour établir un lien vers un titre dans un autre fichier, utilisez un lien relatif vers ce fichier, suivi du symbole dièse et des mots du titre. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets. Voici un exemple :

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
