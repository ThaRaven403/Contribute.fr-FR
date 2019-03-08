---
title: external-bookmark-not-found
description: Explication et résolution du problème de génération Docs external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427459"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>Avertissement

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

Vous tentez d’établir un lien vers un titre d’un autre fichier qui n’existe pas.

## <a name="resolution"></a>Résolution

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

Examinez le fichier vers lequel vous établissez un lien et mettez à jour le lien de votre signet pour le faire pointer vers une section valide du fichier.

Pour établir un lien vers un titre dans un autre article, utilisez le lien relatif à un fichier ou relatif à un site plus un symbole dièse, suivi des mots du titre. Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets. Voici un exemple :

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
