---
title: yaml-header-invalid
description: Explication et résolution du problème de génération Docs yaml-header-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459024"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>Avertissement

`Invalid YAML header: Improper use of a colon in a metadata entry.`

Ceci signifie généralement qu’une valeur de métadonnées sans guillemets dans un en-tête YAML inclut un signe deux-points ou un autre caractère spécial. Cela peut également signifier qu’un espace est manquant après le signe deux-points dans une paire clé/valeur.

## <a name="resolution"></a>Résolution

Examinez votre en-tête YAML. Recherchez les fautes suivantes.

Signe deux-points dans une valeur sans guillemets :

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

Remplacez par :

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

Pas d’espace après le signe deux-points dans une paire clé/valeur :

```yml
---
title:I omitted a space.
---
```

Remplacez par :

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
