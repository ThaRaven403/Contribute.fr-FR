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
# <a name="docs-pr-validation-service"></a><span data-ttu-id="5f79d-101">Service de validation de demande de tirage (pull request) Docs</span><span class="sxs-lookup"><span data-stu-id="5f79d-101">Docs PR validation service</span></span>

<span data-ttu-id="5f79d-102">Le service de validation de demande de tirage Docs est une application GitHub qui exécuter des règles de validation sur des fichiers dans une demande de tirage.</span><span class="sxs-lookup"><span data-stu-id="5f79d-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="5f79d-103">Quand le service de validation est activé sur un dépôt, vous constaterez le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="5f79d-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="5f79d-104">Vous envoyez une demande de tirage.</span><span class="sxs-lookup"><span data-stu-id="5f79d-104">You submit a PR.</span></span>
1. <span data-ttu-id="5f79d-105">Dans le commentaire GitHub qui indique l’état de votre demande de tirage, l’état des « contrôles » activés sur le dépôt s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5f79d-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="5f79d-106">Notez que dans cet exemple, deux contrôles sont activés : « Commit Validation » et « OpenPublishing.Build » :</span><span class="sxs-lookup"><span data-stu-id="5f79d-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![certains contrôles ont échoué](media/validation-failed.png)

   <span data-ttu-id="5f79d-108">La build peut réussir même si la validation de la confirmation échoue.</span><span class="sxs-lookup"><span data-stu-id="5f79d-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="5f79d-109">Pour plus d’informations, cliquez sur **Détails**.</span><span class="sxs-lookup"><span data-stu-id="5f79d-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="5f79d-110">Sur la page Details, tous les contrôles de validation s’affichent, avec des informations sur la façon de corriger les problèmes :</span><span class="sxs-lookup"><span data-stu-id="5f79d-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![message de validation](media/validation-details.png)

<span data-ttu-id="5f79d-112">Pour obtenir la liste des validations actuelles du service, consultez la table des matières à gauche dans cet article.</span><span class="sxs-lookup"><span data-stu-id="5f79d-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>