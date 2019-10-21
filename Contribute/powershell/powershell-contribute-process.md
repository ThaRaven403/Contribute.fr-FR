---
title: Processus de contribution pour les dépôts de documentation PowerShell
description: Cet article fournit une brève introduction à la contribution aux dépôts de documentation PowerShell. Vous découvrirez les dépôts utilisés, le processus d’organisation du contenu et les stratégies de gestion des exemples de code et autres ressources.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/07/2019
ms.openlocfilehash: 9802942dccbfad2cb860739ffba4b30d2b0af0c9
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290193"
---
# <a name="process-for-contributing-to-powershell-docs"></a>Processus de contribution à la documentation PowerShell

Nous apprécions toute contribution de la communauté à la documentation. Vous trouverez ci-dessous quelques règles qu’il convient de garder à l’esprit quand vous contribuez à la documentation PowerShell :

- Ne nous surprenez **pas** avec de grandes demandes de tirage (pull requests). Ouvrez plutôt un problème et lancez une discussion pour que nous puissions nous entendre sur la marche à suivre, ceci afin de ne pas gaspiller votre temps inutilement.
- **SUIVEZ** ces instructions et les guides de style pour le [code ](powershell-style-code.md) et les [informations de référence](powershell-style-reference.md).
- **Utilisez** le fichier de [modèle](powershell-style-basic-markdown.md) comme point de départ pour votre travail.
- **Créez** une branche distincte sur votre duplication (fork) avant de travailler sur les articles.
- **Suivez** le [workflow GitHub Flow](../how-to-write-workflows-major.md).
- **Rédigez** fréquemment des tweets et des billets de blog (ou autres) concernant vos contributions.

Le respect de ces instructions est garant d’une meilleure expérience à la fois pour vous et pour nous.

## <a name="make-a-contribution-to-powershell-docs"></a>Contribuer à la documentation PowerShell

