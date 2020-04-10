---
title: Feuille de route concernant les étiquettes et les projets
description: Cet article explique comment les étiquettes et les projets sont utilisés dans le dépôt dotnet/docs.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 03/24/2020
ms.openlocfilehash: 0dcac28db04378730b186c0f23064c1433d9f80e
ms.sourcegitcommit: bf2f4c7d9050b480d4db306df19d4c9f8714eff0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/07/2020
ms.locfileid: "80760373"
---
# <a name="labels-and-projects-roadmap"></a><span data-ttu-id="dd8fd-103">Feuille de route concernant les étiquettes et les projets</span><span class="sxs-lookup"><span data-stu-id="dd8fd-103">Labels and projects roadmap</span></span>

<span data-ttu-id="dd8fd-104">Dans l’équipe de documentation .NET, nous faisons largement appel aux [étiquettes GitHub](https://github.com/dotnet/docs/labels) pour organiser notre travail.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-104">The .NET docs team makes extensive use of [GitHub labels](https://github.com/dotnet/docs/labels) to organize our work.</span></span> <span data-ttu-id="dd8fd-105">En filtrant sur des combinaisons d’étiquettes, nous pouvons rapidement nous concentrer sur les sections du [site web Documentation .NET](https://docs.microsoft.com/dotnet) qui nous intéressent.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-105">By filtering on combinations of labels, we can quickly focus on sections of interest on the [.NET docs website](https://docs.microsoft.com/dotnet).</span></span>

<span data-ttu-id="dd8fd-106">Nous utilisons également des projets [GitHub](https://github.com/dotnet/docs/projects) pour organiser des sprints et autres épopées axées sur des objectifs.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-106">We also use [GitHub projects](https://github.com/dotnet/docs/projects) to organize sprints and other goal-oriented epics.</span></span>

<span data-ttu-id="dd8fd-107">Cette feuille de route examine comment nous utilisons ces outils d’organisation et contient des liens vers des filtres pratiques qui nous permettent de rechercher des zones d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-107">This roadmap explains how we use these organizational tools and has links to handy filters we use to find areas of interest.</span></span>

## <a name="labels"></a><span data-ttu-id="dd8fd-108">Étiquettes</span><span class="sxs-lookup"><span data-stu-id="dd8fd-108">Labels</span></span>

<span data-ttu-id="dd8fd-109">Si c’est la première fois que vous contribuez à [dotnet/docs](https://github.com/dotnet/docs), commencez par les problèmes [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs).</span><span class="sxs-lookup"><span data-stu-id="dd8fd-109">If this is your first experience contributing to [dotnet/docs](https://github.com/dotnet/docs), start with the [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) issues.</span></span> <span data-ttu-id="dd8fd-110">Ces problèmes ont une étendue plus ciblée.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-110">These are issues that have a more focused scope.</span></span> <span data-ttu-id="dd8fd-111">Ils constituent un excellent point de départ pour une première contribution.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-111">They are a great way to make your first contribution.</span></span> <span data-ttu-id="dd8fd-112">À partir de la vue up-for-grabs vous pouvez filtrer les problèmes selon leur zone et leur priorité.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-112">From the up-for-grabs view, you can further filter issues based on areas and priority.</span></span> <span data-ttu-id="dd8fd-113">Les problèmes adaptés aux débutants sont identifiés avec l’étiquette [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue). Utilisez-la si vous souhaitez commencer par une petite contribution.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-113">We've identified good issues for beginners with the [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue) if you want to try a smaller first contribution.</span></span>

<span data-ttu-id="dd8fd-114">Nous utilisons des étiquettes pour classifier les problèmes de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="dd8fd-114">We use labels to classify issues in many different ways:</span></span>

- <span data-ttu-id="dd8fd-115">[Guides .NET](#find-a-single-net-guide) et [sections d’un guide](#search-one-section-of-a-guide)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-115">[.NET Guides](#find-a-single-net-guide) and [sections of a guide](#search-one-section-of-a-guide).</span></span>
- [<span data-ttu-id="dd8fd-116">Version cible</span><span class="sxs-lookup"><span data-stu-id="dd8fd-116">Target release</span></span>](#releases)
- [<span data-ttu-id="dd8fd-117">Priorité</span><span class="sxs-lookup"><span data-stu-id="dd8fd-117">Priority</span></span>](#priority)

<span data-ttu-id="dd8fd-118">Vous pouvez combiner une étiquette de chaque ensemble (guide, version, priorité) pour limiter votre champ de recherche aux problèmes sur lesquels vous souhaitez travailler.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-118">You can combine a label from each set (guide, release, priority) to create a narrow focus to find issues you want to work on.</span></span>

### <a name="find-a-single-net-guide"></a><span data-ttu-id="dd8fd-119">Trouver un guide .NET unique</span><span class="sxs-lookup"><span data-stu-id="dd8fd-119">Find a single .NET guide</span></span>

<span data-ttu-id="dd8fd-120">Nous utilisons des étiquettes pour chacun des livres électroniques d’architecture et chaque guide .NET.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-120">We use labels for each of the architecture e-books and for each .NET Guide.</span></span>

<span data-ttu-id="dd8fd-121">![:book: guide avec un arrière-plan vert clair](./media/labels-projects/guide.png "Préfixe des étiquettes de guide d’architecture")</span><span class="sxs-lookup"><span data-stu-id="dd8fd-121">![:book: guide on light green background](./media/labels-projects/guide.png "Prefix for architecture guide labels")</span></span>

<span data-ttu-id="dd8fd-122">Les livres électroniques d’architecture sont signalés par le préfixe `:book: guide` et ont un arrière-plan vert clair.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-122">Architecture e-books are noted with the `:book: guide` prefix and have a light green background.</span></span> <span data-ttu-id="dd8fd-123">Il s’agit des zones de forme longue qui couvrent l’architecture recommandée.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-123">These are the long-form areas that cover recommended architecture.</span></span> <span data-ttu-id="dd8fd-124">Voici les problèmes actuels filtrés selon les guides d’architecture .NET.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-124">Here are current issues filtered for each of the .NET architecture guides.</span></span>

- <span data-ttu-id="dd8fd-125">[ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps) (Applications web ASP.NET Core)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-125">[ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps)</span></span>
- [<span data-ttu-id="dd8fd-126">Blazor</span><span class="sxs-lookup"><span data-stu-id="dd8fd-126">Blazor</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- <span data-ttu-id="dd8fd-127">[Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native) (Natif cloud)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-127">[Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native)</span></span>
- <span data-ttu-id="dd8fd-128">[Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle) (Cycle de vie Docker)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-128">[Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle)</span></span>
- [<span data-ttu-id="dd8fd-129">gRPC</span><span class="sxs-lookup"><span data-stu-id="dd8fd-129">gRPC</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [<span data-ttu-id="dd8fd-130">Modernizing w/ Windows containers</span><span class="sxs-lookup"><span data-stu-id="dd8fd-130">Modernizing w/ Windows containers</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [<span data-ttu-id="dd8fd-131">.NET Microservices</span><span class="sxs-lookup"><span data-stu-id="dd8fd-131">.NET Microservices</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [<span data-ttu-id="dd8fd-132">Serverless apps</span><span class="sxs-lookup"><span data-stu-id="dd8fd-132">Serverless apps</span></span>](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

<span data-ttu-id="dd8fd-133">Ce style d’étiquette est également appliqué à [Framework Design Guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span><span class="sxs-lookup"><span data-stu-id="dd8fd-133">This label style is also applied to the [Framework design guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines).</span></span> <span data-ttu-id="dd8fd-134">Cette zone a la même conception d’étiquette, mais les demandes de tirage (pull request) de la communauté sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-134">This area has the same label design, but community PRs are discouraged.</span></span> <span data-ttu-id="dd8fd-135">Ce contenu est réimprimé avec autorisation et ne doit pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-135">This is material reprinted with permission and should not be edited.</span></span>

<span data-ttu-id="dd8fd-136">![:books: Area avec un arrière-plan bleu foncé](./media/labels-projects/area.png "Préfixe des étiquettes de la zone .NET Guide")</span><span class="sxs-lookup"><span data-stu-id="dd8fd-136">![:books: Area on dark blue background](./media/labels-projects/area.png "Prefix for .NET Guide area labels")</span></span>

<span data-ttu-id="dd8fd-137">Chaque guide .NET est signalé par le préfixe `:books: Area` et a un arrière-plan bleu foncé.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-137">Each .NET Guide is noted with the `:books: Area` prefix and has a dark blue background.</span></span> <span data-ttu-id="dd8fd-138">Voici les problèmes actuels filtrés selon les guides .NET.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-138">Here are current issues filtered for each of the .NET guides.</span></span>

- [<span data-ttu-id="dd8fd-139">API Reference</span><span class="sxs-lookup"><span data-stu-id="dd8fd-139">API Reference</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [<span data-ttu-id="dd8fd-140">Kit de développement logiciel (SDK) .NET Azure</span><span class="sxs-lookup"><span data-stu-id="dd8fd-140">Azure .NET SDK</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [<span data-ttu-id="dd8fd-141">C# Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-141">C# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [<span data-ttu-id="dd8fd-142">Desktop Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-142">Desktop Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [<span data-ttu-id="dd8fd-143">F# Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-143">F# Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [<span data-ttu-id="dd8fd-144">ML.NET Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-144">ML.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- <span data-ttu-id="dd8fd-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Peut être supprimé</span><span class="sxs-lookup"><span data-stu-id="dd8fd-145">[.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Could be removed</span></span>
- [<span data-ttu-id="dd8fd-146">.NET Core Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-146">.NET Core Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [<span data-ttu-id="dd8fd-147">.NET for Apache Spark Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-147">.NET for Apache Spark Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [<span data-ttu-id="dd8fd-148">.NET Framework Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-148">.NET Framework Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [<span data-ttu-id="dd8fd-149">.NET Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-149">.NET Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- <span data-ttu-id="dd8fd-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - Peut être supprimé</span><span class="sxs-lookup"><span data-stu-id="dd8fd-150">[Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - could be removed.</span></span>
- [<span data-ttu-id="dd8fd-151">Visual Basic Guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-151">Visual Basic Guide</span></span>](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a><span data-ttu-id="dd8fd-152">Rechercher dans une section d’un guide</span><span class="sxs-lookup"><span data-stu-id="dd8fd-152">Search one section of a guide</span></span>

<span data-ttu-id="dd8fd-153">![:card_file_box: Technology avec un arrière-plan bleu ciel](./media/labels-projects/technology.png "Préfixe des étiquettes de la sous-zone .NET Guide")</span><span class="sxs-lookup"><span data-stu-id="dd8fd-153">![:card_file_box: Area on medium blue background](./media/labels-projects/technology.png "Prefix for .NET Guide sub-area labels")</span></span>

<span data-ttu-id="dd8fd-154">Les guides .NET étant volumineux, ces étiquettes permettent de limiter l’étendue à une section d’un guide.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-154">The .NET guides are large, so these labels further limit the scope by a section of a guide.</span></span> <span data-ttu-id="dd8fd-155">Chaque sous-zone d’un guide .NET est signalée par le préfixe `:card_file_box: Technology` et a un arrière-plan bleu ciel.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-155">Each .NET Guide subarea is noted with the `:card_file_box: Technology` prefix and has a medium blue background.</span></span> <span data-ttu-id="dd8fd-156">Bon nombre d’étiquettes s’appliquent à plusieurs guides, mais certaines ne figurent que dans un seul guide.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-156">Many of these labels apply to multiple guides, while others are in only one guide.</span></span> <span data-ttu-id="dd8fd-157">Après avoir sélectionné une zone à l’aide d’un filtre, ajoutez l’une de ces étiquettes pour limiter encore plus l’étendue des problèmes.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-157">After filtering on an area, add one of these labels to further limit the scope of issues.</span></span>

- <span data-ttu-id="dd8fd-158">AppCompat</span><span class="sxs-lookup"><span data-stu-id="dd8fd-158">AppCompat</span></span>
- <span data-ttu-id="dd8fd-159">Async Task (Tâche asynchrone)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-159">Async Task</span></span>
- <span data-ttu-id="dd8fd-160">C# Advanced concepts (Concepts avancés en C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-160">C# Advanced concepts</span></span>
- <span data-ttu-id="dd8fd-161">C# compiler (Compilateur C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-161">C# compiler</span></span>
- <span data-ttu-id="dd8fd-162">C# Fundamentals (Notions de base de C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-162">C# Fundamentals</span></span>
- <span data-ttu-id="dd8fd-163">C# Get Started (Bien démarrer avec C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-163">C# Get Started</span></span>
- <span data-ttu-id="dd8fd-164">C# Language Reference (Référence du langage C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-164">C# Language Reference</span></span>
- <span data-ttu-id="dd8fd-165">C# Null safety (Sécurité contre les valeurs Null dans C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-165">C# Null safety</span></span>
- <span data-ttu-id="dd8fd-166">C# What’s new (Nouveautés de C#)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-166">C# What's new</span></span>
- <span data-ttu-id="dd8fd-167">CLI</span><span class="sxs-lookup"><span data-stu-id="dd8fd-167">CLI</span></span>
- <span data-ttu-id="dd8fd-168">Data Access (Accès aux données)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-168">Data Access</span></span>
- <span data-ttu-id="dd8fd-169">Docker</span><span class="sxs-lookup"><span data-stu-id="dd8fd-169">Docker</span></span>
- <span data-ttu-id="dd8fd-170">Installers (Programmes d’installation)</span><span class="sxs-lookup"><span data-stu-id="dd8fd-170">Installers</span></span>
- <span data-ttu-id="dd8fd-171">LINQ</span><span class="sxs-lookup"><span data-stu-id="dd8fd-171">LINQ</span></span>
- <span data-ttu-id="dd8fd-172">NCL</span><span class="sxs-lookup"><span data-stu-id="dd8fd-172">NCL</span></span>
- <span data-ttu-id="dd8fd-173">.NET Standard</span><span class="sxs-lookup"><span data-stu-id="dd8fd-173">.NET Standard</span></span>
- <span data-ttu-id="dd8fd-174">Roslyn APIs</span><span class="sxs-lookup"><span data-stu-id="dd8fd-174">Roslyn APIs</span></span>
- <span data-ttu-id="dd8fd-175">Sécurité</span><span class="sxs-lookup"><span data-stu-id="dd8fd-175">Security</span></span>
- <span data-ttu-id="dd8fd-176">WCF</span><span class="sxs-lookup"><span data-stu-id="dd8fd-176">WCF</span></span>
- <span data-ttu-id="dd8fd-177">WF</span><span class="sxs-lookup"><span data-stu-id="dd8fd-177">WF</span></span>
- <span data-ttu-id="dd8fd-178">WIF</span><span class="sxs-lookup"><span data-stu-id="dd8fd-178">WIF</span></span>
- <span data-ttu-id="dd8fd-179">WinForms</span><span class="sxs-lookup"><span data-stu-id="dd8fd-179">WinForms</span></span>
- <span data-ttu-id="dd8fd-180">WPF</span><span class="sxs-lookup"><span data-stu-id="dd8fd-180">WPF</span></span>

### <a name="releases"></a><span data-ttu-id="dd8fd-181">Versions</span><span class="sxs-lookup"><span data-stu-id="dd8fd-181">Releases</span></span>

<span data-ttu-id="dd8fd-182">![:checkered_flag: Release: avec un arrière-plan jaune foncé](./media/labels-projects/release.png "Préfixe des étiquettes de version")</span><span class="sxs-lookup"><span data-stu-id="dd8fd-182">![:checkered_flag: Release: on dark yellow](./media/labels-projects/release.png "Prefix for release labels")</span></span>

<span data-ttu-id="dd8fd-183">Les problèmes marqués pour une version spécifique sont signalés par le préfixe `:checkered_flag: Release:` et ont un arrière-plan jaune foncé.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-183">Issues tagged for a specific release are noted with the `:checkered_flag: Release:` prefix and have a dark yellow background.</span></span>

- <span data-ttu-id="dd8fd-184">.NET Core 2.2</span><span class="sxs-lookup"><span data-stu-id="dd8fd-184">.NET Core 2.2</span></span>
- <span data-ttu-id="dd8fd-185">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="dd8fd-185">.NET Core 3.0</span></span>
- <span data-ttu-id="dd8fd-186">.NET Framework 4.8</span><span class="sxs-lookup"><span data-stu-id="dd8fd-186">.NET Framework 4.8</span></span>
- <span data-ttu-id="dd8fd-187">.NET 5</span><span class="sxs-lookup"><span data-stu-id="dd8fd-187">.NET 5</span></span>

### <a name="priority"></a><span data-ttu-id="dd8fd-188">Priorité</span><span class="sxs-lookup"><span data-stu-id="dd8fd-188">Priority</span></span>

<span data-ttu-id="dd8fd-189">Les étiquettes de priorité commencent par la lettre `P` et se terminent par un chiffre.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-189">Priority labels are all `P` followed by a single digit.</span></span> <span data-ttu-id="dd8fd-190">Plus le nombre est petit, plus la priorité est élevée :</span><span class="sxs-lookup"><span data-stu-id="dd8fd-190">Lower numbers are higher priority:</span></span>

- <span data-ttu-id="dd8fd-191">P0</span><span class="sxs-lookup"><span data-stu-id="dd8fd-191">P0</span></span>
- <span data-ttu-id="dd8fd-192">P1</span><span class="sxs-lookup"><span data-stu-id="dd8fd-192">P1</span></span>
- <span data-ttu-id="dd8fd-193">P2</span><span class="sxs-lookup"><span data-stu-id="dd8fd-193">P2</span></span>
- <span data-ttu-id="dd8fd-194">P3</span><span class="sxs-lookup"><span data-stu-id="dd8fd-194">P3</span></span>

### <a name="what-about-the-other-labels"></a><span data-ttu-id="dd8fd-195">Qu’en est-il des autres étiquettes ?</span><span class="sxs-lookup"><span data-stu-id="dd8fd-195">What about the other labels?</span></span>

<span data-ttu-id="dd8fd-196">Les équipes de contenu utilisent bien d’autres étiquettes pour gérer différentes classifications de problèmes.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-196">There are many other labels used by the content teams to manage different classifications of issues.</span></span> <span data-ttu-id="dd8fd-197">Si vous n’êtes pas membre de l’équipe de contenu, vous pouvez ignorer ces autres étiquettes.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-197">If you're not on the content team, you can ignore these other labels.</span></span>

## <a name="projects"></a><span data-ttu-id="dd8fd-198">Projets</span><span class="sxs-lookup"><span data-stu-id="dd8fd-198">Projects</span></span>

<span data-ttu-id="dd8fd-199">Nous utilisons des projets de deux manières :</span><span class="sxs-lookup"><span data-stu-id="dd8fd-199">We use projects in two ways:</span></span>

- <span data-ttu-id="dd8fd-200">Types de projets Mois AAAA : Il s’agit de tableaux scrum pour le plan de travail de chaque mois.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-200">Month YYYY project types: These are scrum boards for each month's working plan.</span></span>
- <span data-ttu-id="dd8fd-201">Épopées de longue durée : Nous les utilisons pour organiser les tâches en fonction d’un objectif donné quand le travail s’étale sur plusieurs mois.</span><span class="sxs-lookup"><span data-stu-id="dd8fd-201">Long-running epics: These are used to organize tasks toward a goal when the work will occur over several months.</span></span>
