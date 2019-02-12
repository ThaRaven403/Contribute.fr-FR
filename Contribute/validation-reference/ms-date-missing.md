---
title: ms-date-missing
description: Explication et résolution du problème de génération de documents ms-date-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713243"
---
# <a name="ms-date-missing"></a>ms-date-missing

**Bientôt disponible !**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

La date est utilisée pour indiquer la « fraîcheur », c’est-à-dire la date à laquelle la pertinence, la précision, les captures d’écran et le fonctionnement des liens ont été vérifiés dans l’article. Cela ne correspond pas à la dernière date à laquelle l’article a été *publié*, qui s’affiche sur la page si `ms.date` n’est pas explicitement spécifié.

## <a name="resolution"></a>Résolution

Confirmez que l’article est à jour sans contenu rompu, puis ajoutez une date valide au format MM/JJ/AAAA.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
