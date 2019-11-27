---
title: h1-missing
description: Explication et résolution du problème de génération Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ff29a06b5a8d53d0152329807acc416463f4fe2
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528904"
---
# <a name="h1-missing"></a><span data-ttu-id="5d082-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="5d082-103">h1-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="5d082-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5d082-104">Suggestion</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="5d082-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="5d082-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="5d082-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="5d082-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="5d082-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="5d082-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="5d082-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="5d082-108">Resolution</span></span>

<span data-ttu-id="5d082-109">Pour résoudre ce problème, ajoutez un titre H1 comme premier contenu après le bloc de métadonnées YML dans votre fichier :</span><span class="sxs-lookup"><span data-stu-id="5d082-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="5d082-110">Cette règle ne s’applique pas aux fichiers inclus.</span><span class="sxs-lookup"><span data-stu-id="5d082-110">This rule does not apply to included files.</span></span> <span data-ttu-id="5d082-111">Si vous recevez des résultats H1 sur des fichiers inclus, vous devez plus probablement déplacer vos fichiers inclus dans un dossier `includes`.</span><span class="sxs-lookup"><span data-stu-id="5d082-111">If you get H1 results on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="5d082-112">Le dossier `includes` peut être à n’importe quel niveau dans le chemin du fichier.</span><span class="sxs-lookup"><span data-stu-id="5d082-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="5d082-113">En fonction du chemin, la génération Docs reconnaît le fichier comme fichier inclus et les validations H1 ne sont pas exécutées.</span><span class="sxs-lookup"><span data-stu-id="5d082-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>
>
> <span data-ttu-id="5d082-114">Une cause courante de l’absence de validations H1 dans les fichiers parents est l’utilisation incorrecte des fichiers inclus : H1 se trouve dans le fichier inclus et non dans le fichier parent.</span><span class="sxs-lookup"><span data-stu-id="5d082-114">A common cause of missing H1s in parent files is misuse of included files: the H1 is in the included file, not in the parent file.</span></span> <span data-ttu-id="5d082-115">Cela n’est pas autorisé, car l’utilisation de H1 dans un fichier inclus signifie qu’il existe des doublons de H1 dans des fichiers parents ou que le fichier inclus n’est utilisé qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="5d082-115">This isn't allowed, because using an H1 in an included file either means there are duplicate H1s in parent files or the included file is used only once.</span></span> <span data-ttu-id="5d082-116">Les validations H1 doivent être uniques au sein d’un jeu de contenu et les fichiers inclus ne doivent être utilisés que pour partager du contenu entre plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="5d082-116">H1s should be unique within a content set and included files should only be used to share content among multiple files.</span></span> <span data-ttu-id="5d082-117">Si vous recevez des résultats `h1-missing` parce que H1 se trouve dans un fichier inclus, la solution consiste à déplacer H1 – et tout le contenu inclus si le fichier inclus est utilisé une seule fois – dans le fichier parent.</span><span class="sxs-lookup"><span data-stu-id="5d082-117">If you get `h1-missing` results because the H1 is in an included file, the solution is to move the H1 - and all the included content if the included file is used only once - into the parent file.</span></span> <span data-ttu-id="5d082-118">Pour plus d’informations sur les fichiers inclus dans docs, consultez l’article interne de Microsoft [Inclure du contenu réutilisable dans des articles.](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master)</span><span class="sxs-lookup"><span data-stu-id="5d082-118">For more information about included files in Docs, see the Microsoft-internal article [Include reusable content in articles](https://review.docs.microsoft.com/en-us/help/contribute/includes-best-practices?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
