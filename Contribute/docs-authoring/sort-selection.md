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
# <a name="sort-selection"></a>Trier la sélection

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

Dans un fichier Markdown ( *\*.md*), quand vous avez effectué une sélection, deux éléments de menu contextuel de tri sont désormais disponibles. Cliquez avec le bouton droit sur le texte sélectionné pour ouvrir le menu contextuel. Vous voyez quelque chose de similaire aux éléments de menu suivants :

:::image type="content" source="media/sort-selection-menu.png" alt-text="Menu contextuel de tri de la sélection":::

> [!TIP]
> Les éléments de menu contextuel de tri sont masqués jusqu’à ce qu’il y ait une sélection valide dans l’éditeur de texte Visual Studio Code.

## <a name="sort-selection-ascending-a-to-z"></a>Trier la sélection par ordre croissant (de A à Z)

La sélection de l’option **Sort selection ascending (A to Z)** (Trier la sélection par ordre croissant (de A à Z)) permet de trier l’ensemble de la sélection dans l’ordre croissant, par ordre alphabétique de A à Z.

## <a name="sort-selection-descending-z-to-a"></a>Trier la sélection par ordre décroissant (Z à A)

La sélection de l’option **Sort selection descending (Z to A)** (Trier la sélection par ordre décroissant (Z à A)) permet de trier l’ensemble de la sélection dans l’ordre décroissant, par ordre alphabétique de Z à A.

## <a name="considerations"></a>Observations

Le mécanisme de tri sous-jacent utilise le tri en *langage naturel*. Cela le rend plus puissant et plus complet que le tri standard. Soit le tableau suivant :

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

Sans tri en langage naturel, l’ordre pour `Column1` aurait été 1, 11, 2, etc., mais il comprend que 11 est supérieur à 2, ce qui se traduit par l’ordre croissant suivant :

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

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démonstration du tri de la sélection](media/sort-selection.gif)](media/sort-selection.gif#lightbox)
