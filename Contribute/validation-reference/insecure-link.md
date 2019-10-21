---
title: insecure-link
description: Explication et résolution du problème de génération Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: b97d4c4a0f61e5f3448331a56fe4bde442ff1cca
ms.sourcegitcommit: 0cb0177c209abab1a72af4f411ef527fa5cf10f9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2019
ms.locfileid: "72379510"
---
# <a name="insecure-link"></a><span data-ttu-id="83963-103">insecure-link</span><span class="sxs-lookup"><span data-stu-id="83963-103">insecure-link</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="83963-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="83963-104">Suggestion</span></span>

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

<span data-ttu-id="83963-105">Ce message signifie que vous avez utilisé un lien Markdown explicite avec `http` ou que vous avez utilisé une URL brute, comme `www.microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="83963-105">This message means that you either used an explicit Markdown link with `http` or you used a raw URL, such as `www.microsoft.com`.</span></span> <span data-ttu-id="83963-106">Les URL brutes sont converties en liens non sécurisés quand elles sont publiées sur Docs ; elles ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="83963-106">Raw URLs are converted to insecure links when published to Docs, and should not be used.</span></span>

## <a name="resolution"></a><span data-ttu-id="83963-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="83963-107">Resolution</span></span>

<span data-ttu-id="83963-108">Changez toutes les URL vers des sites Microsoft pour qu’elles utilisent `https` au lieu de `http`.</span><span class="sxs-lookup"><span data-stu-id="83963-108">Change all URLs to Microsoft sites to use `https` instead of `http`.</span></span>

<span data-ttu-id="83963-109">Si votre lien est une URL brute, remplacez-le par un lien Markdown explicite commençant par `https`.</span><span class="sxs-lookup"><span data-stu-id="83963-109">If your link is a raw URL, change it to an explicit Markdown link beginning with `https`.</span></span>

> [!TIP]
> <span data-ttu-id="83963-110">L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft.</span><span class="sxs-lookup"><span data-stu-id="83963-110">The Docs Markdown extension for VS Code includes a cleanup script for Microsoft links.</span></span> <span data-ttu-id="83963-111">Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`.</span><span class="sxs-lookup"><span data-stu-id="83963-111">The script checks all links to Microsoft sites in a repo to ensure that they begin with `https` instead of `http` and don't contain locale codes, such as `en-us`.</span></span> <span data-ttu-id="83963-112">Pour exécuter le script :</span><span class="sxs-lookup"><span data-stu-id="83963-112">To run the script:</span></span>
>
> 1. <span data-ttu-id="83963-113">Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="83963-113">Install the [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) extension for VS Code.</span></span>
> 1. <span data-ttu-id="83963-114">Appuyez sur Alt+M pour ouvrir le menu de Markdown.</span><span class="sxs-lookup"><span data-stu-id="83963-114">Click alt + M to open the Markdown menu.</span></span>
> 1. <span data-ttu-id="83963-115">Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).</span><span class="sxs-lookup"><span data-stu-id="83963-115">Select **Cleanup**, then **Microsoft links**.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
