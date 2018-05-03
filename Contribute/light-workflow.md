---
title: Flux de travail de contribution à GitHub pour les changements mineurs ou peu fréquents
description: Cet article vous montre comment utiliser le flux de travail de contributeur « mineur » pour contribuer aux articles de docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>Flux de travail de contribution à GitHub pour les changements mineurs ou peu fréquents

> [!IMPORTANT]
> Tous les référentiels qui publient sur docs.microsoft.com ont adopté soit le [Code de conduite open source de Microsoft](https://opensource.microsoft.com/codeofconduct/), soit le [Code de conduite de .NET Foundation](https://dotnetfoundation.org/code-of-conduct). Pour plus d’informations, consultez les [questions fréquentes (FAQ) sur le code de conduite](https://opensource.microsoft.com/codeofconduct/faq/). Vous pouvez aussi envoyer vos questions ou vos commentaires à [opencode@microsoft.com](mailto:opencode@microsoft.com) ou à [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org).<br>
>
> Les corrections mineures ou les clarifications pour la documentation, ainsi que les exemples de code dans les référentiels publics, sont couverts par les [Conditions d’utilisation du site web docs.microsoft.com](https://docs.microsoft.com/legal/termsofuse). Les nouveautés ou modifications significatives génèrent un commentaire dans la demande de tirage qui vous invite à signer un contrat de licence de contribution en ligne si vous n’êtes pas un employé de Microsoft. Vous devrez remplir le formulaire en ligne pour que nous puissions accepter votre requête de tirage (pull request).

## <a name="overview"></a>Vue d'ensemble

Ce flux de travail convient pour les changements mineurs ou peu fréquents, en utilisant l’éditeur Markdown web de GitHub. L’éditeur GitHub est limité en possibilités, car l’interface utilisateur ne prend pas en charge toutes les opérations et tous les scénarios de création de Git. Si vous souhaitez effectuer des contributions importantes, ou que vous avez besoin d’aide pour les fonctionnalités avancées de Git (comme la gestion des branches ou la résolution des conflits de fusion avancés), consultez le [flux de travail pour les changements majeurs ou à long terme](full-workflow.md).

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>Procédure d’utilisation de l’éditeur GitHub pour proposer vos modifications

1. Accédez au dépôt GitHub et au fichier Markdown correspondants de l’article. Vous pouvez utiliser l’une des méthodes suivantes :

   - Recherchez l’article en parcourant les fichiers Markdown du dépôt GitHub associé.
   - Accédez à l’article sur [docs.microsoft.com](https://docs.microsoft.com/) et sélectionnez le lien **Modifier** en haut à droite de la page.

     ![Emplacement du lien de modification](./media/light-workflow/contributetogit.png)

2. Sélectionnez l’icône de crayon **Modifier ce fichier** pour passer en mode édition :

    ![Emplacement de l’icône de crayon](./media/light-workflow/editicon.png)

3. Effectuez des modifications avec Markdown sous l’onglet **Modifier le fichier** et affichez l’aperçu de vos modifications sous l’onglet **Aperçu des modifications**. L’utilisation de l’éditeur est simple à comprendre mais, si vous avez besoin d’aide, consultez les guides suivants :

   - [Guide d'utilisation de Markdown](how-to-write-use-markdown.md)
   - [Création de fichiers sur GitHub](https://github.com/blog/1327-creating-files-on-github)
   - [Charger des fichiers sur vos référentiels](https://github.com/blog/2105-upload-files-to-your-repositories)

4. Défilez vers le bas de la page, où vous verrez un des éléments suivants :

   - **Proposer un changement de fichier** : s’affiche quand vous avez accès en lecture seule au dépôt, par exemple pour la [modification de fichiers dans le dépôt d’un autre utilisateur](https://help.github.com/articles/editing-files-in-another-user-s-repository/). Dans ce cas, GitHub créera une branche « patch » dans votre embranchement du référentiel (et créera automatiquement un embranchement si nécessaire). Après avoir sélectionné **Proposer un changement de fichier**, une page de **comparaison des modifications apportées** s’affiche pour que vous puissiez vérifier vos modifications. Sélectionnez ensuite le bouton **Create pull request** (Créer une demande de tirage) pour envoyer vos modifications dans la file d’attente des demandes de tirage, puis passez à la [section suivante](#pull-request-processing).

   - **Valider les modifications** : s’affiche quand vous avez les autorisations en écriture sur un dépôt, comme pour la [modification de fichiers dans votre propre dépôt](https://help.github.com/articles/editing-files-in-your-repository/). Dans ce cas, GitHub vous propose deux options pour enregistrer vos modifications :

     - **Valider directement sur la branche `<branch-name>`**, où `<branch-name>` est le nom de la branche sur laquelle vous étiez quand vous avez sélectionné le bouton **Modifier**. Cela applique vos modifications directement à la branche au lieu de créer une requête de tirage. Et vous avez terminé !

     - **Créer une nouvelle branche pour cette validation et lancer une demande de tirage**, qui vous demande un nom par défaut pour créer une branche. Après avoir sélectionné **Proposer un changement de fichier**, une page de **comparaison des modifications apportées** s’affiche pour que vous puissiez vérifier vos modifications. Sélectionnez ensuite le bouton **Create pull request** (Créer une demande de tirage) pour envoyer vos modifications dans la file d’attente des demandes de tirage, puis passez à la [section suivante](#pull-request-processing).

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>Étapes suivantes

- Passez aux articles « Bases de l’écriture » pour en savoir plus sur Markdown, la syntaxe des extensions Markdown et plus encore.
