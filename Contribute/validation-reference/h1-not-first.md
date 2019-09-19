---
title: h1-not-first
description: Explication et résolution du problème de génération de la documentation h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895459"
---
# <a name="h1-not-first"></a>h1-not-first

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Markdown content is not allowed before H1.`

Seul le titre des métadonnées YAML peut se trouver avant le titre H1 dans un fichier Markdown. Par exemple, si vous voulez ajouter une note ou une image en haut de l’article, celle-ci doit venir après le titre H1. Ce qui suit n’est pas autorisé :

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

Procédez plutôt comme suit :

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

Une autre cause courante de ce problème est les [marques d’ordre d’octet](http://www.websina.com/bugzero/kb/unicode-bom.html) avant l’en-tête YAML. Ceux-ci viennent parfois avec des problèmes d’encodage lors de la validation du contenu dans les dépôts. Ils entraînent un rendu incorrect dans GitHub et doivent être supprimés.

## <a name="resolution"></a>Résolution

Supprimez tout contenu autre que le titre des métadonnées YAML avant le titre H1.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
