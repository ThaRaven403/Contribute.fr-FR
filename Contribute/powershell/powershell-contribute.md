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
# <a name="contributing-to-powershell-documentation"></a>Contribution à la documentation PowerShell

Merci de l’intérêt que vous portez à la documentation PowerShell.

Ce document explique comment contribuer aux articles et aux exemples de code hébergés sur le site de la documentation PowerShell. Les contributions peuvent être aussi bien basiques (simples corrections de faute de frappe) que complexes (rédaction de nouveaux articles).

Le site de la documentation PowerShell est construit à partir de plusieurs dépôts contenant un ou plusieurs docsets :

- [Informations de référence sur les concepts et les applets de commande de PowerShell][psdocs]
- Exemples de code du SDK PowerShell : dépôt privé contenant les exemples utilisés dans les articles sur le SDK
- [Informations de référence du SDK .NET PowerShell ](/dotnet/api/?view=pscore-6.2.0) : contenu du dépôt privé généré à partir du code source de PowerShell

Les problèmes liés à l’ensemble de ce contenu sont suivis dans le dépôt [PowerShell-Docs][docsrepo].

## <a name="repository-structure"></a>Structure du dépôt

Le dépôt PowerShell-Docs est constitué de trois docsets qui sont publiés sur [Microsoft Docs][psdocs]. Les docsets sont contenus dans les dossiers suivants :

- [/reference/][ref] : contient les informations de référence sur les applets de commande PowerShell pour les applets de commande fournies avec PowerShell. Les informations de référence sont collectées dans les dossiers des versions (3.0, 4.0, 5.0, 5.1, 6 et 7). Ce docset ne contient pas les informations de référence pour les modules fournis avec Windows ou d’autres produits Microsoft.
- [/reference/docs-conceptual][conceptual] : contient la documentation sur les concepts de PowerShell. Ceci inclut les instructions de configuration, des exemples de scripts, des rubriques de procédures, etc.
- [/developer/][SDK] : contient la documentation sur les concepts du SDK PowerShell.

<!--link refs-->
[psdocs]: https://docs.microsoft.com/powershell
[docsrepo]: https://github.com/MicrosoftDocs/PowerShell-Docs
[ref]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference
[conceptual]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/reference/docs-conceptual
[SDK]: https://github.com/MicrosoftDocs/PowerShell-Docs/tree/staging/developer
