---
title: Tri de la sélection - Docs Authoring Pack
description: Découvrez comment utiliser la fonctionnalité de tri de la sélection à partir de l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: b4bd1761dc1bd9326275f011bb1935f6b695404d
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336747"
---
# <a name="sort-selection"></a><span data-ttu-id="21cc3-103">Trier la sélection</span><span class="sxs-lookup"><span data-stu-id="21cc3-103">Sort selection</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="21cc3-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="21cc3-104">Summary</span></span>

<span data-ttu-id="21cc3-105">Dans un fichier Markdown ( *\*.md*), quand vous avez effectué une sélection, deux éléments de menu contextuel de tri sont désormais disponibles.</span><span class="sxs-lookup"><span data-stu-id="21cc3-105">In a Markdown (*\*.md*) file, when you've made a selection - two sorting context menu items are now available.</span></span> <span data-ttu-id="21cc3-106">Cliquez avec le bouton droit sur le texte sélectionné pour ouvrir le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="21cc3-106">Right-click on the selected text to open the context menu.</span></span> <span data-ttu-id="21cc3-107">Vous voyez quelque chose de similaire aux éléments de menu suivants :</span><span class="sxs-lookup"><span data-stu-id="21cc3-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/sort-selection-menu.png" alt-text="Menu contextuel de tri de la sélection":::

> [!TIP]
> <span data-ttu-id="21cc3-109">Les éléments de menu contextuel de tri sont masqués jusqu’à ce qu’il y ait une sélection valide dans l’éditeur de texte Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="21cc3-109">The sorting context menu items are hidden until there is a valid selection in the Visual Studio Code text editor.</span></span>

## <a name="sort-selection-ascending-a-to-z"></a><span data-ttu-id="21cc3-110">Trier la sélection par ordre croissant (de A à Z)</span><span class="sxs-lookup"><span data-stu-id="21cc3-110">Sort selection ascending (A to Z)</span></span>

<span data-ttu-id="21cc3-111">La sélection de l’option **Sort selection ascending (A to Z)** (Trier la sélection par ordre croissant (de A à Z)) permet de trier l’ensemble de la sélection dans l’ordre croissant, par ordre alphabétique de A à Z.</span><span class="sxs-lookup"><span data-stu-id="21cc3-111">Selecting the **Sort selection ascending (A to Z)** option will sort the entire selection ascending, alphabetically from A to Z.</span></span>

## <a name="sort-selection-descending-z-to-a"></a><span data-ttu-id="21cc3-112">Trier la sélection par ordre décroissant (Z à A)</span><span class="sxs-lookup"><span data-stu-id="21cc3-112">Sort selection descending (Z to A)</span></span>

<span data-ttu-id="21cc3-113">La sélection de l’option **Sort selection descending (Z to A)** (Trier la sélection par ordre décroissant (Z à A)) permet de trier l’ensemble de la sélection dans l’ordre décroissant, par ordre alphabétique de Z à A.</span><span class="sxs-lookup"><span data-stu-id="21cc3-113">Selecting the **Sort selection descending (Z to A)** option will sort the entire selection ascending, alphabetically from Z to A.</span></span>

## <a name="considerations"></a><span data-ttu-id="21cc3-114">Observations</span><span class="sxs-lookup"><span data-stu-id="21cc3-114">Considerations</span></span>

<span data-ttu-id="21cc3-115">Le mécanisme de tri sous-jacent utilise le tri en *langage naturel*.</span><span class="sxs-lookup"><span data-stu-id="21cc3-115">The underlying sorting mechanism uses *natural language* sorting.</span></span> <span data-ttu-id="21cc3-116">Cela le rend plus puissant et plus complet que le tri standard.</span><span class="sxs-lookup"><span data-stu-id="21cc3-116">This makes it more powerful and comprehensive than standard sorting.</span></span> <span data-ttu-id="21cc3-117">Soit le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="21cc3-117">Consider the following table:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| 2       | Number 2                               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
| 11      | Number 11                              |
```

<span data-ttu-id="21cc3-118">Sans tri en langage naturel, l’ordre pour `Column1` aurait été 1, 11, 2, etc., mais il comprend que 11 est supérieur à 2, ce qui se traduit par l’ordre croissant suivant :</span><span class="sxs-lookup"><span data-stu-id="21cc3-118">Without natural language sorting, the order for `Column1` would have been 1, 11, 2, etc. but instead it understands that 11 is greater than 2 - resulting in the following ascending order:</span></span>

```markdown
| Column1 | Column2                                |
|---------|----------------------------------------|
| 1       | Number 1                               |
| 2       | Number 2                               |
| 11      | Number 11                              |
| Aa      | The first letter in the alphabet       |
| Ab      | The first letter in the alphabet       |
| C       | The a letter after A in the alphabet   |
| M       | Somewhere in the middle?               |
| X       | The alphabet letter is towards the end |
| Z       | The last letter in the alphabet        |
```

## <a name="in-action"></a><span data-ttu-id="21cc3-119">En action</span><span class="sxs-lookup"><span data-stu-id="21cc3-119">In action</span></span>

<span data-ttu-id="21cc3-120">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="21cc3-120">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="21cc3-121">[![Démonstration du tri de la sélection](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="21cc3-121">[![Sort selection demo](media/sort-selection.gif)](media/sort-selection.gif#lightbox)</span></span>
