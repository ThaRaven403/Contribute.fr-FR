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
# <a name="reformat-markdown-tables"></a>Modifier la mise en forme des tableaux Markdown

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

Dans un fichier Markdown ( *\*.md*), quand vous sélectionnez un tableau complet, deux éléments de menu contextuel de mise en forme des tableaux sont désormais disponibles. Cliquez avec le bouton droit sur le tableau Markdown sélectionné pour ouvrir le menu contextuel. Vous voyez quelque chose de similaire aux éléments de menu suivants :

:::image type="content" source="media/reformat-table-menu.png" alt-text="Menu contextuel de modification de la mise en forme des tableaux":::

> [!TIP]
> Cette fonctionnalité **ne fonctionne pas** avec plusieurs sélections de tableau ; elle s’applique à un seul tableau Markdown. Vous devez sélectionner la totalité de la table, y compris les en-têtes pour obtenir les résultats souhaités.

## <a name="consolidate-selected-table"></a>Compacter le tableau sélectionné

La sélection de l’option **Consolidate selected table** (Compacter le tableau sélectionné) réduit les en-têtes et le contenu du tableau avec un seul espace de chaque côté de chaque valeur.

## <a name="evenly-distribute-selected-table"></a>Distribuer uniformément le tableau sélectionné

La sélection de l’option **Evenly distribute selected table** (Distribuer uniformément le tableau sélectionné) calcule la valeur la plus longue dans chaque colonne et distribue uniformément toutes les autres valeurs en conséquence en insérant des espaces.

## <a name="considerations"></a>Observations

La fonctionnalité n’impacte pas le rendu du tableau, mais elle aide à améliorer sa lisibilité, ce qui facilite sa gestion. La fonctionnalité de modification de la mise en forme des tableaux conserve l’alignement des colonnes intact.

Soit le tableau suivant :

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

Après distribution uniforme :

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

Après compactage :

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

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démonstration de la modification de la mise en forme des tableaux](media/reformat-table.gif)](media/reformat-table.gif#lightbox)
