---
title: internal-bookmark-not-found
description: Explication et résolution du problème de génération Docs internal-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 9/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: 53b98f8da199e3495cc00b2388d983191268eee6
ms.sourcegitcommit: 89147521f0aa3b39e7ddf390136b09a43d95c416
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "70856217"
---
# <a name="bookmark-not-found"></a><span data-ttu-id="c593d-103">bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="c593d-103">bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="c593d-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="c593d-104">Warning</span></span>

`Cannot find bookmark '{bookmark-id}' in '{parent-file}'.`

<span data-ttu-id="c593d-105">Vous tentez d’établir un lien vers un titre du fichier actuel ou un autre fichier qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c593d-105">You're trying to link to a heading in the current file or another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="c593d-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="c593d-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="c593d-107">Vérifiez le titre vers lequel vous voulez établir un lien et mettez à jour le lien.</span><span class="sxs-lookup"><span data-stu-id="c593d-107">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="c593d-108">Pour établir un lien vers une section de l’article actuel, utilisez un symbole dièse, suivi des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="c593d-108">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="c593d-109">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets.</span><span class="sxs-lookup"><span data-stu-id="c593d-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c593d-110">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="c593d-110">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="c593d-111">Pour établir un lien vers un titre dans un autre fichier, utilisez un lien relatif vers ce fichier, suivi du symbole dièse et des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="c593d-111">To link to a heading in another file, use a relative link to that file, followed by a hash symbol and the words of the heading.</span></span> <span data-ttu-id="c593d-112">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets.</span><span class="sxs-lookup"><span data-stu-id="c593d-112">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="c593d-113">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="c593d-113">The following is an example:</span></span>

```markdown
See [the Resolution section in h1-empty](h1-empty.md#resolution).
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
