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
# <a name="labels-and-projects-roadmap"></a>Feuille de route concernant les étiquettes et les projets

Dans l’équipe de documentation .NET, nous faisons largement appel aux [étiquettes GitHub](https://github.com/dotnet/docs/labels) pour organiser notre travail. En filtrant sur des combinaisons d’étiquettes, nous pouvons rapidement nous concentrer sur les sections du [site web Documentation .NET](https://docs.microsoft.com/dotnet) qui nous intéressent.

Nous utilisons également des projets [GitHub](https://github.com/dotnet/docs/projects) pour organiser des sprints et autres épopées axées sur des objectifs.

Cette feuille de route examine comment nous utilisons ces outils d’organisation et contient des liens vers des filtres pratiques qui nous permettent de rechercher des zones d’intérêt.

## <a name="labels"></a>Étiquettes

Si c’est la première fois que vous contribuez à [dotnet/docs](https://github.com/dotnet/docs), commencez par les problèmes [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs). Ces problèmes ont une étendue plus ciblée. Ils constituent un excellent point de départ pour une première contribution. À partir de la vue up-for-grabs vous pouvez filtrer les problèmes selon leur zone et leur priorité. Les problèmes adaptés aux débutants sont identifiés avec l’étiquette [good-first-issue](https://github.com/dotnet/docs/labels/good-first-issue). Utilisez-la si vous souhaitez commencer par une petite contribution.

Nous utilisons des étiquettes pour classifier les problèmes de plusieurs façons :

- [Guides .NET](#find-a-single-net-guide) et [sections d’un guide](#search-one-section-of-a-guide)
- [Version cible](#releases)
- [Priorité](#priority)

Vous pouvez combiner une étiquette de chaque ensemble (guide, version, priorité) pour limiter votre champ de recherche aux problèmes sur lesquels vous souhaitez travailler.

### <a name="find-a-single-net-guide"></a>Trouver un guide .NET unique

Nous utilisons des étiquettes pour chacun des livres électroniques d’architecture et chaque guide .NET.

![:book: guide avec un arrière-plan vert clair](./media/labels-projects/guide.png "Préfixe des étiquettes de guide d’architecture")

Les livres électroniques d’architecture sont signalés par le préfixe `:book: guide` et ont un arrière-plan vert clair. Il s’agit des zones de forme longue qui couvrent l’architecture recommandée. Voici les problèmes actuels filtrés selon les guides d’architecture .NET.

- [ASP.NET Core web apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20ASP.NET%20Core%20web%20apps) (Applications web ASP.NET Core)
- [Blazor](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Blazor)
- [Cloud Native](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Cloud%20Native) (Natif cloud)
- [Docker lifecycle](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Docker%20lifecycle) (Cycle de vie Docker)
- [gRPC](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20gRPC)
- [Modernizing w/ Windows containers](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Modernizing%20w%2F%20Windows%20containers)
- [.NET Microservices](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20.NET%20Microservices)
- [Serverless apps](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Serverless%20apps)

Ce style d’étiquette est également appliqué à [Framework Design Guidelines](https://github.com/dotnet/docs/labels/%3Abook%3A%20guide%20-%20Framework%20Design%20Guidelines). Cette zone a la même conception d’étiquette, mais les demandes de tirage (pull request) de la communauté sont déconseillées. Ce contenu est réimprimé avec autorisation et ne doit pas être modifié.

![:books: Area avec un arrière-plan bleu foncé](./media/labels-projects/area.png "Préfixe des étiquettes de la zone .NET Guide")

Chaque guide .NET est signalé par le préfixe `:books: Area` et a un arrière-plan bleu foncé. Voici les problèmes actuels filtrés selon les guides .NET.

- [API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20API%20Reference)
- [Kit de développement logiciel (SDK) .NET Azure](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Azure%20.NET%20SDk)
- [C# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20C%23%20Guide)
- [Desktop Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Desktop%20Guide)
- [F# Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20F%23%20Guide)
- [ML.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20ML.NET%20Guide)
- [.NET Architecture Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Architecture%20Guide) - Peut être supprimé
- [.NET Core Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Core%20Guide)
- [.NET for Apache Spark Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20for%20Apache%20Spark%20Guide)
- [.NET Framework Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Framework%20Guide)
- [.NET Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20.NET%20Guide)
- [Roslyn API Reference](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Roslyn%20API%20Reference) - Peut être supprimé
- [Visual Basic Guide](https://github.com/dotnet/docs/labels/%3Abooks%3A%20Area%20-%20Visual%20Basic%20Guide)

#### <a name="search-one-section-of-a-guide"></a>Rechercher dans une section d’un guide

![:card_file_box: Technology avec un arrière-plan bleu ciel](./media/labels-projects/technology.png "Préfixe des étiquettes de la sous-zone .NET Guide")

Les guides .NET étant volumineux, ces étiquettes permettent de limiter l’étendue à une section d’un guide. Chaque sous-zone d’un guide .NET est signalée par le préfixe `:card_file_box: Technology` et a un arrière-plan bleu ciel. Bon nombre d’étiquettes s’appliquent à plusieurs guides, mais certaines ne figurent que dans un seul guide. Après avoir sélectionné une zone à l’aide d’un filtre, ajoutez l’une de ces étiquettes pour limiter encore plus l’étendue des problèmes.

- AppCompat
- Async Task (Tâche asynchrone)
- C# Advanced concepts (Concepts avancés en C#)
- C# compiler (Compilateur C#)
- C# Fundamentals (Notions de base de C#)
- C# Get Started (Bien démarrer avec C#)
- C# Language Reference (Référence du langage C#)
- C# Null safety (Sécurité contre les valeurs Null dans C#)
- C# What’s new (Nouveautés de C#)
- CLI
- Data Access (Accès aux données)
- Docker
- Installers (Programmes d’installation)
- LINQ
- NCL
- .NET Standard
- Roslyn APIs
- Sécurité
- WCF
- WF
- WIF
- WinForms
- WPF

### <a name="releases"></a>Versions

![:checkered_flag: Release: avec un arrière-plan jaune foncé](./media/labels-projects/release.png "Préfixe des étiquettes de version")

Les problèmes marqués pour une version spécifique sont signalés par le préfixe `:checkered_flag: Release:` et ont un arrière-plan jaune foncé.

- .NET Core 2.2
- .NET Core 3.0
- .NET Framework 4.8
- .NET 5

### <a name="priority"></a>Priorité

Les étiquettes de priorité commencent par la lettre `P` et se terminent par un chiffre. Plus le nombre est petit, plus la priorité est élevée :

- P0
- P1
- P2
- P3

### <a name="what-about-the-other-labels"></a>Qu’en est-il des autres étiquettes ?

Les équipes de contenu utilisent bien d’autres étiquettes pour gérer différentes classifications de problèmes. Si vous n’êtes pas membre de l’équipe de contenu, vous pouvez ignorer ces autres étiquettes.

## <a name="projects"></a>Projets

Nous utilisons des projets de deux manières :

- Types de projets Mois AAAA : Il s’agit de tableaux scrum pour le plan de travail de chaque mois.
- Épopées de longue durée : Nous les utilisons pour organiser les tâches en fonction d’un objectif donné quand le travail s’étale sur plusieurs mois.
