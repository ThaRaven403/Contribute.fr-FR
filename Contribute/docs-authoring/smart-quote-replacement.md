---
title: Remplacement automatique des guillemets courbes - Docs Authoring Pack
description: Découvrez comment remplacer automatiquement les guillemets courbes avec l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336701"
---
# <a name="smart-quote-replacement"></a><span data-ttu-id="7c5f0-103">Remplacement des guillemets courbes</span><span class="sxs-lookup"><span data-stu-id="7c5f0-103">Smart quote replacement</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="7c5f0-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="7c5f0-104">Summary</span></span>

<span data-ttu-id="7c5f0-105">Les développeurs de contenu sont responsables de la création de certaines des fonctionnalités les plus avancées de la technologie et de l’intelligence modernes. Pourtant, nos outils actuels préfèrent l’utilisation de « guillemets droits » dans Markdown.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-105">Content developers are responsible for authoring some of the most advanced features of modern technology and intelligence, yet our tooling today prefers the usage of "dumb quotes" in Markdown.</span></span> <span data-ttu-id="7c5f0-106">À l’opposé nous trouvons naturellement les « guillemets courbes ».</span><span class="sxs-lookup"><span data-stu-id="7c5f0-106">The antonym of course being "smart quotes".</span></span> <span data-ttu-id="7c5f0-107">Les guillemets courbes sont courants avec les typographies idéales, mais ne sont pas privilégiés par Markdown et le rendu du code HTML.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-107">Smart quotes are common with ideal typographies, but not preferred with Markdown and rendered HTML.</span></span>

<span data-ttu-id="7c5f0-108">Quand vous travaillez sur un document Microsoft Word, par exemple, vous avez peut-être remarqué que quand vous maintenez enfoncée la touche <kbd>Maj</kbd> et que vous tapez un <kbd>"</kbd> Microsoft Word remplace rapidement le caractère `"` par un caractère guillemet courbe équivalent `“`.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-108">When working on a Microsoft Word document for example, you may have noticed that when you hold the <kbd>Shift</kbd> and type a <kbd>"</kbd> Microsoft Word quickly replaces the `"` character with a smart quote equivalent `“` character.</span></span>

| <span data-ttu-id="7c5f0-109">Description</span><span class="sxs-lookup"><span data-stu-id="7c5f0-109">Description</span></span>        | <span data-ttu-id="7c5f0-110">Unicode</span><span class="sxs-lookup"><span data-stu-id="7c5f0-110">Unicode</span></span>  | <span data-ttu-id="7c5f0-111">Guillemet courbe</span><span class="sxs-lookup"><span data-stu-id="7c5f0-111">Smart Quote</span></span> | <span data-ttu-id="7c5f0-112">Remplacement</span><span class="sxs-lookup"><span data-stu-id="7c5f0-112">Replacement</span></span> |
|--------------------|----------|-------------|-------------|
| <span data-ttu-id="7c5f0-113">Guillemet double gauche</span><span class="sxs-lookup"><span data-stu-id="7c5f0-113">Double left quote</span></span>  | `\u201c` | `“`         | `"`         |
| <span data-ttu-id="7c5f0-114">Guillemet double droit</span><span class="sxs-lookup"><span data-stu-id="7c5f0-114">Double right quote</span></span> | `\u201d` | `”`         | `"`         |
| <span data-ttu-id="7c5f0-115">Guillemet simple gauche</span><span class="sxs-lookup"><span data-stu-id="7c5f0-115">Single left quote</span></span>  | `\u2018` | `‘`         | `'`         |
| <span data-ttu-id="7c5f0-116">Guillemet simple droit</span><span class="sxs-lookup"><span data-stu-id="7c5f0-116">Single right quote</span></span> | `\u2019` | `’`         | `'`         |

<span data-ttu-id="7c5f0-117">Dans un fichier Markdown ( *\*.md*), quand vous collez du texte ou que vous mettez à jour du contenu, cette fonctionnalité évalue activement le contenu et remplace automatiquement les valeurs en conséquence.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-117">In a Markdown (*\*.md*) file, when you paste in text or as you update content - this feature will actively evaluate the content and automatically replace values accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="7c5f0-118">La fonctionnalité de remplacement des guillemets courbes remplace également d’autres caractères, tels que les caractères `©, ™, ®, •`, d’indice et d’exposant, entre autres.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-118">The smart quote replacement feature also replaces other characters, such as but not limited to; (`©, ™, ®, •`, subscript and superscript characters).</span></span> <span data-ttu-id="7c5f0-119">C’est utile lors du collage de texte à partir de documents Word.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-119">This is useful when pasting text from Word documents.</span></span>

## <a name="preferences"></a><span data-ttu-id="7c5f0-120">Préférences</span><span class="sxs-lookup"><span data-stu-id="7c5f0-120">Preferences</span></span>

<span data-ttu-id="7c5f0-121">Cette fonctionnalité est facultative, mais prend par défaut la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-121">This feature is optional, but defaults to `true`.</span></span> <span data-ttu-id="7c5f0-122">Pour activer ou désactiver cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="7c5f0-122">To toggle this feature on or off:</span></span>

1. <span data-ttu-id="7c5f0-123">Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).</span><span class="sxs-lookup"><span data-stu-id="7c5f0-123">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="7c5f0-124">Activez/désactivez le paramètre dans la section **Markdown : Replace Smart Quotes** (Markdown : Remplacer les guillemets courbes).</span><span class="sxs-lookup"><span data-stu-id="7c5f0-124">Toggle the setting in the **Markdown: Replace Smart Quotes** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="7c5f0-125">En action</span><span class="sxs-lookup"><span data-stu-id="7c5f0-125">In action</span></span>

<span data-ttu-id="7c5f0-126">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="7c5f0-126">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="7c5f0-127">[![Démonstration de remplacement des guillemets courbes](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="7c5f0-127">[![Replace smart quotes demo](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)</span></span>
