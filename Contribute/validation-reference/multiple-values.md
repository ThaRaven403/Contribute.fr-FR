---
title: multiple-values
description: Explication et résolution du problème de génération de documents multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465113"
---
# <a name="multiple-values"></a>multiple-values

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

Vous avez spécifié plusieurs valeurs pour un attribut qui ne peut avoir qu’une seule valeur.

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

Les attributs qui ne peuvent avoir qu’une seule valeur doivent être spécifiés au format YML à valeur unique (scalaire).

## <a name="resolution"></a>Résolution

Vous obtenez cette Suggestion à chaque fois qu’un tableau à plusieurs valeurs est utilisé pour un attribut à valeur unique, avec plusieurs valeurs ou une valeur unique dans le tableau.

YML prend en charge les formats de tableaux suivants pour les attributs à plusieurs valeurs, comme `ms.custom` :

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

Ces formats ne sont pas valides pour les attributs à une seule valeur, comme `author`.

Si vous avez spécifié plusieurs valeurs, passez en revue les valeurs spécifiées et déterminez la valeur correcte. Supprimez les autres valeurs et spécifiez la valeur unique sur la même ligne que l’attribut sans crochets, comme suit :

```yml
---
author: meganbradley
---
```

Si vous avez un tableau à valeur unique, attribuez-lui le format scalaire ci-dessus.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
