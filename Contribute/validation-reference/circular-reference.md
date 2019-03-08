---
title: circular-reference
description: Explication et résolution du problème de génération Docs circular-reference
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459208"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>Erreur

`Files '{file name 1}' and '{file name 2}' reference each other.`

Par exemple, il peut s’agit d’un fichier inclus qui établit un lien vers le fichier actuel, ou d’un lien vers un fichier qui a été redirigé vers le fichier actuel.

## <a name="resolution"></a>Résolution

Examinez les liens dans les fichiers et effectuez les modifications nécessaires pour qu’aucun fichier ne soit lié à lui-même ou ne s’inclue pas lui-même.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
