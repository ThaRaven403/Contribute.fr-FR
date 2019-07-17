---
title: author-missing
description: Explication et résolution du problème de génération de documents author-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 33d704d64f4a3a1d96792bb01b403aefb3143eb8
ms.sourcegitcommit: 1311ccbbf38312bfe6947082870bc9e90d38c986
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67791512"
---
# <a name="author-missing"></a><span data-ttu-id="20798-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="20798-103">author-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="20798-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="20798-104">Suggestion</span></span>

`Missing attribute: author. Add the current author's GitHub ID.`

<span data-ttu-id="20798-105">L’attribut `author` identifie l’auteur de l’article par ID GitHub.</span><span class="sxs-lookup"><span data-stu-id="20798-105">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="20798-106">Résolution</span><span class="sxs-lookup"><span data-stu-id="20798-106">Resolution</span></span>

<span data-ttu-id="20798-107">Ajoutez l’ID GitHub de l’auteur actuel à l’en-tête YML :</span><span class="sxs-lookup"><span data-stu-id="20798-107">Add the current author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<span data-ttu-id="20798-108">Notez que ce doit être le propriétaire *actuel* de l’article, pas l’auteur d’origine si l’appartenance a changé.</span><span class="sxs-lookup"><span data-stu-id="20798-108">Note that this should be the *current* owner of the article, not the original author if ownership has changed.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
