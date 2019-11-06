---
title: validation-timeout
description: Explication et résolution du problème Docs Build validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166758"
---
# <a name="validation-timeout"></a><span data-ttu-id="a2f21-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="a2f21-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="a2f21-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="a2f21-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

<span data-ttu-id="a2f21-105">Parfois, des problèmes temporaires affectant le service de validation, par exemple un serveur dans un état incorrect, empêchent Docs Build d’appeler correctement le service.</span><span class="sxs-lookup"><span data-stu-id="a2f21-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="a2f21-106">Après plusieurs tentatives, l’appel expire et la validation est annulée pour éviter des retards de build et l’encombrement du pipeline de build.</span><span class="sxs-lookup"><span data-stu-id="a2f21-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="a2f21-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="a2f21-107">Resolution</span></span>

<span data-ttu-id="a2f21-108">Essayez de fermer et de rouvrir votre PR ou de forcer une build complète via le [portail Docs](https://ops.microsoft.com/#/).</span><span class="sxs-lookup"><span data-stu-id="a2f21-108">Try closing and re-opening your PR, or forcing a full build via [Docs Portal](https://ops.microsoft.com/#/).</span></span> <span data-ttu-id="a2f21-109">Souvent, les problèmes de service disparaissent d’eux-mêmes après la tentative initiale.</span><span class="sxs-lookup"><span data-stu-id="a2f21-109">Often service issues clear themselves up after the initial retry.</span></span>

<span data-ttu-id="a2f21-110">Notez que vous devez être administrateur de référentiel pour forcer une build via le portail Docs.</span><span class="sxs-lookup"><span data-stu-id="a2f21-110">Note that you must be a repo admin to force a build via Docs Portal.</span></span> <span data-ttu-id="a2f21-111">Si vous ne savez pas qui est votre administrateur de référentiel ou si vous continuez à recevoir ce message après une build forcée, signalez le problème via [https://SiteHelp](https://SiteHelp) si vous êtes un employé Microsoft, ou @ citez l’auteur d’un article dans votre PR pour obtenir une assistance si vous êtes un contributeur externe.</span><span class="sxs-lookup"><span data-stu-id="a2f21-111">If you don't know who your repo admin is, or if you continue to get this message after a forced build, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<span data-ttu-id="a2f21-112">Si vous êtes administrateur de référentiel, vous pouvez forcer une build complète comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2f21-112">If you're a repo admin, you can force a full build as follows:</span></span>

1. <span data-ttu-id="a2f21-113">Accédez au [portail Docs](https://ops.microsoft.com/#/) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="a2f21-113">Go to [Docs Portal](https://ops.microsoft.com/#/) and sign in.</span></span>
1. <span data-ttu-id="a2f21-114">Recherchez votre référentiel en effectuant une recherche en haut à gauche, puis sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="a2f21-114">Find your repo by searching in the upper left corner, and select it.</span></span>

   <span data-ttu-id="a2f21-115">:::image type="content" source="media/find-repo.png" alt-text="Rechercher votre référentiel via la zone de recherche du portail Docs":::</span><span class="sxs-lookup"><span data-stu-id="a2f21-115">:::image type="content" source="media/find-repo.png" alt-text="find your repo via the Docs Portal search box":::</span></span>
1. <span data-ttu-id="a2f21-116">Sous l’onglet **Historique de build**, cliquez sur **+ Publication manuelle**.</span><span class="sxs-lookup"><span data-stu-id="a2f21-116">On the **Build History** tab, click **+ Manual Publish**.</span></span>
1. <span data-ttu-id="a2f21-117">Sélectionnez la branche qui reçoit l’avertissement, par exemple Master.</span><span class="sxs-lookup"><span data-stu-id="a2f21-117">Select the branch that's getting the Warning, such as Master.</span></span>
1. <span data-ttu-id="a2f21-118">Pour la cible, conservez la valeur par défaut **Docs site**.</span><span class="sxs-lookup"><span data-stu-id="a2f21-118">For target, keep the default, **Docs site**.</span></span>
1. <span data-ttu-id="a2f21-119">Cochez la case **Forcer la publication**.</span><span class="sxs-lookup"><span data-stu-id="a2f21-119">Check the **Force Publish** checkbox.</span></span>
1. <span data-ttu-id="a2f21-120">Cliquez sur **Publier**.</span><span class="sxs-lookup"><span data-stu-id="a2f21-120">Click **Publish**.</span></span>

   <span data-ttu-id="a2f21-121">:::image type="content" source="media/force-build.png" alt-text="étapes pour forcer une build complète":::</span><span class="sxs-lookup"><span data-stu-id="a2f21-121">:::image type="content" source="media/force-build.png" alt-text="steps to force a full build":::</span></span>

<span data-ttu-id="a2f21-122">Cela force une build complète sur la branche.</span><span class="sxs-lookup"><span data-stu-id="a2f21-122">This will force a full build on the branch.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
