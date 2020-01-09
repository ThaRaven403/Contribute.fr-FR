---
title: Envoi d’une demande de tirage (pull request)
description: Cet article décrit le processus de demande de tirage et les bonnes pratiques pour garantir que votre contribution peut être fusionnée.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 156b5ec7b77bba5cf0a0ef2756ed8b64c21a8342
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188228"
---
# <a name="best-practices-for-pull-requests"></a>Bonnes pratiques pour les demandes de tirage

Pour publier des modifications au contenu, vous devez envoyer une requête de tirage pour votre embranchement. Chaque demande de tirage doit être révisée avant de pouvoir être fusionnée.

## <a name="target-the-correct-branch"></a>Cibler la branche correcte

Tous les changements doivent être apportés à la branche `staging`. Les changements ne doivent jamais être ciblés sur la branche `live`. Les changements apportés à la branche `staging` sont fusionnés dans `live`, de sorte que tous les changements apportés à `live` sont remplacés.

Si vous envoyez un changement à la documentation qui s’applique seulement à une version non publiée de PowerShell, vérifiez s’il existe une branche de publication (release) pour cette version. Tous les changements qui s’appliquent à une version ultérieure spécifique doivent être ciblés sur la branche de la publication (release). Les branches de publication (release) ont le modèle de nom suivant : `release-<version>`.

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a>Aidez la file d'attente de requêtes à mieux fonctionner pour tout le monde

Il existe deux réalités fondamentales dans la file d’attente de PR :

- Les demandes de tirage de petite étendue et avec des changements très similaires sont plus rapides à réviser.
- La révision des demandes de tirage de grande étendue ou contenant des changements sans liens entre eux prend plus de temps.

### <a name="avoid-branches-that-update-large-numbers-of-files"></a>Éviter les branches qui mettent à jour un grand nombre de fichiers

Séparez les mises à jour mineures à des articles existants des nouveaux articles ou révisions majeures. Travaillez sur ces changements dans des branches de travail distinctes.

Les changements en bloc entraînent des demandes de tirage avec un grand nombre de fichiers à changer. Limitez vos demandes de tirage à un maximum de 50 fichiers à changer. Les grandes demandes de tirage sont difficiles à réviser et sont plus susceptibles de contenir des erreurs.

### <a name="renaming-or-deleting-files"></a>Renommage ou suppression de fichiers

Quand vous renommez ou supprimez des fichiers, évitez de mélanger ces changements avec des ajouts ou des mises à jour du contenu.
Gérez ces changements dans une demande de tirage distincte qui sera fusionnée après la demande de tirage pour les mises à jour associées. Par exemple, mettez à jour le fichier des redirections et vérifiez que la redirection fonctionne avant de supprimer un article.

Vous devez mettre à jour tous les fichiers qui sont liés au fichier renommé. Cela comprend tous les fichiers de table des matières. Vous devez également ajouter des entrées de redirection dans le fichier de redirection maître (`.openpublishing.redirection.json`) à la racine du dépôt.

## <a name="docs-pr-validation-service"></a>Service de validation de demande de tirage (pull request) Docs

Le service de validation de demande de tirage Docs est une application GitHub qui exécuter des règles de validation sur des fichiers dans une demande de tirage.

Vous pouvez observer le comportement suivant :

1. Vous envoyez une demande de tirage.
1. Dans le commentaire GitHub qui indique l’état de votre demande de tirage, l’état des « contrôles » activés sur le dépôt s’affiche. Notez que dans cet exemple, deux contrôles sont activés : « Commit Validation » et « OpenPublishing.Build » :

   ![certains contrôles ont échoué](media/powershell-pull-requests/validation-failed.png)

   La build peut réussir même si la validation de la confirmation échoue.

1. Pour plus d’informations, cliquez sur **Détails**.
1. Dans la page Details, vous voyez tous les contrôles de validation qui ont échoué, avec des informations sur la façon de corriger les problèmes.
1. Quand la validation réussit, le commentaire suivant est ajouté à la demande de tirage :

   ![Validation de build](media/powershell-pull-requests/build-validation.png)

Si vous êtes contributeur externe (non-Microsoft), vous n’avez pas accès aux rapports de génération détaillés ni aux liens d’aperçu.

### <a name="build-warnings"></a>Avertissements de build

Normalement, vous devez corriger toutes les erreurs, tous les avertissements et toutes les suggestions d’une build. Certains avertissements peuvent cependant être ignorés.

Les avertissements suivants peuvent être ignorés :

- > Impossible de trouver le nom du service pour `<version>/<modulepath>/About/About.md`

- > Les métadonnées avec les noms suivants ne peuvent pas être définies dans l’en-tête YAML, ou sous forme de métadonnées au niveau du fichier dans docfx.json ou en tant que métadonnées globales dans docfx.json : `locale`. Elles sont générées par la plateforme Docs : les valeurs définies à ces 3 emplacements sont donc ignorées. Pour résoudre l’avertissement, supprimez-les des 3 emplacements.
