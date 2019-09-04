---
title: multiple-values
description: Explication et résolution du problème de génération de documents multiple-values
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 515a8cd76cbd3d9bd117b1d0d59492f4a77bea4c
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236474"
---
# <a name="multiple-values"></a><span data-ttu-id="aa2e6-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="aa2e6-103">multiple-values</span></span>

## <a name="warning"></a><span data-ttu-id="aa2e6-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="aa2e6-104">Warning</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="aa2e6-105">Vous avez spécifié plusieurs valeurs pour un attribut qui ne peut avoir qu’une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="aa2e6-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="aa2e6-106">Les attributs qui ne peuvent avoir qu’une seule valeur doivent être spécifiés au format YML à valeur unique (scalaire).</span><span class="sxs-lookup"><span data-stu-id="aa2e6-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="aa2e6-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="aa2e6-107">Resolution</span></span>

<span data-ttu-id="aa2e6-108">Vous obtenez cette Suggestion à chaque fois qu’un tableau à plusieurs valeurs est utilisé pour un attribut à valeur unique, avec plusieurs valeurs ou une valeur unique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="aa2e6-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="aa2e6-109">YML prend en charge les formats de tableaux suivants pour les attributs à plusieurs valeurs, comme `ms.custom` :</span><span class="sxs-lookup"><span data-stu-id="aa2e6-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="aa2e6-110">Ces formats ne sont pas valides pour les attributs à une seule valeur, comme `author`.</span><span class="sxs-lookup"><span data-stu-id="aa2e6-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="aa2e6-111">Si vous avez spécifié plusieurs valeurs, passez en revue les valeurs spécifiées et déterminez la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="aa2e6-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="aa2e6-112">Supprimez les autres valeurs et spécifiez la valeur unique sur la même ligne que l’attribut sans crochets, comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa2e6-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="aa2e6-113">Si vous avez un tableau à valeur unique, attribuez-lui le format scalaire ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="aa2e6-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="aa2e6-114">Attributs dans l’étendue</span><span class="sxs-lookup"><span data-stu-id="aa2e6-114">Attributes in scope</span></span>

<span data-ttu-id="aa2e6-115">Les attributs suivants doivent être à valeur unique :</span><span class="sxs-lookup"><span data-stu-id="aa2e6-115">The following attributes are required to be single-valued:</span></span>

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
