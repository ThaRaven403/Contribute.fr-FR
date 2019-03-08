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
# <a name="yaml-header-invalid"></a><span data-ttu-id="f4250-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="f4250-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="f4250-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="f4250-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="f4250-105">Ceci signifie généralement qu’une valeur de métadonnées sans guillemets dans un en-tête YAML inclut un signe deux-points ou un autre caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="f4250-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="f4250-106">Cela peut également signifier qu’un espace est manquant après le signe deux-points dans une paire clé/valeur.</span><span class="sxs-lookup"><span data-stu-id="f4250-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="f4250-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="f4250-107">Resolution</span></span>

<span data-ttu-id="f4250-108">Examinez votre en-tête YAML.</span><span class="sxs-lookup"><span data-stu-id="f4250-108">Review your YAML header.</span></span> <span data-ttu-id="f4250-109">Recherchez les fautes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4250-109">Look for the following mistakes.</span></span>

<span data-ttu-id="f4250-110">Signe deux-points dans une valeur sans guillemets :</span><span class="sxs-lookup"><span data-stu-id="f4250-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="f4250-111">Remplacez par :</span><span class="sxs-lookup"><span data-stu-id="f4250-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="f4250-112">Pas d’espace après le signe deux-points dans une paire clé/valeur :</span><span class="sxs-lookup"><span data-stu-id="f4250-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="f4250-113">Remplacez par :</span><span class="sxs-lookup"><span data-stu-id="f4250-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
