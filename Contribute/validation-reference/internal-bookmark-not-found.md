---
title: internal-bookmark-not-found
description: Explication et résolution du problème de génération Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427495"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="bd8c5-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="bd8c5-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="bd8c5-104">**Bientôt disponible !**</span><span class="sxs-lookup"><span data-stu-id="bd8c5-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="bd8c5-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="bd8c5-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="bd8c5-106">Vous tentez d’établir un lien vers un titre du fichier actuel qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="bd8c5-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="bd8c5-107">Résolution</span><span class="sxs-lookup"><span data-stu-id="bd8c5-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="bd8c5-108">Vérifiez le titre vers lequel vous voulez établir un lien et mettez à jour le lien.</span><span class="sxs-lookup"><span data-stu-id="bd8c5-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="bd8c5-109">Pour établir un lien vers une section de l’article actuel, utilisez un symbole dièse, suivi des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="bd8c5-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="bd8c5-110">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets.</span><span class="sxs-lookup"><span data-stu-id="bd8c5-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="bd8c5-111">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="bd8c5-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
