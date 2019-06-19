---
title: validation-timeout
description: Explication et résolution du problème Docs Build validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033294"
---
# <a name="validation-timeout"></a><span data-ttu-id="266cf-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="266cf-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="266cf-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="266cf-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="266cf-105">Parfois, des problèmes temporaires affectant le service de validation, par exemple un serveur dans un état incorrect, empêchent Docs Build d’appeler correctement le service.</span><span class="sxs-lookup"><span data-stu-id="266cf-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="266cf-106">Après plusieurs tentatives, l’appel expire et la validation est annulée pour éviter des retards de build et l’encombrement du pipeline de build.</span><span class="sxs-lookup"><span data-stu-id="266cf-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="266cf-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="266cf-107">Resolution</span></span>

<span data-ttu-id="266cf-108">Essayez de fermer puis de rouvrir votre demande de tirage ou d’exécuter à nouveau une build manuelle via le portail Docs (uniquement pour les administrateurs de référentiel).</span><span class="sxs-lookup"><span data-stu-id="266cf-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="266cf-109">Souvent, les problèmes de service disparaissent d’eux-mêmes après la tentative initiale.</span><span class="sxs-lookup"><span data-stu-id="266cf-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="266cf-110">Si vous avez besoin de l’aide d’un administrateur ou si vous continuez à recevoir ce message, signalez un problème via [https://SiteHelp](https://SiteHelp) si vous êtes un employé Microsoft, ou @ citez l’auteur d’un article dans votre demande de tirage pour obtenir une assistance si vous êtes un collaborateur externe.</span><span class="sxs-lookup"><span data-stu-id="266cf-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
