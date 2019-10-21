---
title: Contribuer aux dépôts de documentation PowerShell
description: Cet article traite des dépôts qui composent la documentation PowerShell.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 6b975c085aa42846be9951a77d3fdebbd5fb17a1
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290170"
---
# <a name="contributing-to-powershell-documentation"></a><span data-ttu-id="58e51-103">Contribution à la documentation PowerShell</span><span class="sxs-lookup"><span data-stu-id="58e51-103">Contributing to PowerShell Documentation</span></span>

<span data-ttu-id="58e51-104">Merci de l’intérêt que vous portez à la documentation PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58e51-104">Thank you for your interest in PowerShell documentation!</span></span>

<span data-ttu-id="58e51-105">Ce document explique comment contribuer aux articles et aux exemples de code hébergés sur le site de la documentation PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58e51-105">This document covers the process for contributing to the articles and code samples that are hosted on the PowerShell documentation site.</span></span> <span data-ttu-id="58e51-106">Les contributions peuvent être aussi bien basiques (simples corrections de faute de frappe) que complexes (rédaction de nouveaux articles).</span><span class="sxs-lookup"><span data-stu-id="58e51-106">Contributions may be as simple as typo corrections or as complex as new articles.</span></span>

<span data-ttu-id="58e51-107">Le site de la documentation PowerShell est construit à partir de plusieurs dépôts contenant un ou plusieurs docsets :</span><span class="sxs-lookup"><span data-stu-id="58e51-107">The PowerShell documentation site is built from multiple repositories containing one or more docsets:</span></span>

- <span data-ttu-id="58e51-108">[Informations de référence sur les concepts et les applets de commande de PowerShell][psdocs]</span><span class="sxs-lookup"><span data-stu-id="58e51-108">[PowerShell concepts & cmdlet reference][psdocs]</span></span>
- <span data-ttu-id="58e51-109">Exemples de code du SDK PowerShell : dépôt privé contenant les exemples utilisés dans les articles sur le SDK</span><span class="sxs-lookup"><span data-stu-id="58e51-109">PowerShell SDK code samples - private repository containing the samples used in the SDK articles</span></span>
- <span data-ttu-id="58e51-110">[Informations de référence du SDK .NET PowerShell ](/dotnet/api/?view=pscore-6.2.0) : contenu du dépôt privé généré à partir du code source de PowerShell</span><span class="sxs-lookup"><span data-stu-id="58e51-110">[PowerShell .NET SDK reference](/dotnet/api/?view=pscore-6.2.0) - private repository contents generated from PowerShell source code</span></span>

<span data-ttu-id="58e51-111">Les problèmes liés à l’ensemble de ce contenu sont suivis dans le dépôt [PowerShell-Docs][docsrepo].</span><span class="sxs-lookup"><span data-stu-id="58e51-111">Issues for all this content are tracked in the [PowerShell-Docs][docsrepo] repository.</span></span>

## <a name="repository-structure"></a><span data-ttu-id="58e51-112">Structure du dépôt</span><span class="sxs-lookup"><span data-stu-id="58e51-112">Repository Structure</span></span>

<span data-ttu-id="58e51-113">Le dépôt PowerShell-Docs est constitué de trois docsets qui sont publiés sur [Microsoft Docs][psdocs]. Les docsets sont contenus dans les dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="58e51-113">The PowerShell-Docs repository consists of three docsets that are published to [Microsoft Docs][psdocs]. The docsets are contained in the following folders:</span></span>

- <span data-ttu-id="58e51-114">[/reference/][ref] : contient les informations de référence sur les applets de commande PowerShell pour les applets de commande fournies avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58e51-114">[/reference/][ref] - contains the PowerShell cmdlet reference for the cmdlets that ship in PowerShell.</span></span> <span data-ttu-id="58e51-115">Les informations de référence sont collectées dans les dossiers des versions (3.0, 4.0, 5.0, 5.1, 6 et 7).</span><span class="sxs-lookup"><span data-stu-id="58e51-115">The reference is collected in versions folders (3.0, 4.0, 5.0, 5.1, 6, and 7).</span></span> <span data-ttu-id="58e51-116">Ce docset ne contient pas les informations de référence pour les modules fournis avec Windows ou d’autres produits Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58e51-116">This docset does not contain the reference for the modules that ship in Windows or other Microsoft products.</span></span>
- <span data-ttu-id="58e51-117">[/reference/docs-conceptual][conceptual] : contient la documentation sur les concepts de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58e51-117">[/reference/docs-conceptual][conceptual] - contains the PowerShell conceptual documentation.</span></span> <span data-ttu-id="58e51-118">Ceci inclut les instructions de configuration, des exemples de scripts, des rubriques de procédures, etc.</span><span class="sxs-lookup"><span data-stu-id="58e51-118">This include setup instructions, sample scripts, how-to topics, and more.</span></span>
- <span data-ttu-id="58e51-119">[/developer/][SDK] : contient la documentation sur les concepts du SDK PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58e51-119">[/developer/][SDK] - contains the PowerShell SDK conceptual documentation.</span></span>

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
