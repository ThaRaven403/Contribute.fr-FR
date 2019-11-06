---
title: validation-timeout
description: Explication et résolution du problème Docs Build validation-timeout
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9f8074d3746ea375e29704853c82f48d95273cdc
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166758"
---
# <a name="validation-timeout"></a>validation-timeout

## <a name="warning"></a>Avertissement

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or force a full build of your branch via https://ops.microsoft.com. Note that forcing a full build requires admin permissions to the repo. If you don’t know who your repo admin is, or if you continue to see this message after a forced build, file an issue via https://SiteHelp.`

Parfois, des problèmes temporaires affectant le service de validation, par exemple un serveur dans un état incorrect, empêchent Docs Build d’appeler correctement le service. Après plusieurs tentatives, l’appel expire et la validation est annulée pour éviter des retards de build et l’encombrement du pipeline de build.

## <a name="resolution"></a>Résolution

Essayez de fermer et de rouvrir votre PR ou de forcer une build complète via le [portail Docs](https://ops.microsoft.com/#/). Souvent, les problèmes de service disparaissent d’eux-mêmes après la tentative initiale.

Notez que vous devez être administrateur de référentiel pour forcer une build via le portail Docs. Si vous ne savez pas qui est votre administrateur de référentiel ou si vous continuez à recevoir ce message après une build forcée, signalez le problème via [https://SiteHelp](https://SiteHelp) si vous êtes un employé Microsoft, ou @ citez l’auteur d’un article dans votre PR pour obtenir une assistance si vous êtes un contributeur externe.

Si vous êtes administrateur de référentiel, vous pouvez forcer une build complète comme suit :

1. Accédez au [portail Docs](https://ops.microsoft.com/#/) et connectez-vous.
1. Recherchez votre référentiel en effectuant une recherche en haut à gauche, puis sélectionnez-le.

   :::image type="content" source="media/find-repo.png" alt-text="Rechercher votre référentiel via la zone de recherche du portail Docs":::
1. Sous l’onglet **Historique de build**, cliquez sur **+ Publication manuelle**.
1. Sélectionnez la branche qui reçoit l’avertissement, par exemple Master.
1. Pour la cible, conservez la valeur par défaut **Docs site**.
1. Cochez la case **Forcer la publication**.
1. Cliquez sur **Publier**.

   :::image type="content" source="media/force-build.png" alt-text="étapes pour forcer une build complète":::

Cela force une build complète sur la branche.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
