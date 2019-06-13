---
title: validation-timeout
description: Explication et résolution du problème Docs Build validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024207"
---
# <a name="validation-timeout"></a><span data-ttu-id="d7a0b-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="d7a0b-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="d7a0b-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="d7a0b-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="d7a0b-105">Parfois, des problèmes temporaires affectant le service de validation, par exemple un serveur dans un état incorrect, empêchent Docs Build d’appeler correctement le service.</span><span class="sxs-lookup"><span data-stu-id="d7a0b-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="d7a0b-106">Après trois tentatives, l’appel expire et la validation est annulée pour éviter des retards de build et l’encombrement du pipeline de build.</span><span class="sxs-lookup"><span data-stu-id="d7a0b-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="d7a0b-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="d7a0b-107">Resolution</span></span>

<span data-ttu-id="d7a0b-108">Essayez de fermer puis de rouvrir votre demande de tirage ou d’exécuter à nouveau une build manuelle (uniquement pour les administrateurs de référentiel).</span><span class="sxs-lookup"><span data-stu-id="d7a0b-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="d7a0b-109">Souvent, les problèmes de service disparaissent d’eux-mêmes après la tentative initiale.</span><span class="sxs-lookup"><span data-stu-id="d7a0b-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="d7a0b-110">Si vous continuez à recevoir ce message, signalez un problème via [https://SiteHelp](https://SiteHelp) si vous êtes un employé Microsoft, ou @ citez l’auteur d’un article dans votre demande de tirage pour obtenir une assistance si vous êtes un collaborateur externe.</span><span class="sxs-lookup"><span data-stu-id="d7a0b-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
