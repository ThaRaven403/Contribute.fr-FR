---
title: ms-author-invalid
description: Explication et résolution du problème de génération Docs ms-author-invalid
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ae01c34ea60cec30698d7e11264d05c3f398d1c
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791553"
---
# <a name="ms-author-invalid"></a>ms-author-invalid

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>Suggestion

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a>Résolution

Vérifiez que la valeur `ms.author` est l’alias Microsoft valide de l’auteur actuel. Si l’alias est une liste de distribution, il doit également figurer dans la liste verte.

Vous trouverez les valeurs valides des listes de distribution sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
