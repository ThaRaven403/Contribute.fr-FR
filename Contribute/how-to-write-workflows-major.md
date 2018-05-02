---
title: Flux de travail de contribution à GitHub pour les changements majeurs ou à long terme
description: Cet article vous montre comment utiliser le flux de travail de contributeur « majeur » pour contribuer aux articles de docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 08/30/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: e26b62923eed22d5b2005b1d84dc4ae240d262b1
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2018
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Flux de travail de contribution à GitHub pour les changements majeurs ou à long terme

> [!IMPORTANT]
> Tous les dépôts qui publient sur docs.microsoft.com ont adopté soit le [Code de conduite open source de Microsoft](https://opensource.microsoft.com/codeofconduct/), soit le [Code de conduite de .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Pour plus d’informations, consultez les [questions fréquentes (FAQ) sur le code de conduite](https://opensource.microsoft.com/codeofconduct/faq/). Vous pouvez aussi envoyer vos questions ou vos commentaires à [opencode@microsoft.com](mailto:opencode@microsoft.com) ou à [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Les corrections mineures ou les clarifications pour la documentation, ainsi que les exemples de code dans les dépôts publics, sont couverts par les [Conditions d’utilisation du site web docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Les nouveautés ou modifications significatives génèrent un commentaire dans la demande de tirage qui vous invite à signer un contrat de licence de contribution en ligne si vous n’êtes pas un employé de Microsoft. Vous devrez remplir le formulaire en ligne pour que nous puissions accepter votre demande de tirage (pull request).

## <a name="overview"></a>Vue d'ensemble

Ce flux de travail convient pour un contributeur qui a besoin de faire un changement majeur ou qui sera un contributeur fréquent d’un dépôt. Les contributeurs fréquents ont généralement des changements continus (à long terme) qui peuvent passer par plusieurs cycles de création/validation/préproduction ou être répartis sur plusieurs jours avant la validation et la fusion de la demande de tirage.

Voici des exemples de ce type de contribution :

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Avant de commencer, passons en revue quelques-uns des termes et monikers de Git/GitHub utilisés dans ce flux de travail. Vous n'avez pas à les comprendre dès maintenant. Sachez juste que vous allez les étudier et que vous pouvez revenir à cette section quand vous souhaitez vérifier une définition.

| Nom | Description |
|-----------|-------------|
|duplication (fork)|Normalement utilisé comme nom lorsqu'il est fait référence à une copie d'un dépôt GitHub principal. En pratique, une duplication (fork) est simplement un autre dépôt. Mais il est particulier en cela que GitHub conserve une connexion avec le dépôt principal/parent. Ce terme est parfois utilisé sous forme verbale, par exemple « Vous devez d’abord dupliquer le dépôt ».|
|remote|Une connexion nommée à un dépôt distant, comme les remotes « origin » et « upstream ». Git les appelle « remotes », car elles servent à référencer un dépôt hébergé sur un autre ordinateur. Dans ce flux de travail, une connexion remote concerne toujours un dépôt GitHub.|
|origin|Nom affecté à la connexion entre votre dépôt local et le dépôt à partir duquel il a été cloné. Dans ce flux de travail, origin représente la connexion à votre duplication. Il s’agit parfois du moniker pour le dépôt d’origine lui-même, par exemple dans la phrase « N’oubliez pas d’envoyer vos modifications sur origin ».|
|upstream|Comme pour la connexion remote origin, upstream est le nom d'une connexion vers un autre dépôt. Dans ce flux de travail, upstream représente la connexion entre votre dépôt local et le dépôt principal, à partir duquel votre duplication a été créé. Il s’agit parfois du moniker pour le dépôt ascendant lui-même, par exemple dans la phrase « N’oubliez pas d’extraire les modifications de l’amont ».|

## <a name="workflow"></a>Flux de travail

>[!IMPORTANT]
> Si vous ne l’avez pas déjà fait, vous devez effectuer les étapes de la section [Configuration](get-started-setup-github.md). Cette section vous guide lors de la configuration de votre compte GitHub, l’installation de Git Bash et d’un éditeur Markdown, la création d’une duplication et la configuration de votre dépôt local. Si vous découvrez les concepts de Git et GitHub, comme les dépôts ou les branches, consultez d’abord les [Bases de Git et GitHub](git-github-fundamentals.md).

Dans ce flux de travail, les changements circulent dans un cycle répétitif. En partant du dépôt local de votre appareil, ils passent par votre branche GitHub, dans le dépôt GitHub principal, puis reviennent localement lorsque vous intégrez les modifications d'autres contributeurs.

### <a name="use-github-flow"></a>Utiliser le flux GitHub

Rappelez-vous, comme indiqué dans les [Bases de Git et GitHub](git-github-fundamentals.md#git), qu’un dépôt Git contient une branche principale et des branches supplémentaires en cours de modification qui n’ont pas été intégrées à la branche principale. Quand vous introduisez une série de changements liés logiquement, une bonne pratique consiste à créer une *branche de travail* pour gérer vos modifications via le flux de travail. Nous l’appelons ici branche de travail, car il s’agit d’un espace de travail pour itérer/affiner les modifications, jusqu’à ce qu’elles puissent être réintégrées à la branche principale.

Isoler les changements liés dans une branche spécifique vous permet de contrôler et d'introduire ces changements de façon indépendante, en les ciblant pour une date de publication particulière dans le cycle de publication. En réalité, en fonction du type de travail que vous faites, vous pouvez facilement vous retrouver avec plusieurs branches de travail dans votre dépôt. Il n’est pas rare de travailler sur plusieurs branches en même temps, chacune représentant un projet différent.

>[!TIP]
>L’insertion de modifications dans la branche principale n’est *pas* une bonne pratique. Supposons que vous utilisez la branche principale pour introduire une série de changements pour une publication de fonctionnalité planifiée. Vous terminez les modifications et attendez de les publier. Entre-temps, vous recevez une demande urgente de correction. Vous apportez donc la modification à un fichier dans la branche principale et publiez la modification. Dans cet exemple, vous publiez par erreur à la fois le correctif *et* les modifications que vous attendiez de publier à une date précise.

Créons maintenant une nouvelle branche de travail dans votre dépôt local pour capturer les modifications que vous proposez. Chaque client Git est différent : consultez l’aide du client choisi. Vous trouverez une vue d’ensemble du processus dans le Guide de GitHub sur [Flux GitHub](https://guides.github.com/introduction/flow/).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Étapes suivantes

Et voilà ! Vous avez apporté une contribution au contenu de docs.microsoft.com !

- Pour en savoir plus sur des rubriques comme Markdown et la syntaxe des extensions Markdown, passez à la section « Bases de l’écriture ».
