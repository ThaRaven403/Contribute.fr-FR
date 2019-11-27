---
title: h1-not-first
description: Explication et résolution du problème de génération de la documentation h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528910"
---
# <a name="h1-not-first"></a>h1-not-first

## <a name="warning"></a>Avertissement

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
