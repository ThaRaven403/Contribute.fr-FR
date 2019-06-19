---
title: Guide du contributeur Microsoft Docs - Vue d’ensemble
description: Ce guide vous explique comment contribuer au site de documentation Microsoft docs.microsoft.com.
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.openlocfilehash: 9b091f864f5191c9f7a00900ec11a4a1cffdb698
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653502"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Guide du contributeur Microsoft Docs - Vue d’ensemble

Bienvenue dans le guide du contributeur [docs.microsoft.com](https://docs.microsoft.com) (Docs) !

Plusieurs des ensembles de documents Microsoft sont open source et hébergés sur GitHub. Certains ensembles de documents ne sont pas open source, mais plusieurs ont des référentiels publics dans lesquels vous pouvez suggérer des modifications via des requêtes de tirage. Cette approche open source simplifie et améliore la communication entre les ingénieurs produit, les équipes de contenu et les clients, et offre d’autres avantages :

- _Planification en open_ des dépôts open source pour obtenir du feedback permettant de savoir quels documents sont les plus demandés.
- _Révision en open_ des dépôts open source pour publier le contenu le plus utile lors de notre première publication.
- _Mise à jour en open_ des dépôts open source pour simplifier l’amélioration en continu du contenu.

L’expérience utilisateur sur [docs.microsoft.com](https://docs.microsoft.com) intègre directement les workflows [GitHub](https://github.com) pour être encore plus agréable. Commencez par [modifier le document que vous visualisez](#quick-edits-to-existing-documents). Apportez votre aide en [révisant de nouvelles rubriques](#review-open-prs), ou [signalez des problèmes de qualité](#create-quality-issues).

> [!IMPORTANT]
> Tous les référentiels qui publient sur docs.microsoft.com ont adopté soit le [Code de conduite Microsoft Open Source](https://opensource.microsoft.com/codeofconduct/), soit le [Code de conduite .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Pour plus d’informations, consultez les [questions fréquentes (FAQ) sur le code de conduite](https://opensource.microsoft.com/codeofconduct/faq/). Vous pouvez aussi envoyer vos questions ou vos commentaires à [opencode@microsoft.com](mailto:opencode@microsoft.com) ou à [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Les corrections mineures ou les clarifications pour la documentation, ainsi que les exemples de code dans les référentiels publics, sont couverts par les [Conditions d’utilisation du site web docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Les nouveautés ou modifications significatives génèrent un commentaire dans la demande de tirage (pull request) qui vous invite à signer un contrat de licence de contribution en ligne si vous n’êtes pas un employé de Microsoft. Vous devrez remplir le formulaire en ligne pour que nous puissions examiner ou accepter votre demande de tirage (pull request).

## <a name="quick-edits-to-existing-documents"></a>Modifications rapides de documents existants

Les modifications rapides permettent de rationaliser le processus de signalement et de correction de petites erreurs et omissions dans des documents. Malgré tous nos efforts, les documents que nous publions _peuvent_ contenir de petites fautes de grammaire et d’orthographe. Même si vous pouvez signaler des problèmes et nous faire part d’erreurs, il est plus rapide et plus facile de créer une demande de tirage (pull request) pour résoudre un problème lorsque l’option est disponible.

1. Certaines pages de documents vous permettent de modifier le contenu directement dans le navigateur. Dans ce cas, un bouton **Edit (Modifier)** comme celui illustré ci-dessous s’affiche. En cliquant sur le bouton **Edit (Modifier)** , vous accédez au fichier source sur GitHub. Si le bouton **Modifier** (icône crayon sans texte) est absent, cela signifie que la page de documentation ne peut pas être modifiée.

   ![Emplacement du lien de modification](./media/index/edit-article.png)

2. Ensuite, cliquez sur l’icône crayon pour modifier l’article, comme indiqué. Si l’icône représentant un crayon est grisée, vous devez vous connecter à votre compte GitHub ou créer un compte. 

   ![Emplacement de l’icône de crayon](./media/index/edit-icon.png)


3. Effectuez vos modifications dans l’éditeur web. Cliquez sur l’onglet **Preview changes (Aperçu des modifications)** pour vérifier la mise en forme de votre modification.

4. Une fois vos modifications effectuées, faites défiler vers le bas de la page. Entrez un titre et une description de vos modifications et cliquez sur **Propose file change (Proposer une modification du fichier)** comme indiqué sur la figure suivante :

   ![Proposer une modification de fichier](./media/index/submit-pull-request.png)

5. À présent que vous avez proposé votre modification, vous devez demander aux propriétaires du référentiel de « tirer (pull) » vos modifications dans leur référentiel. Pour cela, vous utilisez une « requête de tirage (pull) ». Lorsque vous avez cliqué sur **Proposer une modification du fichier** dans la figure ci-dessus, vous devriez avoir été dirigé vers une nouvelle page qui ressemble à la figure suivante :

   ![create pull request (créer une requête de tirage)](media/index/create-pull-request.png)

   Cliquez sur **Créer une requête de tirage (pull)** , entrez un titre (et une description si vous le voulez) pour la requête de tirage (pull), puis cliquez à nouveau sur **Créer une requête de tirage (pull)** . (Si vous débutez avec GitHub, consultez [About Pull Requests (À propos des demandes de tirage)](https://help.github.com/en/articles/about-pull-requests) pour plus d’informations.)

6. Et voilà ! Les membres de l’équipe de contenu réviseront et fusionneront votre demande de tirage (PR). Vous recevrez peut-être des commentaires avec des demandes des modification si vous avez effectué des modifications majeures.

L’interface utilisateur de modification GitHub est fonction de vos autorisations dans le référentiel. Les images précédentes concernent les contributeurs qui n’ont pas d’autorisations d’écriture pour le référentiel cible. GitHub crée automatiquement une duplication (fork) du référentiel cible dans votre compte. Si vous bénéficiez d’un accès en écriture au dépôt cible, GitHub y crée une nouvelle branche. Le nom de la branche a la structure **\<GitHubId\>-patch-n**, avec votre identifiant GitHub et un identificateur numérique pour la branche du correctif.

Nous utilisons des demandes de tirage pour toutes les modifications, même pour les contributeurs bénéficiant d’un accès en écriture. La branche `master` de la plupart des référentiels étant protégée, les mises à jour doivent êtres envoyées sous forme de demandes de tirage (PR).

L’expérience de modification dans le navigateur est la mieux adaptée à des modifications mineures ou peu fréquentes. Si vous effectuez des contributions importantes ou que vous utilisez des fonctionnalités avancées de Git (comme la gestion des branches ou la résolution des conflits de fusion avancés), vous devez [dupliquer le dépôt et travailler localement](how-to-write-workflows-major.md).

> [!NOTE]
> Si cette option est activée, vous pouvez modifier un article dans **n’importe quelle langue** et, selon le type de modification, voici ce qui se produit :
> 1. toute modification linguistique approuvée permet aussi d’améliorer notre moteur de traduction automatique
> 2. toute modification qui change de manière significative le contenu de l’article sera gérée en interne pour envoyer une modification du même article en anglais, afin qu’elle soit traduite dans toutes les langues, si elle est approuvée.
> Donc, vos suggestions d’améliorations n’auront pas seulement un effet positif sur les articles dans votre langue, mais dans toutes les langues disponibles.

## <a name="review-open-prs"></a>Revue des demandes de tirage (PR) ouvertes

Vous pouvez lire les nouvelles rubriques avant leur publication en consultant les demandes de tirage (PR) actuellement ouvertes. Les révisions suivent le processus de [flux GitHub](https://guides.github.com/introduction/flow/). Vous pouvez voir les mises à jour proposées ou les nouveaux articles dans les référentiels publics. Révisez-les et ajoutez vos commentaires. Parcourez l’un de nos référentiels de documents pour consulter les demandes de tirage (PR) ouvertes des zones qui vous intéressent. Les commentaires de la communauté sur des mises à jour proposées aident toute la communauté virtuelle.

## <a name="create-quality-issues"></a>Signaler des problèmes de qualité

Nos documents font l’objet d’un travail continu. Les problèmes pertinents nous aident à concentrer nos efforts sur les priorités absolues de la communauté virtuelle. Plus vous pouvez fournir de détails, plus la signalisation du problème sera utile. Dites-nous quelles informations vous avez cherchées. Dites-nous quels termes vous avez utilisés pour la recherche. Si vous n’arrivez-pas à la lancer, dites-nous comment vous souhaitez commencer à explorer une technologie qui ne vous est pas familière.

La plupart des pages de la documentation Microsoft contiennent une section **Commentaires** au bas de la page sur laquelle vous pouvez cliquer pour laisser des **commentaires sur le produit** ou des **commentaires sur le contenu** afin d’effectuer le suivi des problèmes spécifiques à cet article.

Les problèmes permettent d’amorcer une conversation sur ce dont vous avez besoin. L’équipe chargée du contenu réagira aux problèmes signalés avec des idées concernant ce que nous pouvons ajouter et vous demandera votre avis. Lorsque nous créons un brouillon, nous vous demandons de [réviser la demande de tirage (PR)](#review-open-prs).

## <a name="get-more-involved"></a>Engagez-vous plus

D’autres rubriques vous aident à commencer à contribuer de manière productive à Microsoft Docs. Elles expliquent les extensions utilisées sur la plateforme Microsoft Docs, ainsi que l’utilisation des référentiels GitHub et des outils Markdown.
