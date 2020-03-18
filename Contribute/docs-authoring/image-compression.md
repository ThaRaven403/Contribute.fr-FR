---
title: Compression d’image - Docs Authoring Pack
description: Découvrez comment compresser des images dans l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 4b93ac23b83128d5b9125297879d008e9300509c
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336655"
---
# <a name="image-compression"></a>Compression d’image

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a>Récapitulatif

Toute la documentation est fournie via le web, à l’exception des versions PDF de la documentation. Quand vous servez du contenu statique, il est préférable de réduire le nombre d’octets envoyés sur le réseau. Une façon de procéder consiste à compresser les images au repos.

L’extension Docs Authoring Pack comprend des éléments de menu contextuel de compression d’image. Les extensions/types d’images suivants sont pris en charge :

* *\*.png*
* *\*.jpg*
* *\*.jpeg*
* *\*.gif*
* *\*.svg*
* *\*.webp*

Les algorithmes de compression d’image sans perte sont utilisés, le cas échéant.

## <a name="compress-image"></a>Compresser une image

Dans le volet de navigation de l’**Explorateur**, cliquez avec le bouton droit sur un fichier image, puis sélectionnez l’option **Compress image** (Compresser l’image). L’image est ensuite compressée.

## <a name="compress-images-in-folder"></a>Compresser des images dans le dossier

Dans le volet de navigation de l’**Explorateur**, cliquez avec le bouton droit sur un dossier contenant des images, puis sélectionnez l’option **Compress images in folder** (Compresser les images du dossier). Toutes les images du dossier sont compressées.

## <a name="considerations"></a>Observations

Les images de grande résolution sont redimensionnées implicitement. Les dimensions maximales sont basées sur la largeur maximale de `1,200px` suggérée par la plateforme. La valeur maximale est utilisée uniquement quand les images sont plus volumineuses que leur taille recommandée et elles conservent les proportions quand elles sont automatiquement redimensionnées.

## <a name="preferences"></a>Préférences

Les dimensions maximales sont configurables, mais il existe une largeur maximale par défaut de `1200` pixels. Pour configurer les dimensions maximales, sélectionnez **Fichier-> Préférences-> Paramètres** et filtrez par `"Docs Image Extension"`.

:::image type="content" source="media/configure-image-compression.png" alt-text="Configurer la compression d’image":::

> [!NOTE]
> Si **Max Width** (Largeur maximale) ou **Max Height** (Hauteur maximale) a pour valeur `0`, les variantes de résolution sont simplement ignorées.

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démonstration de la compression d’image](media/compress-image.gif)](media/compress-image.gif#lightbox)
