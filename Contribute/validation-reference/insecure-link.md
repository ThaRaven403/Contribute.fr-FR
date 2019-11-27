---
title: insecure-link
description: Explication et résolution du problème de génération Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528841"
---
# <a name="insecure-link"></a><span data-ttu-id="c2e22-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="c2e22-103">insecure-link</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2e22-104">Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels.</span><span class="sxs-lookup"><span data-stu-id="c2e22-104">This rule was initially enabled as a "Suggestion" to give content teams time to gauge impact and develop a plan to clean up their repos.</span></span> <span data-ttu-id="c2e22-105">**Elle va devenir un « Avertissement » le 20/12/2019**.</span><span class="sxs-lookup"><span data-stu-id="c2e22-105">**It will be elevated to a "Warning" on 12/20/2019**.</span></span>

## <a name="suggestion"></a><span data-ttu-id="c2e22-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="c2e22-106">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="c2e22-107">Ce message signifie que vous avez utilisé un lien Markdown explicite avec `http` ou que vous avez utilisé une URL brute, comme `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="c2e22-107">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="c2e22-108">Les URL brutes sont converties en liens non sécurisés quand elles sont publiées sur Docs ; elles ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="c2e22-108">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="c2e22-109">Résolution</span><span class="sxs-lookup"><span data-stu-id="c2e22-109">Resolution</span></span>

<span data-ttu-id="c2e22-110">Changez toutes les URL vers des sites Microsoft pour qu’elles utilisent `https` au lieu de `http`.</span><span class="sxs-lookup"><span data-stu-id="c2e22-110">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="c2e22-111">Si votre lien est une URL brute, remplacez-le par un lien Markdown explicite commençant par `https`, comme :</span><span class="sxs-lookup"><span data-stu-id="c2e22-111">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`, such as:</span></span>

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> <span data-ttu-id="c2e22-112">L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2e22-112">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="c2e22-113">Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`.</span><span class="sxs-lookup"><span data-stu-id="c2e22-113">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="c2e22-114">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="c2e22-114">To run the script:</span></span>
>
> 1. <span data-ttu-id="c2e22-115">Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="c2e22-115">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="c2e22-116">Appuyez sur Alt+M pour ouvrir le menu de Markdown.</span><span class="sxs-lookup"><span data-stu-id="c2e22-116">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="c2e22-117">Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).</span><span class="sxs-lookup"><span data-stu-id="c2e22-117">Select **Cleanup**, then **Microsoft links**.</span></span>

<span data-ttu-id="c2e22-118">Dans certains cas, vous devrez certainement documenter des adresses web, telles que des noms de domaine complets, qui ne sont pas censées être des liens cliquables.</span><span class="sxs-lookup"><span data-stu-id="c2e22-118">In some cases, you might need to document web addresses, such as fully-qualified domain names, that aren't meant to be clickable links.</span></span> <span data-ttu-id="c2e22-119">Elles doivent être mises en forme en tant que code inline, comme :</span><span class="sxs-lookup"><span data-stu-id="c2e22-119">These should be styled as inline code, such as:</span></span>

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
