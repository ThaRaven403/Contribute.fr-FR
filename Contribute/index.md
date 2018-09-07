---
title: Guide du contributeur Microsoft Docs - Vue d’ensemble
description: Ce guide vous explique comment contribuer au site de documentation Microsoft docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 04/17/2018
ms.openlocfilehash: 94fad6f4b2faeefff687eb57cd2de8a0fb5bbbf3
ms.sourcegitcommit: 5e508a7ad2991632a38f302e4769b36e3bf37eb2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43308890"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Guide du contributeur Microsoft Docs - Vue d’ensemble

Bienvenue dans le guide du contributeur [docs.microsoft.com](https://docs.microsoft.com) (Docs) !

Beaucoup de nos ensembles de documentation sont open source et hébergés sur GitHub. Ce modèle est de plus en plus souvent adopté par les équipes Microsoft. Même les ensembles de documents qui sont pas entièrement open source ont des référentiels publics où vous êtes invité à faire des demandes de tirage (pull requests). Ceci rationalise et améliore la communication entre les ingénieurs produits, les équipes de contenu et nos clients. Le travail en open source offre de nombreux avantages :

- Un plan du référentiel open source pour savoir quels sont les documents les plus demandés.
- Une revue du référentiel open source pour publier le contenu le plus utile lors de notre première mise en production.
- Une mise à jour du référentiel open source pour faciliter l’amélioration de son contenu.

L’expérience utilisateur sur [docs.microsoft.com](https://docs.microsoft.com) intègre directement les workflows [GitHub](https://github.com) pour être encore plus agréable. Commencez par [modifier le document que vous visualisez](#quick-edits-to-existing-documents). Apportez votre aide en [révisant de nouvelles rubriques](#review-open-prs), ou [signalez des problèmes de qualité](#create-quality-issues).

> [!IMPORTANT]
> Tous les référentiels qui publient sur docs.microsoft.com ont adopté soit le [Code de conduite de Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/), soit le [Code de conduite de .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Pour plus d’informations, consultez les [questions fréquentes (FAQ) sur le code de conduite](https://opensource.microsoft.com/codeofconduct/faq/). Vous pouvez aussi envoyer vos questions ou vos commentaires à [opencode@microsoft.com](mailto:opencode@microsoft.com) ou à [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Les corrections mineures ou les clarifications pour la documentation, ainsi que les exemples de code dans les référentiels publics, sont couverts par les [Conditions d’utilisation du site web docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Les nouveautés ou modifications significatives génèrent un commentaire dans la demande de tirage (pull request) qui vous invite à signer un contrat de licence de contribution en ligne si vous n’êtes pas un employé de Microsoft. Vous devrez remplir le formulaire en ligne pour que nous puissions examiner ou accepter votre demande de tirage (pull request).

## <a name="quick-edits-to-existing-documents"></a>Modifications rapides de documents existants

Les modifications rapides permettent de rationaliser le processus de signalement et de correction de petites erreurs et omissions dans des documents. Malgré tous les efforts, nos documents publiés peuvent contenir de petites fautes de grammaire et d’orthographe. Même si vous pouvez signaler des problèmes et nous faire part d’erreurs, il est plus rapide et plus facile de créer une demande de tirage (pull request) pour résoudre un problème. Presque tous les articles sont dotés d’un bouton de modification comme celui de la figure suivante. En cliquant sur le bouton **Modification** (ou terme localisé équivalent), vous accédez au fichier source sur GitHub.

![Emplacement du lien de modification](./media/index/edit-article.png)

Cliquez ensuite sur l’icône représentant un crayon affichée sur la figure suivante pour modifier l’article.

> [!NOTE]
> Si l’icône représentant un crayon est grisée, vous devez vous connecter à votre compte GitHub ou créer un compte. Effectuez vos modifications dans l’éditeur web. Vous pouvez cliquer sur l’onglet **Aperçu der modifications** pour vérifier le format de votre modification.

![Emplacement de l’icône de crayon](./media/index/editicon.png)

Une fois vos modifications effectuées, faites défiler vers le bas de la page. Entrez un titre et une description pour votre demande de tirage (PR) et cliquez sur **Proposer une modification du fichier** comme indiqué sur la figure suivante :

![votre proposition de modification](./media/index/submit-pull-request.png)

À présent que vous avez proposé votre modification, vous devez demander aux propriétaires du référentiel de « tirer (pull) » vos modifications dans leur référentiel. Pour cela, vous utilisez une « requête de tirage (pull) ». Lorsque vous avez cliqué sur **Proposer une modification du fichier** dans la figure ci-dessus, vous devriez avoir été dirigé vers une nouvelle page qui ressemble à la figure suivante :

![créer une requête de tirage](media/index/create-pull-request.png)

Cliquez sur **Créer une requête de tirage (pull)**, entrez un titre (et une description si vous le voulez) pour la requête de tirage (pull), puis cliquez à nouveau sur **Créer une requête de tirage (pull)**.

Et voilà ! Les membres de l’équipe de contenu réviseront et fusionneront votre demande de tirage (PR). Vous recevrez peut-être des commentaires avec des demandes des modification si vous avez effectué des modifications majeures.

L’interface utilisateur de modification GitHub est fonction de vos autorisations dans le référentiel. Les images précédentes sont concernent les contributeurs qui n’ont pas d’autorisations d’écriture pour le référentiel cible. GitHub crée automatiquement une duplication (fork) du référentiel cible dans votre compte. Si vous bénéficiez d’un accès en écriture au référentiel cible, GitHub y crée une nouvelle branche. Le nom de la branche a la structure **\<GitHubId\>-patch-n**, avec votre identifiant GitHub et un identificateur numérique pour la branche du correctif.

Nous utilisons des demandes de tirage (PR) pour toutes les modifications, même pour les contributeurs bénéficiant d’un accès en écriture. La branche `master` de la plupart des référentiels étant protégée, les mises à jour doivent êtres envoyées sous forme de demandes de tirage (PR).

L’expérience de modification dans le navigateur est la mieux adaptée à des modifications mineures ou peu fréquentes. Si vous effectuez des contributions importantes, ou que vous utilisez des fonctionnalités avancées de Git (comme la gestion des branches ou la résolution des conflits de fusion avancés), vous devez [dupliquer le référentiel et travailler localement](how-to-write-workflows-major.md).

> [!NOTE]
> Si cette option est activée, vous pouvez modifier un article dans **n’importe quelle langue** et, selon le type de modification, voici ce qui se produit :
> 1. toute modification linguistique approuvée permet aussi d’améliorer notre moteur de traduction automatique
> 2. toute modification qui change de manière significative le contenu de l’article sera gérée en interne pour envoyer une modification du même article en anglais, afin qu’elle soit traduite dans toutes les langues, si elle est approuvée.
> Donc, vos suggestions d’améliorations n’auront pas seulement un effet positif sur les articles dans votre langue, mais dans toutes les langues disponibles.

## <a name="review-open-prs"></a>Réviser des demandes de tirage (PR) ouvertes

Vous pouvez lire les nouvelles rubriques avant leur publication en consultant les demandes de tirage (PR) actuellement ouvertes. Les révisions suivent le processus de [flux GitHub](https://guides.github.com/introduction/flow/). Vous pouvez voir les mises à jour proposées ou les nouveaux articles dans les référentiels publics. Révisez-les et ajoutez vos commentaires. Parcourez l’un de nos référentiels de documents pour consulter les demandes de tirage (PR) ouvertes des zones qui vous intéressent. Les commentaires de la communauté sur des mises à jour proposées aident toute la communauté virtuelle.

## <a name="create-quality-issues"></a>Signaler des problèmes de qualité

Nos documents font l’objet d’un travail continu. Les problèmes pertinents nous aident à concentrer nos efforts sur les priorités absolues de la communauté virtuelle. Plus vous pouvez fournir de détails, plus la signalisation du problème sera utile. Dites-nous quelles informations vous avez cherchées. Dites-nous quels termes vous avez utilisés pour la recherche. Si vous n’arrivez-pas à la lancer, dites-nous comment vous souhaitez commencer à explorer une technologie qui ne vous est pas familière.

Les problèmes permettent d’amorcer une conversation sur ce dont vous avez besoin. L’équipe chargée du contenu réagira aux problèmes signalés avec des idées concernant ce que nous pouvons ajouter et vous demandera votre avis. Lorsque nous créons un brouillon, nous vous demandons de [réviser la demande de tirage (PR)](#review-open-prs).

## <a name="get-more-involved"></a>Engagez-vous plus

D’autres rubriques vous aident à commencer à contribuer de manière productive à Microsoft Docs. Elles expliquent les extensions utilisées sur la plateforme Microsoft Docs, ainsi que l’utilisation des référentiels GitHub et des outils Markdown.
