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
# <a name="sort-redirects"></a><span data-ttu-id="546f8-103">Trier les redirections</span><span class="sxs-lookup"><span data-stu-id="546f8-103">Sort redirects</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="546f8-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="546f8-104">Summary</span></span>

<span data-ttu-id="546f8-105">À mesure qu’un docset docs.microsoft.com évolue, certains fichiers Markdown finissent par être supprimés.</span><span class="sxs-lookup"><span data-stu-id="546f8-105">With the evolution of a docs.microsoft.com docset, some Markdown files eventually will be deleted.</span></span> <span data-ttu-id="546f8-106">Quand un fichier Markdown est supprimé, nous devons fournir une redirection afin que toute référence à l’article supprimé soit correctement résolue par la redirection.</span><span class="sxs-lookup"><span data-stu-id="546f8-106">When a Markdown file is deleted, we're required to provide a redirect so that any reference to the deleted article is properly resolved via the redirect.</span></span> <span data-ttu-id="546f8-107">Les redirections sont spécifiées dans le fichier *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="546f8-107">Redirections are specified in the *.openpublishing.redirection.json* file.</span></span>

1. <span data-ttu-id="546f8-108">Ouvrez la palette de commandes, puis appuyez sur <kbd>F1</kbd> (ou <kbd>⇧⌘P</kbd> sur macOS).</span><span class="sxs-lookup"><span data-stu-id="546f8-108">Open the Command Palette, press <kbd>F1</kbd> (or <kbd>⇧⌘P</kbd> on macOS)</span></span>
1. <span data-ttu-id="546f8-109">Tapez : **Docs : Sort master redirection file** (Trier le fichier de redirection maître)</span><span class="sxs-lookup"><span data-stu-id="546f8-109">Type: **Docs: Sort master redirection file**</span></span>
1. <span data-ttu-id="546f8-110">Sélectionnez la commande pour l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="546f8-110">Select the command to execute it</span></span>
1. <span data-ttu-id="546f8-111">Observez les changements apportés au fichier *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="546f8-111">Observe changes to *.openpublishing.redirection.json* file</span></span>

## <a name="considerations"></a><span data-ttu-id="546f8-112">Observations</span><span class="sxs-lookup"><span data-stu-id="546f8-112">Considerations</span></span>

<span data-ttu-id="546f8-113">Le concept de « chaînage » est lié à la conception initiale du fichier *.openpublishing.redirection.json*.</span><span class="sxs-lookup"><span data-stu-id="546f8-113">The concept of "daisy chaining" exists with how the *.openpublishing.redirection.json* file was originally designed.</span></span> <span data-ttu-id="546f8-114">Au fil du temps, les fichiers ajoutés en tant que redirection finissent par devenir obsolètes.</span><span class="sxs-lookup"><span data-stu-id="546f8-114">Over time, files added as a redirect will eventually become stale.</span></span> <span data-ttu-id="546f8-115">Cela se produit quand le fichier A est supprimé et nécessite une redirection vers le fichier B, puis que le fichier B est supprimé, puis redirigé vers le fichier C. Idéalement, les deux entrées pointent vers C, afin que A soit redirigé vers C et que B reste le même.</span><span class="sxs-lookup"><span data-stu-id="546f8-115">This happens when file A is deleted and needs a redirect to file B, then later file B is deleted and then redirects to file C. Ideally, both entries would point to C - so that A redirects to C, and B remains the same.</span></span> <span data-ttu-id="546f8-116">Il s’agit d’un gain de performances mineur alors que vous passez beaucoup de temps sur la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="546f8-116">This is a minor performance gain, and the feature is actively being worked on.</span></span>

## <a name="in-action"></a><span data-ttu-id="546f8-117">En action</span><span class="sxs-lookup"><span data-stu-id="546f8-117">In action</span></span>

<span data-ttu-id="546f8-118">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="546f8-118">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="546f8-119">[![Démo de tri de redirections](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="546f8-119">[![Sort redirects demo](media/sort-redirect.gif)](media/sort-redirect.gif#lightbox)</span></span>
