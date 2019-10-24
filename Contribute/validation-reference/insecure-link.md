---
title: insecure-link
description: Explication et résolution du problème de génération Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587672"
---
# <a name="insecure-link"></a><span data-ttu-id="5dad7-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="5dad7-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dad7-104">Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels.</span><span class="sxs-lookup"><span data-stu-id="5dad7-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="5dad7-105">**Elle va devenir un « Avertissement » le 20/12/2019**.</span><span class="sxs-lookup"><span data-stu-id="5dad7-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="5dad7-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5dad7-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="5dad7-107">Ce message signifie que vous avez utilisé un lien Markdown explicite avec `http` ou que vous avez utilisé une URL brute, comme `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="5dad7-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="5dad7-108">Les URL brutes sont converties en liens non sécurisés quand elles sont publiées sur Docs ; elles ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="5dad7-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="5dad7-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="5dad7-109">Resolution</span></span>

<span data-ttu-id="5dad7-110">Changez toutes les URL vers des sites Microsoft pour qu’elles utilisent `https` au lieu de `http`.</span><span class="sxs-lookup"><span data-stu-id="5dad7-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="5dad7-111">Si votre lien est une URL brute, remplacez-le par un lien Markdown explicite commençant par `https`.</span><span class="sxs-lookup"><span data-stu-id="5dad7-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="5dad7-112">L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dad7-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="5dad7-113">Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`.</span><span class="sxs-lookup"><span data-stu-id="5dad7-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="5dad7-114">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="5dad7-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="5dad7-115">Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="5dad7-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="5dad7-116">Appuyez sur Alt+M pour ouvrir le menu de Markdown.</span><span class="sxs-lookup"><span data-stu-id="5dad7-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="5dad7-117">Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).</span><span class="sxs-lookup"><span data-stu-id="5dad7-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
