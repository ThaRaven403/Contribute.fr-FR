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
# <a name="image-compression"></a><span data-ttu-id="e2cbe-103">Compression d’image</span><span class="sxs-lookup"><span data-stu-id="e2cbe-103">Image compression</span></span>

[!INCLUDE [markdown-extension](includes/image-extension.md)]

## <a name="summary"></a><span data-ttu-id="e2cbe-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="e2cbe-104">Summary</span></span>

<span data-ttu-id="e2cbe-105">Toute la documentation est fournie via le web, à l’exception des versions PDF de la documentation. Quand vous servez du contenu statique, il est préférable de réduire le nombre d’octets envoyés sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-105">All documentation is provided via the web, with the exception of PDF versions of docs. When serving static content, it is best to minimize the number of bytes sent over the wire.</span></span> <span data-ttu-id="e2cbe-106">Une façon de procéder consiste à compresser les images au repos.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-106">One way to do that is to compress images at rest.</span></span>

<span data-ttu-id="e2cbe-107">L’extension Docs Authoring Pack comprend des éléments de menu contextuel de compression d’image.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-107">The Docs Authoring Pack extension includes image compression context menu items.</span></span> <span data-ttu-id="e2cbe-108">Les extensions/types d’images suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="e2cbe-108">The following image types / extensions are supported:</span></span>

* <span data-ttu-id="e2cbe-109">*\*.png*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-109">*\*.png*</span></span>
* <span data-ttu-id="e2cbe-110">*\*.jpg*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-110">*\*.jpg*</span></span>
* <span data-ttu-id="e2cbe-111">*\*.jpeg*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-111">*\*.jpeg*</span></span>
* <span data-ttu-id="e2cbe-112">*\*.gif*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-112">*\*.gif*</span></span>
* <span data-ttu-id="e2cbe-113">*\*.svg*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-113">*\*.svg*</span></span>
* <span data-ttu-id="e2cbe-114">*\*.webp*</span><span class="sxs-lookup"><span data-stu-id="e2cbe-114">*\*.webp*</span></span>

<span data-ttu-id="e2cbe-115">Les algorithmes de compression d’image sans perte sont utilisés, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-115">The lossless image compression algorithms are used, where applicable.</span></span>

## <a name="compress-image"></a><span data-ttu-id="e2cbe-116">Compresser une image</span><span class="sxs-lookup"><span data-stu-id="e2cbe-116">Compress image</span></span>

<span data-ttu-id="e2cbe-117">Dans le volet de navigation de l’**Explorateur**, cliquez avec le bouton droit sur un fichier image, puis sélectionnez l’option **Compress image** (Compresser l’image).</span><span class="sxs-lookup"><span data-stu-id="e2cbe-117">From the **Explorer** navigation pane, right-click on an image file - then select the **Compress image** option.</span></span> <span data-ttu-id="e2cbe-118">L’image est ensuite compressée.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-118">The image is then compressed.</span></span>

## <a name="compress-images-in-folder"></a><span data-ttu-id="e2cbe-119">Compresser des images dans le dossier</span><span class="sxs-lookup"><span data-stu-id="e2cbe-119">Compress images in folder</span></span>

<span data-ttu-id="e2cbe-120">Dans le volet de navigation de l’**Explorateur**, cliquez avec le bouton droit sur un dossier contenant des images, puis sélectionnez l’option **Compress images in folder** (Compresser les images du dossier).</span><span class="sxs-lookup"><span data-stu-id="e2cbe-120">From the **Explorer** navigation pane, right-click on a folder containing images - then select the **Compress images in folder** option.</span></span> <span data-ttu-id="e2cbe-121">Toutes les images du dossier sont compressées.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-121">All images in the folder are compressed.</span></span>

## <a name="considerations"></a><span data-ttu-id="e2cbe-122">Observations</span><span class="sxs-lookup"><span data-stu-id="e2cbe-122">Considerations</span></span>

<span data-ttu-id="e2cbe-123">Les images de grande résolution sont redimensionnées implicitement.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-123">Large resolution images are implicitly resized.</span></span> <span data-ttu-id="e2cbe-124">Les dimensions maximales sont basées sur la largeur maximale de `1,200px` suggérée par la plateforme.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-124">The maximum dimensions are based on the platform suggested max width of `1,200px`.</span></span> <span data-ttu-id="e2cbe-125">La valeur maximale est utilisée uniquement quand les images sont plus volumineuses que leur taille recommandée et elles conservent les proportions quand elles sont automatiquement redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-125">The max is only used when images are larger than they are recommended to be, and they will maintain the aspect ratio when automatically resized.</span></span>

## <a name="preferences"></a><span data-ttu-id="e2cbe-126">Préférences</span><span class="sxs-lookup"><span data-stu-id="e2cbe-126">Preferences</span></span>

<span data-ttu-id="e2cbe-127">Les dimensions maximales sont configurables, mais il existe une largeur maximale par défaut de `1200` pixels.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-127">The maximum dimensions are configurable, but a default max width of `1200` pixels exists.</span></span> <span data-ttu-id="e2cbe-128">Pour configurer les dimensions maximales, sélectionnez **Fichier-> Préférences-> Paramètres** et filtrez par `"Docs Image Extension"`.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-128">To configure the max dimensions, select **File -> Preferences -> Settings** and filter by `"Docs Image Extension"`.</span></span>

:::image type="content" source="media/configure-image-compression.png" alt-text="Configurer la compression d’image":::

> [!NOTE]
> <span data-ttu-id="e2cbe-130">Si **Max Width** (Largeur maximale) ou **Max Height** (Hauteur maximale) a pour valeur `0`, les variantes de résolution sont simplement ignorées.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-130">A value of `0` in either the **Max Width** or **Max Height** will simply ignore resolution variances.</span></span>

## <a name="in-action"></a><span data-ttu-id="e2cbe-131">En action</span><span class="sxs-lookup"><span data-stu-id="e2cbe-131">In action</span></span>

<span data-ttu-id="e2cbe-132">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="e2cbe-132">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="e2cbe-133">[![Démonstration de la compression d’image](media/compress-image.gif)](media/compress-image.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="e2cbe-133">[![Compress image demo](media/compress-image.gif)](media/compress-image.gif#lightbox)</span></span>