Vous pouvez choisir parmi les [problèmes](https://github.com/MicrosoftDocs/PowerShell-Docs/issues/new/choose) existants.
En fonction de vos intérêts et de votre niveau d’implication, vous pouvez choisir parmi les catégories suivantes :

- **Petites modifications** . Pour les petits changements, consultez les instructions relatives aux modifications dans GitHub dans la [page d’accueil](../index.md#quick-edits-to-existing-documents) du guide du contributeur. Les petites modifications sont les suivantes :

  - Correction des fautes de frappe et d’orthographe
  - Amélioration de la grammaire ou de la mise en forme
  - Modifications techniques ou factuelles mineures

- **Maintenance**. Cette catégorie comprend des contributions assez simples, telles que la réparation de liens rompus ou incorrects, l’ajout d’exemples de code manquants ou la résolution de problèmes de contenu limités. Dans certains cas, ces problèmes peuvent concerner de grandes quantités de fichiers. Vous devez alors nous indiquer sur quoi vous souhaitez travailler avant de commencer. Ajoutez un commentaire au problème pour nous signaler que vous travaillez dessus.

- **Mises à jour de contenu**. Étant donné la taille gigantesque du jeu de documentation, le contenu devient facilement obsolète et nécessite une révision. De plus, pour diverses raisons une partie du contenu est dupliquée, voir tripliquée. La mise à jour du contenu implique de s’assurer que chacune des rubriques est à jour ou de réviser le contenu d’un domaine de fonctionnalités afin d’éliminer la duplication et de garantir que tout le contenu unique est préservé dans le jeu de documentation plus petit.

- **Création de nouveau contenu**. Si vous souhaitez créer votre propre rubrique, ces problèmes listent les rubriques que nous aimerions vouloir ajouter à notre jeu de documentation. Veillez tout de même à nous le signaler avant de commencer à travailler sur une rubrique. Si vous souhaitez créer une rubrique qui n’est pas mentionnée ici, ouvrez un problème.

Une fois que vous avez choisi une tâche sur laquelle travailler, suivez le guide [Bien démarrer](../get-started-setup-github.md) pour créer un compte GitHub et configurer votre environnement.

### <a name="making-large-changes"></a>Apporter des modifications de grande ampleur

**Étape 1** : Si vous souhaitez rédiger du nouveau contenu ou réviser du contenu existant en profondeur, ouvrez un problème décrivant ce que vous voulez faire.

**Étape 2** : Dupliquez (fork) le dépôt `MicrosoftDocs/PowerShell-Docs` et créez une branche de travail pour vos modifications.

**Étape 3** : Effectuez les changements dans cette nouvelle branche.

S’il s’agit d’une nouvelle rubrique, utilisez le modèle du [guide de style](powershell-style-basic-markdown.md) comme point de départ. Le guide de style contient les instructions de rédaction et explique les métadonnées nécessaires pour chaque article.

Accédez au dossier qui correspond à l’emplacement dans la Table des matières déterminé pour votre article à l’étape 1.
Ce dossier contient les fichiers Markdown pour tous les articles de cette section. Si nécessaire, créez un nouveau dossier où placer les fichiers pour votre contenu. L’article principal de cette section se nomme *index.md*.
Pour les images et autres ressources statiques, créez (s’il n’existe pas) un sous-dossier nommé **media** dans le dossier qui contient votre article. Dans le dossier **media**, créez un sous-dossier avec le nom de l’article (sauf le fichier d’index).

Veillez à bien respecter la syntaxe Markdown. Pour obtenir des instructions et des exemples détaillés, consultez le [guide de style](powershell-style-basic-markdown.md).

**Exemple de structure**

```
reference
  /docs-conceptual
    /learn
      /remoting
        managing-remote-sessions.md
        /images
          /managing-remote-sessions
            sesssion-list.png
```

**Étape 4** : Envoyez une demande de tirage (pull request) depuis votre branche de travail vers la branche *staging*.

Normalement, une demande de tirage ne doit concerner qu’un seul problème à la fois. La demande de tirage peut modifier un un plusieurs fichiers. Si vous traitez plusieurs correctifs sur plusieurs fichiers, il est préférable de soumettre plusieurs demandes de tirage.

Si votre demande de tirage résout un problème existant, ajoutez le mot clé `Fixes #Issue_Number` au message de validation ou à la description de la demande de tirage. Ainsi, le problème sera fermé automatiquement lors de la fusion de la demande de tirage. Pour plus d’informations, consultez [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).

L’équipe PowerShell révise votre demande de tirage et vous indique si d’autres changements sont nécessaires pour l’approuver.

**Étape 5** : Apportez les mises à jour nécessaires à votre branche, comme convenu avec l’équipe.

Une fois la demande de tirage approuvée, les responsables de la maintenance fusionnent votre demande de tirage dans la branche *staging*. Nous envoyons (push) régulièrement toutes les validations de la branche *staging* vers la branche *live*. Une fois votre contribution active, vous pouvez la voir sur le [site de la documentation PowerShell](https://docs.microsoft.com/PowerShell/). En règle générale, nous publions deux à trois fois au cours de la semaine.

## <a name="contributor-license-agreement"></a>Contrat de licence pour les contributeurs

Vous devez signer le [contrat de licence de contribution](https://cla.opensource.microsoft.com/MicrosoftDocs/PowerShell-Docs) avant que votre demande de tirage soit fusionnée. Il s’agit d’une obligation ponctuelle pour contribuer à notre documentation.

Vous n’êtes pas obligé de signer le contrat tout de suite. Vous pouvez cloner, dupliquer (fork) et soumettre votre demande de tirage comme d’habitude.
Une fois votre demande de tirage créée, elle est classifiée par un bot CLA. Si le changement est mineur (par exemple, vous avez corrigé une faute de frappe), la demande de tirage est libellée avec `cla-not-required`. Sinon, elle est classifiée en tant que `cla-required`. Une fois que vous avez signé le CLA, la demande de tirage actuelle et toutes les demandes ultérieures sont libellées en tant que `cla-signed`.
