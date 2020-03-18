---
title: Modifier la mise en forme des tableaux Markdown - Docs Authoring Pack
description: Découvrez comment utiliser les différentes fonctionnalités de mise en forme des tableaux Markdown à partir de l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 07c95f2a0d24a49f59eaffe1bec64ee872530c2f
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336770"
---
# <a name="reformat-markdown-tables"></a><span data-ttu-id="034e1-103">Modifier la mise en forme des tableaux Markdown</span><span class="sxs-lookup"><span data-stu-id="034e1-103">Reformat Markdown tables</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="034e1-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="034e1-104">Summary</span></span>

<span data-ttu-id="034e1-105">Dans un fichier Markdown ( *\*.md*), quand vous sélectionnez un tableau complet, deux éléments de menu contextuel de mise en forme des tableaux sont désormais disponibles.</span><span class="sxs-lookup"><span data-stu-id="034e1-105">In a Markdown (*\*.md*) file, when you select a complete table - two table formatting context menu items are now available.</span></span> <span data-ttu-id="034e1-106">Cliquez avec le bouton droit sur le tableau Markdown sélectionné pour ouvrir le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="034e1-106">Right-click on the selected Markdown table to open the context menu.</span></span> <span data-ttu-id="034e1-107">Vous voyez quelque chose de similaire aux éléments de menu suivants :</span><span class="sxs-lookup"><span data-stu-id="034e1-107">You will see something similar to the following menu items:</span></span>

:::image type="content" source="media/reformat-table-menu.png" alt-text="Menu contextuel de modification de la mise en forme des tableaux":::

> [!TIP]
> <span data-ttu-id="034e1-109">Cette fonctionnalité **ne fonctionne pas** avec plusieurs sélections de tableau ; elle s’applique à un seul tableau Markdown.</span><span class="sxs-lookup"><span data-stu-id="034e1-109">This feature **does not** work with multiple table selections, but rather is intended for a single Markdown table.</span></span> <span data-ttu-id="034e1-110">Vous devez sélectionner la totalité de la table, y compris les en-têtes pour obtenir les résultats souhaités.</span><span class="sxs-lookup"><span data-stu-id="034e1-110">You must select the entire table, including headings for desired results.</span></span>

## <a name="consolidate-selected-table"></a><span data-ttu-id="034e1-111">Compacter le tableau sélectionné</span><span class="sxs-lookup"><span data-stu-id="034e1-111">Consolidate selected table</span></span>

<span data-ttu-id="034e1-112">La sélection de l’option **Consolidate selected table** (Compacter le tableau sélectionné) réduit les en-têtes et le contenu du tableau avec un seul espace de chaque côté de chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="034e1-112">Selecting the **Consolidate selected table** option will collapse the table headings and contents with only a single space on either side of each value.</span></span>

## <a name="evenly-distribute-selected-table"></a><span data-ttu-id="034e1-113">Distribuer uniformément le tableau sélectionné</span><span class="sxs-lookup"><span data-stu-id="034e1-113">Evenly distribute selected table</span></span>

<span data-ttu-id="034e1-114">La sélection de l’option **Evenly distribute selected table** (Distribuer uniformément le tableau sélectionné) calcule la valeur la plus longue dans chaque colonne et distribue uniformément toutes les autres valeurs en conséquence en insérant des espaces.</span><span class="sxs-lookup"><span data-stu-id="034e1-114">Selecting the **Evenly distribute selected table** option will calculate the longest value in each column and evenly distribute all the other values accordingly with space.</span></span>

## <a name="considerations"></a><span data-ttu-id="034e1-115">Observations</span><span class="sxs-lookup"><span data-stu-id="034e1-115">Considerations</span></span>

<span data-ttu-id="034e1-116">La fonctionnalité n’impacte pas le rendu du tableau, mais elle aide à améliorer sa lisibilité, ce qui facilite sa gestion.</span><span class="sxs-lookup"><span data-stu-id="034e1-116">The feature will not impact the rendering of the table, but it will help to improve the readability of the table - thus making more maintainable.</span></span> <span data-ttu-id="034e1-117">La fonctionnalité de modification de la mise en forme des tableaux conserve l’alignement des colonnes intact.</span><span class="sxs-lookup"><span data-stu-id="034e1-117">The reformatting table feature will keep column alignment intact.</span></span>

<span data-ttu-id="034e1-118">Soit le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="034e1-118">Consider the following table:</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|--:|---------|:--:|:----|
||         |  |         |
|     |  |         |   a value      |
||         |         |         |
|     |         | This is a long value |       but why? |
|     |         |         |         |
|     |                                           |         | Here is something |
|  |         |   |         |
```

<span data-ttu-id="034e1-119">Après distribution uniforme :</span><span class="sxs-lookup"><span data-stu-id="034e1-119">After being "evenly distributed":</span></span>

```markdown
| Column1 | This is a long column name | Column3              |                   |
|--------:|----------------------------|:--------------------:|:------------------|
|         |                            |                      |                   |
|         |                            |                      | a value           |
|         |                            |                      |                   |
|         |                            | This is a long value | but why?          |
|         |                            |                      |                   |
|         |                            |                      | Here is something |
|         |                            |                      |                   |
```

<span data-ttu-id="034e1-120">Après compactage :</span><span class="sxs-lookup"><span data-stu-id="034e1-120">After being "consolidated":</span></span>

```markdown
| Column1 | This is a long column name | Column3 |  |
|-:|--|:-:|:-|
|  |  |  |  |
|  |  |  | a value |
|  |  |  |  |
|  |  | This is a long value | but why? |
|  |  |  |  |
|  |  |  | Here is something |
|  |  |  |  |
```

## <a name="in-action"></a><span data-ttu-id="034e1-121">En action</span><span class="sxs-lookup"><span data-stu-id="034e1-121">In action</span></span>

<span data-ttu-id="034e1-122">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="034e1-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="034e1-123">[![Démonstration de la modification de la mise en forme des tableaux](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="034e1-123">[![Reformat table demo](media/reformat-table.gif)](media/reformat-table.gif#lightbox)</span></span>
