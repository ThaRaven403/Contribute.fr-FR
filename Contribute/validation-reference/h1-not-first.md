---
title: h1-not-first
description: Explication et résolution du problème de génération de la documentation h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 09/10/2019
ms.prod: non-product-specific
ms.openlocfilehash: c5e2eeeb5c464cd2923e23110cdab9a83324e53e
ms.sourcegitcommit: 89ec9772d9cc8281c633833c6fa51f629e9cd566
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "70895459"
---
# <a name="h1-not-first"></a><span data-ttu-id="6aac2-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="6aac2-103">h1-not-first</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="6aac2-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="6aac2-104">Suggestion</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="6aac2-105">Seul le titre des métadonnées YAML peut se trouver avant le titre H1 dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="6aac2-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="6aac2-106">Par exemple, si vous voulez ajouter une note ou une image en haut de l’article, celle-ci doit venir après le titre H1.</span><span class="sxs-lookup"><span data-stu-id="6aac2-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="6aac2-107">Ce qui suit n’est pas autorisé :</span><span class="sxs-lookup"><span data-stu-id="6aac2-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="6aac2-108">Procédez plutôt comme suit :</span><span class="sxs-lookup"><span data-stu-id="6aac2-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="6aac2-109">Une autre cause courante de ce problème est les [marques d’ordre d’octet](http://www.websina.com/bugzero/kb/unicode-bom.html) avant l’en-tête YAML.</span><span class="sxs-lookup"><span data-stu-id="6aac2-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="6aac2-110">Ceux-ci viennent parfois avec des problèmes d’encodage lors de la validation du contenu dans les dépôts.</span><span class="sxs-lookup"><span data-stu-id="6aac2-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="6aac2-111">Ils entraînent un rendu incorrect dans GitHub et doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="6aac2-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="6aac2-112">Résolution</span><span class="sxs-lookup"><span data-stu-id="6aac2-112">Resolution</span></span>

<span data-ttu-id="6aac2-113">Supprimez tout contenu autre que le titre des métadonnées YAML avant le titre H1.</span><span class="sxs-lookup"><span data-stu-id="6aac2-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
