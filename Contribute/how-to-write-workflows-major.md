---
title: Flux de travail de contribution à GitHub pour les changements majeurs ou à long terme
description: Cet article vous montre comment utiliser le flux de travail de contributeur « majeur » pour contribuer aux articles de docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 08/30/2017
ms.openlocfilehash: 5231b68f04caa94d3ff2ff26afc38e3218ca06b8
ms.sourcegitcommit: 804a99b89785e5c8f056a9da3f0fbde9f0a56a51
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78331903"
---
# <a name="github-contribution-workflow-for-major-or-long-running-changes"></a>Flux de travail de contribution à GitHub pour les changements majeurs ou à long terme

> [!IMPORTANT]
> Tous les référentiels qui publient sur docs.microsoft.com ont adopté soit le [Code de conduite open source de Microsoft](https://opensource.microsoft.com/codeofconduct/), soit le [Code de conduite de .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Pour plus d’informations, consultez les [questions fréquentes (FAQ) sur le code de conduite](https://opensource.microsoft.com/codeofconduct/faq/). Vous pouvez aussi envoyer vos questions ou vos commentaires à [opencode@microsoft.com](mailto:opencode@microsoft.com) ou à [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Les corrections mineures ou les clarifications pour la documentation, ainsi que les exemples de code dans les référentiels publics, sont couverts par les [Conditions d’utilisation du site web docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Les nouveautés ou modifications significatives génèrent un commentaire dans la demande de tirage qui vous invite à signer un contrat de licence de contribution en ligne si vous n’êtes pas un employé de Microsoft. Vous devrez remplir le formulaire en ligne pour que nous puissions accepter votre requête de tirage (pull request).

## <a name="overview"></a>Vue d’ensemble

Ce flux de travail convient pour un contributeur qui a besoin de faire un changement majeur ou qui sera un contributeur fréquent d’un dépôt. Les contributeurs fréquents ont généralement des changements continus (à long terme) qui peuvent passer par plusieurs cycles de création/validation/préproduction ou être répartis sur plusieurs jours avant la validation et la fusion de la demande de tirage.

Voici des exemples de ce type de contribution :

[!INCLUDE[contribute-major-changes-change-definition](includes/contribute-how-to-write-workflows-major-change-definition.md)]

### <a name="terminology"></a>Terminologie

Avant de commencer, passons en revue quelques-uns des termes et monikers de Git/GitHub utilisés dans ce flux de travail. Vous n'avez pas à les comprendre dès maintenant. Sachez juste que vous allez les étudier et que vous pouvez revenir à cette section quand vous souhaitez vérifier une définition.

| Name | Description |
|-----------|-------------|
|embranchement|Normalement utilisé comme nom lorsqu'il est fait référence à une copie d'un référentiel GitHub principal. En pratique, un embranchement est simplement un autre référentiel. Mais il est particulier en cela que GitHub conservez une connexion avec le référentiel principal/parent. Ce terme est parfois utilisé sous forme verbale, par exemple « Vous devez d’abord dupliquer le dépôt ».|
|remote|Une connexion nommée à un référentiel distant, comme les remotes « origin » et « upstream ». Git les appelle « remotes », car elles servent à référencer un dépôt hébergé sur un autre ordinateur. Dans ce flux de travail, une connexion remote concerne toujours un référentiel GitHub.|
|origin|Nom affecté à la connexion entre votre dépôt local et le dépôt à partir duquel il a été cloné. Dans ce flux de travail, origin représente la connexion à votre embranchement. Il s’agit parfois du moniker pour le dépôt d’origine lui-même, par exemple dans la phrase « N’oubliez pas d’envoyer vos modifications sur origin ».|
|upstream|Comme pour la connexion remote origin, upstream est le nom d'une connexion vers un autre référentiel. Dans ce flux de travail, upstream représente la connexion entre votre référentiel local et le référentiel principal, à partir duquel votre embranchement a été créé. Il s’agit parfois du moniker pour le dépôt ascendant lui-même, par exemple dans la phrase « N’oubliez pas d’extraire les modifications de l’amont ».|

## <a name="workflow"></a>Flux de travail

>[!IMPORTANT]
> Si vous ne l’avez pas déjà fait, vous devez effectuer les étapes de la section [Configuration](get-started-setup-github.md). Cette section vous guide lors de la configuration de votre compte GitHub, l’installation de Git Bash et d’un éditeur Markdown, la création d’une duplication et la configuration de votre dépôt local. Si vous découvrez les concepts de Git et GitHub, comme les dépôts ou les branches, consultez d’abord les [Bases de Git et GitHub](git-github-fundamentals.md).

Dans ce flux de travail, les changements circulent dans un cycle répétitif. En partant du référentiel local de votre appareil, ils passent par votre branche GitHub, dans le référentiel GitHub principal, puis reviennent localement lorsque vous intégrez les modifications d'autres contributeurs.

### <a name="use-github-flow"></a>Utiliser le flux GitHub

Rappelez-vous, comme indiqué dans les [Bases de Git et GitHub](git-github-fundamentals.md#git), qu’un dépôt Git contient une branche principale et des branches supplémentaires en cours de modification qui n’ont pas été intégrées à la branche principale. Quand vous introduisez une série de changements liés logiquement, une bonne pratique consiste à créer une *branche de travail* pour gérer vos modifications via le flux de travail. Nous l’appelons ici branche de travail, car il s’agit d’un espace de travail pour itérer/affiner les modifications, jusqu’à ce qu’elles puissent être réintégrées à la branche principale.

Isoler les changements liés dans une branche spécifique vous permet de contrôler et d'introduire ces changements de façon indépendante, en les ciblant pour une date de publication particulière dans le cycle de publication. En réalité, en fonction du type de travail que vous faites, vous pouvez facilement vous retrouver avec plusieurs branches de travail dans votre dépôt. Il n’est pas rare de travailler sur plusieurs branches en même temps, chacune représentant un projet différent.

>[!TIP]
>L’insertion de modifications dans la branche principale n’est *pas* une bonne pratique. Supposons que vous utilisez la branche principale pour introduire une série de changements pour une publication de fonctionnalité planifiée. Vous terminez les modifications et attendez de les publier. Entre-temps, vous recevez une demande urgente de correction. Vous apportez donc la modification à un fichier dans la branche principale et publiez la modification. Dans cet exemple, vous publiez par erreur à la fois le correctif *et* les modifications que vous attendiez de publier à une date précise.

Créons maintenant une nouvelle branche de travail dans votre référentiel local pour capturer les modifications que vous proposez. Si vous avez configuré Git Bash (voir [Installer les outils de création de contenu](get-started-setup-tools.md)), vous pouvez créer une branche et « extraire » cette branche avec une commande à partir de votre dépôt cloné :

````
git checkout -b "branchname"
````

Chaque client Git est différent : consultez l’aide du client choisi. Vous trouverez une vue d’ensemble du processus dans le Guide de GitHub sur [Flux GitHub](https://guides.github.com/introduction/flow/).

## <a name="making-your-changes"></a>Apporter vos changements

Maintenant que vous avez une copie (« clone ») du dépôt Microsoft et que vous avez créé une branche, vous pouvez désormais apporter les changements qui, selon vous, seraient utiles à la communauté en utilisant n’importe quel éditeur de texte ou Markdown, comme indiqué dans la page [Installer les outils de création de contenu](get-started-setup-tools.md).  Vous pouvez enregistrer vos changements localement sans avoir à les envoyer à Microsoft tant que vous n’êtes pas prêt.

## <a name="saving-changes-to-your-repository"></a>Enregistrement des changements dans votre dépôt

Avant d’envoyer vos changements à l’auteur, vous devez d’abord les enregistrer dans votre dépôt Github.  Là encore, même si tous les outils sont différents, si vous utilisez la ligne de commande Git Bash, cette opération peut être effectuée en quelques étapes simples.

Tout d’abord, dans le dépôt, vous devez _indexer_ tous vos changements à commiter.  Vous pouvez le faire en exécutant :

````
git add --all
````

Ensuite, vous devez commiter vos changements enregistrés dans votre dépôt local.  Vous pouvez le faire dans Git Bash en exécutant :

````
git commit -m "Short Description of Changes Made"
````

Enfin, étant donné que vous avez créé cette branche sur votre ordinateur local, vous devez le faire savoir à la duplication (fork) de votre compte GitHub.com.  Si vous utilisez Git Bash, vous pouvez procéder en exécutant :

````
git push --set-upstream origin <branchname>
````

Bravo !  Votre code est maintenant dans votre dépôt GitHub et prêt pour vous permettre de créer une demande de tirage.  

>[!TIP]
> Même si vos changements sont visibles dans votre compte GitHub personnel lorsque vous les envoyez (push), aucune règle n’est nécessaire pour envoyer tout de suite une demande de tirage.  Si vous voulez vous arrêter et revenir ultérieurement pour effectuer d’autres ajustements, aucun problème !

Vous devez corriger quelque chose que vous avez envoyé ?  Aucun problème non plus !  Apportez simplement vos changements dans la même branche, puis commitez-les et envoyez-les à nouveau (inutile de définir le serveur en amont lors des pushs successifs de la même branche).

Vous avez d’autres changements à apporter qui n’ont pas de rapport avec ceux-ci ?  Revenez à la branche master et extrayez une nouvelle branche. Avec Git Bash, c’est aussi simple que ça :

````
git checkout master
git checkout -b "branchname"
````

Vous êtes maintenant dans une nouvelle branche et vous voilà très bien parti pour devenir un super contributeur.

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Étapes suivantes

Et voilà ! Vous avez apporté une contribution au contenu de docs.microsoft.com !

- Pour plus d’informations sur des sujets comme Markdown et la syntaxe des extensions Markdown, lisez l’article [Informations de référence sur Markdown](markdown-reference.md).
