---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084526"
---
# <a name="docs-pr-validation-service"></a>Service de validation de demande de tirage (pull request) Docs

Le service de validation de demande de tirage Docs est une application GitHub qui exécuter des règles de validation sur des fichiers dans une demande de tirage.

Quand le service de validation est activé sur un dépôt, vous constaterez le comportement suivant :

1. Vous envoyez une demande de tirage.
1. Dans le commentaire GitHub qui indique l’état de votre demande de tirage, l’état des « contrôles » activés sur le dépôt s’affiche. Notez que dans cet exemple, deux contrôles sont activés : « Commit Validation » et « OpenPublishing.Build » :

   ![certains contrôles ont échoué](media/validation-failed.png)

   La build peut réussir même si la validation de la confirmation échoue.

1. Pour plus d’informations, cliquez sur **Détails**.
1. Sur la page Details, tous les contrôles de validation s’affichent, avec des informations sur la façon de corriger les problèmes :

   ![message de validation](media/validation-details.png)

Pour obtenir la liste des validations actuelles du service, consultez la table des matières à gauche dans cet article.