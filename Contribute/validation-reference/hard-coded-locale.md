---
title: hard-coded-locale
description: Explication et résolution du problème de génération Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166829"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="68e22-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="68e22-103">hard-coded-locale</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68e22-104">Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels.</span><span class="sxs-lookup"><span data-stu-id="68e22-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="68e22-105">**Elle va devenir un « Avertissement » le 20/12/2019**.</span><span class="sxs-lookup"><span data-stu-id="68e22-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="68e22-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="68e22-106">Suggestion</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

<span data-ttu-id="68e22-107">Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68e22-107">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="68e22-108">Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit.</span><span class="sxs-lookup"><span data-stu-id="68e22-108">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="68e22-109">Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.</span><span class="sxs-lookup"><span data-stu-id="68e22-109">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="68e22-110">Les sites suivants sont dans la portée de cette validation :</span><span class="sxs-lookup"><span data-stu-id="68e22-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="68e22-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="68e22-111">azure.microsoft.com</span></span>
- <span data-ttu-id="68e22-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="68e22-112">docs.microsoft.com</span></span>
- <span data-ttu-id="68e22-113">msdn.microsoft.com (à l’exception de social.msdn.com, qui doit avoir des paramètres régionaux pour être sûr qu’il est lié au forum approprié)</span><span class="sxs-lookup"><span data-stu-id="68e22-113">msdn.microsoft.com (excluding social.msdn.com, which needs locale to ensure the correct forum is linked to)</span></span>
- <span data-ttu-id="68e22-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="68e22-114">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="68e22-115">Résolution</span><span class="sxs-lookup"><span data-stu-id="68e22-115">Resolution</span></span>

<span data-ttu-id="68e22-116">Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68e22-116">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="68e22-117">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="68e22-117">The following is an example.</span></span>

<span data-ttu-id="68e22-118">Avant :</span><span class="sxs-lookup"><span data-stu-id="68e22-118">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="68e22-119">Après :</span><span class="sxs-lookup"><span data-stu-id="68e22-119">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="68e22-120">L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="68e22-120">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="68e22-121">Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`.</span><span class="sxs-lookup"><span data-stu-id="68e22-121">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="68e22-122">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="68e22-122">To run the script:</span></span>
>
> 1. <span data-ttu-id="68e22-123">Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="68e22-123">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="68e22-124">Appuyez sur Alt+M pour ouvrir le menu de Markdown.</span><span class="sxs-lookup"><span data-stu-id="68e22-124">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="68e22-125">Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).</span><span class="sxs-lookup"><span data-stu-id="68e22-125">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
