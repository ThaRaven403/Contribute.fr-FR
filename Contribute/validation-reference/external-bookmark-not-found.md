---
title: external-bookmark-not-found
description: Explication et résolution du problème de génération Docs external-bookmark-not-found
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427459"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="5e16e-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="5e16e-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="5e16e-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="5e16e-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="5e16e-105">Vous tentez d’établir un lien vers un titre d’un autre fichier qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="5e16e-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="5e16e-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="5e16e-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="5e16e-107">Examinez le fichier vers lequel vous établissez un lien et mettez à jour le lien de votre signet pour le faire pointer vers une section valide du fichier.</span><span class="sxs-lookup"><span data-stu-id="5e16e-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="5e16e-108">Pour établir un lien vers un titre dans un autre article, utilisez le lien relatif à un fichier ou relatif à un site plus un symbole dièse, suivi des mots du titre.</span><span class="sxs-lookup"><span data-stu-id="5e16e-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="5e16e-109">Supprimez les signes de ponctuation dans le titre et remplacez les espaces par des tirets.</span><span class="sxs-lookup"><span data-stu-id="5e16e-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="5e16e-110">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="5e16e-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
