---
title: h1-not-first
description: Explication et résolution du problème de génération de la documentation h1-not-first
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 09b91577f4c87125a92c0c116bc07bc7206c6833
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528910"
---
# <a name="h1-not-first"></a><span data-ttu-id="99d1c-103">h1-not-first</span><span class="sxs-lookup"><span data-stu-id="99d1c-103">h1-not-first</span></span>

## <a name="warning"></a><span data-ttu-id="99d1c-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="99d1c-104">Warning</span></span>

`Markdown content is not allowed before H1.`

<span data-ttu-id="99d1c-105">Seul le titre des métadonnées YAML peut se trouver avant le titre H1 dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="99d1c-105">Only the YAML metadata header can come before the H1 in a Markdown file.</span></span> <span data-ttu-id="99d1c-106">Par exemple, si vous voulez ajouter une note ou une image en haut de l’article, celle-ci doit venir après le titre H1.</span><span class="sxs-lookup"><span data-stu-id="99d1c-106">For example, if you want to add a note or an image at the top of the article, it must come after H1.</span></span> <span data-ttu-id="99d1c-107">Ce qui suit n’est pas autorisé :</span><span class="sxs-lookup"><span data-stu-id="99d1c-107">The following is not allowed:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
> [!NOTE]
> You can't do this.

# This is the H1
```

<span data-ttu-id="99d1c-108">Procédez plutôt comme suit :</span><span class="sxs-lookup"><span data-stu-id="99d1c-108">Do this instead:</span></span>

```markdown
---
# This is the YAML metadata header
author: meganbradley
---
# This is the H1

> [!NOTE]
> This is OK.
```

<span data-ttu-id="99d1c-109">Une autre cause courante de ce problème est les [marques d’ordre d’octet](http://www.websina.com/bugzero/kb/unicode-bom.html) avant l’en-tête YAML.</span><span class="sxs-lookup"><span data-stu-id="99d1c-109">Another common cause of this issue is [byte order marks (BOMs)](http://www.websina.com/bugzero/kb/unicode-bom.html) before the YAML header.</span></span> <span data-ttu-id="99d1c-110">Ceux-ci viennent parfois avec des problèmes d’encodage lors de la validation du contenu dans les dépôts.</span><span class="sxs-lookup"><span data-stu-id="99d1c-110">These are sometimes introduced by encoding issues when committing content to repos.</span></span> <span data-ttu-id="99d1c-111">Ils entraînent un rendu incorrect dans GitHub et doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="99d1c-111">They result in bad rendering in GitHub and should be removed.</span></span>

## <a name="resolution"></a><span data-ttu-id="99d1c-112">Résolution</span><span class="sxs-lookup"><span data-stu-id="99d1c-112">Resolution</span></span>

<span data-ttu-id="99d1c-113">Supprimez tout contenu autre que le titre des métadonnées YAML avant le titre H1.</span><span class="sxs-lookup"><span data-stu-id="99d1c-113">Remove any content other than the YAML metadata header from before the H1.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
