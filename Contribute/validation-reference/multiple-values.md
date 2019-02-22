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
# <a name="multiple-values"></a><span data-ttu-id="36719-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="36719-103">multiple-values</span></span>

<span data-ttu-id="36719-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="36719-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="36719-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="36719-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="36719-106">Vous avez spécifié plusieurs valeurs pour un attribut qui ne peut avoir qu’une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="36719-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="36719-107">Les attributs qui ne peuvent avoir qu’une seule valeur doivent être spécifiés au format YML à valeur unique (scalaire).</span><span class="sxs-lookup"><span data-stu-id="36719-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="36719-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="36719-108">Resolution</span></span>

<span data-ttu-id="36719-109">Vous obtenez cette Suggestion à chaque fois qu’un tableau à plusieurs valeurs est utilisé pour un attribut à valeur unique, avec plusieurs valeurs ou une valeur unique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="36719-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="36719-110">YML prend en charge les formats de tableaux suivants pour les attributs à plusieurs valeurs, comme `ms.custom` :</span><span class="sxs-lookup"><span data-stu-id="36719-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="36719-111">Ces formats ne sont pas valides pour les attributs à une seule valeur, comme `author`.</span><span class="sxs-lookup"><span data-stu-id="36719-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="36719-112">Si vous avez spécifié plusieurs valeurs, passez en revue les valeurs spécifiées et déterminez la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="36719-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="36719-113">Supprimez les autres valeurs et spécifiez la valeur unique sur la même ligne que l’attribut sans crochets, comme suit :</span><span class="sxs-lookup"><span data-stu-id="36719-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="36719-114">Si vous avez un tableau à valeur unique, attribuez-lui le format scalaire ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="36719-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
