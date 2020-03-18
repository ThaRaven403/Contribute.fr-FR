---
title: Mises à jour des métadonnées - Docs Authoring Pack
description: Découvrez comment mettre à jour les métadonnées à partir de l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336632"
---
# <a name="update-metadata"></a><span data-ttu-id="9c7f4-103">Mettre à jour les métadonnées</span><span class="sxs-lookup"><span data-stu-id="9c7f4-103">Update metadata</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="9c7f4-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="9c7f4-104">Summary</span></span>

<span data-ttu-id="9c7f4-105">Dans un fichier Markdown ( *\*.md*), deux éléments de menu contextuel sont propres aux métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-105">In a Markdown (*\*.md*) file, there are two contextual menu items specific to metadata.</span></span> <span data-ttu-id="9c7f4-106">Quand vous cliquez avec le bouton droit n’importe où dans l’éditeur de texte, vous voyez quelque chose similaire aux éléments de menu suivants :</span><span class="sxs-lookup"><span data-stu-id="9c7f4-106">When you right-click anywhere in the text editor, you will see something similar to the following menu items:</span></span>

:::image type="content" source="media/update-metadata-menu.png" alt-text="Menu contextuel de mise à jour des métadonnées":::

## <a name="update-msdate-metadata-value"></a><span data-ttu-id="9c7f4-108">Mettre à jour la valeur de métadonnées `ms.date`</span><span class="sxs-lookup"><span data-stu-id="9c7f4-108">Update `ms.date` metadata value</span></span>

<span data-ttu-id="9c7f4-109">La sélection de l’option **Update `ms.date` Metadata Value** (Mettre à jour la valeur de métadonnées `ms.date`) permet de définir la valeur `ms.date` actuelle des fichiers Markdown sur la date du jour.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-109">Selecting the **Update `ms.date` Metadata Value** option will set the current Markdown files `ms.date` value to today's date.</span></span> <span data-ttu-id="9c7f4-110">Si le document n’a pas de champ de métadonnées `ms.date`, aucune action n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-110">If the document does not have an `ms.date` metadata field, no action is taken.</span></span>

## <a name="update-implicit-metadata-values"></a><span data-ttu-id="9c7f4-111">Mettre à jour les valeurs de métadonnées implicites</span><span class="sxs-lookup"><span data-stu-id="9c7f4-111">Update implicit metadata values</span></span>

<span data-ttu-id="9c7f4-112">La sélection de l’option **Update implicit metadata values** (Mettre à jour les valeurs de métadonnées implicites) permet de rechercher et de remplacer toutes les valeurs de métadonnées possibles qui peuvent être spécifiées implicitement.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-112">Selecting the **Update implicit metadata values** option will find and replace all possible metadata values that could be implicitly specified.</span></span> <span data-ttu-id="9c7f4-113">Les valeurs de métadonnées sont spécifiées implicitement dans le fichier *docfx.json*, sous le nœud `build/fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-113">Metadata values are implicitly specified in the *docfx.json* file, under the `build/fileMetadata` node.</span></span> <span data-ttu-id="9c7f4-114">Chaque paire clé-valeur du nœud `fileMetadata` représente les valeurs par défaut des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-114">Each key value pair in the `fileMetadata` node represents metadata defaults.</span></span> <span data-ttu-id="9c7f4-115">Par exemple, un fichier Markdown dans le répertoire *top-level/sub-folder* qui omet la valeur de métadonnées `ms.author` peut spécifier implicitement une valeur par défaut à utiliser dans le nœud `fileMetadata`.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-115">For example, a Markdown file in the *top-level/sub-folder* directory that omits the `ms.author` metadata value could implicitly specify a default value to use in the `fileMetadata` node.</span></span>

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

<span data-ttu-id="9c7f4-116">Dans ce cas, tous les fichiers Markdown prennent implicitement la valeur de métadonnées `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-116">In this case, all Markdown files would implicitly take on the `ms.author: dapine` metadata value.</span></span> <span data-ttu-id="9c7f4-117">La fonctionnalité agit sur ces paramètres implicites qui se trouvent dans le fichier *docfx.json*.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-117">The feature acts on these implicit settings found in the *docfx.json* file.</span></span> <span data-ttu-id="9c7f4-118">Si un fichier Markdown contient des métadonnées dont les valeurs sont explicitement définies sur une valeur autre que les valeurs implicites, elles sont substituées.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-118">If a Markdown file contains metadata with values that are explicitly set to something other than the implicit values, they are overridden.</span></span>

<span data-ttu-id="9c7f4-119">Considérez les métadonnées de fichier Markdown suivantes, ce fichier Markdown se trouvant dans **top-level/sub-folder/includes/example.md** :</span><span class="sxs-lookup"><span data-stu-id="9c7f4-119">Consider the following Markdown file metadata, where this Markdown file resides in **top-level/sub-folder/includes/example.md**:</span></span>

```markdown
---
ms.author: someone-else
---

# Content
```

<span data-ttu-id="9c7f4-120">Si l’option **Update implicit metadata values** (Mettre à jour les valeurs de métadonnées implicites) était exécutée sur ce fichier, avec le contenu supposé de *docfx.json* ci-dessus, la valeur de métadonnées deviendrait `ms.author: dapine`.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-120">If the **Update implicit metadata values** option was executed on this file, with the assumed *docfx.json* content from above the metadata value would be updated to `ms.author: dapine`.</span></span>

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a><span data-ttu-id="9c7f4-121">En action</span><span class="sxs-lookup"><span data-stu-id="9c7f4-121">In action</span></span>

<span data-ttu-id="9c7f4-122">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-122">Below is a brief demonstration of this feature.</span></span>

<span data-ttu-id="9c7f4-123">[![Démonstration de la mise à jour des métadonnées](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9c7f4-123">[![Update metadata demo](media/update-metadata.gif)](media/update-metadata.gif#lightbox)</span></span>
