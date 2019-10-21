---
title: hard-coded-locale
description: Explication et résolution du problème de génération Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: eb9ae17673b3da5f921139d88cc9af469423c9c3
ms.sourcegitcommit: d357977935b432381f3df6297164417ed59ab434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2019
ms.locfileid: "72310333"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="53421-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="53421-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="53421-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="53421-104">Warning</span></span>

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to Microsoft sites.`

<span data-ttu-id="53421-105">Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53421-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="53421-106">Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit.</span><span class="sxs-lookup"><span data-stu-id="53421-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="53421-107">Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.</span><span class="sxs-lookup"><span data-stu-id="53421-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="53421-108">Les sites suivants sont dans la portée de cette validation :</span><span class="sxs-lookup"><span data-stu-id="53421-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="53421-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="53421-109">azure.microsoft.com</span></span>
- <span data-ttu-id="53421-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="53421-110">docs.microsoft.com</span></span>
- <span data-ttu-id="53421-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="53421-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="53421-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="53421-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="53421-113">Résolution</span><span class="sxs-lookup"><span data-stu-id="53421-113">Resolution</span></span>

<span data-ttu-id="53421-114">Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53421-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="53421-115">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="53421-115">The following is an example.</span></span>

<span data-ttu-id="53421-116">Avant :</span><span class="sxs-lookup"><span data-stu-id="53421-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="53421-117">Après :</span><span class="sxs-lookup"><span data-stu-id="53421-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> <span data-ttu-id="53421-118">L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="53421-118">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="53421-119">Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`.</span><span class="sxs-lookup"><span data-stu-id="53421-119">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="53421-120">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="53421-120">To run the script:</span></span>
>
> 1. <span data-ttu-id="53421-121">Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="53421-121">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="53421-122">Appuyez sur Alt+M pour ouvrir le menu de Markdown.</span><span class="sxs-lookup"><span data-stu-id="53421-122">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="53421-123">Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).</span><span class="sxs-lookup"><span data-stu-id="53421-123">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]