---
title: h1-missing
description: Explication et résolution du problème de génération Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459116"
---
# <a name="h1-missing"></a><span data-ttu-id="f077c-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="f077c-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="f077c-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="f077c-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="f077c-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="f077c-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="f077c-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="f077c-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="f077c-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="f077c-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="f077c-108">Résolution</span><span class="sxs-lookup"><span data-stu-id="f077c-108">Resolution</span></span>

<span data-ttu-id="f077c-109">Pour résoudre ce problème, ajoutez un titre H1 comme premier contenu après le bloc de métadonnées YML dans votre fichier :</span><span class="sxs-lookup"><span data-stu-id="f077c-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="f077c-110">Cette règle ne s’applique pas aux fichiers inclus.</span><span class="sxs-lookup"><span data-stu-id="f077c-110">This rule does not apply to included files.</span></span> <span data-ttu-id="f077c-111">Si vous obtenez des avertissements H1 sur des fichiers inclus, vous devez plus probablement déplacer vos fichiers inclus dans un dossier `includes`.</span><span class="sxs-lookup"><span data-stu-id="f077c-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="f077c-112">Le dossier `includes` peut être à n’importe quel niveau dans le chemin du fichier.</span><span class="sxs-lookup"><span data-stu-id="f077c-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="f077c-113">En fonction du chemin, la génération Docs reconnaît le fichier comme fichier inclus et les validations H1 ne sont pas exécutées.</span><span class="sxs-lookup"><span data-stu-id="f077c-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]