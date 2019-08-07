---
title: validation-timeout
description: Explication et résolution du problème Docs Build validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: bb58c472371c429002cf5b35b7d6157ffb28b5cd
ms.sourcegitcommit: 495d49f10df51a8897687940aa653e906c48c2a0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68817421"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Avertissement

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or if you continue to see this message, file an issue via https://SiteHelp.`

Parfois, des problèmes temporaires affectant le service de validation, par exemple un serveur dans un état incorrect, empêchent Docs Build d’appeler correctement le service. Après plusieurs tentatives, l’appel expire et la validation est annulée pour éviter des retards de build et l’encombrement du pipeline de build.

## <a name="resolution"></a>Résolution

Essayez de fermer puis de rouvrir votre demande de tirage ou d’exécuter à nouveau une build manuelle via le portail Docs (uniquement pour les administrateurs de référentiel). Souvent, les problèmes de service disparaissent d’eux-mêmes après la tentative initiale. Si vous avez besoin de l’aide d’un administrateur ou si vous continuez à recevoir ce message, signalez un problème via [https://SiteHelp](https://SiteHelp) si vous êtes un employé Microsoft, ou @ citez l’auteur d’un article dans votre demande de tirage pour obtenir une assistance si vous êtes un collaborateur externe.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
