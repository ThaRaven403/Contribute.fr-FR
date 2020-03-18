---
title: Trier les redirections - Docs Authoring Pack
description: Découvrez comment trier les redirections avec l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4924c631c8720743c283083e53b3a1e9af86b00a
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336678"
---
# <a name="sort-redirects"></a>Trier les redirections

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

À mesure qu’un docset docs.microsoft.com évolue, certains fichiers Markdown finissent par être supprimés. Quand un fichier Markdown est supprimé, nous devons fournir une redirection afin que toute référence à l’article supprimé soit correctement résolue par la redirection. Les redirections sont spécifiées dans le fichier *.openpublishing.redirection.json*.

1. Ouvrez la palette de commandes, puis appuyez sur <kbd>F1</kbd> (ou <kbd>⇧⌘P</kbd> sur macOS).
1. Tapez : **Docs : Sort master redirection file** (Trier le fichier de redirection maître)
1. Sélectionnez la commande pour l’exécuter.
1. Observez les changements apportés au fichier *.openpublishing.redirection.json*.

## <a name="considerations"></a>Observations

Le concept de « chaînage » est lié à la conception initiale du fichier *.openpublishing.redirection.json*. Au fil du temps, les fichiers ajoutés en tant que redirection finissent par devenir obsolètes. Cela se produit quand le fichier A est supprimé et nécessite une redirection vers le fichier B, puis que le fichier B est supprimé, puis redirigé vers le fichier C. Idéalement, les deux entrées pointent vers C, afin que A soit redirigé vers C et que B reste le même. Il s’agit d’un gain de performances mineur alors que vous passez beaucoup de temps sur la fonctionnalité.

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démo de tri de redirections](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)
