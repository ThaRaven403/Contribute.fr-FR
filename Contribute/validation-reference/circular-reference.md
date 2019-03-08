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
# <a name="circular-reference"></a><span data-ttu-id="df4d1-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="df4d1-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="df4d1-104">Erreur</span><span class="sxs-lookup"><span data-stu-id="df4d1-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="df4d1-105">Par exemple, il peut s’agit d’un fichier inclus qui établit un lien vers le fichier actuel, ou d’un lien vers un fichier qui a été redirigé vers le fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="df4d1-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="df4d1-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="df4d1-106">Resolution</span></span>

<span data-ttu-id="df4d1-107">Examinez les liens dans les fichiers et effectuez les modifications nécessaires pour qu’aucun fichier ne soit lié à lui-même ou ne s’inclue pas lui-même.</span><span class="sxs-lookup"><span data-stu-id="df4d1-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
