---
title: h1-in-moniker
description: Explication et résolution du problème de génération Docs h1-in-moniker.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 11/25/2019
ms.prod: non-product-specific
ms.openlocfilehash: f22ce2c9e2a014e4d8bf0ae9b61fa48b11d8c9a1
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528824"
---
# <a name="h1-in-moniker"></a><span data-ttu-id="bc15a-103">h1-in-moniker</span><span class="sxs-lookup"><span data-stu-id="bc15a-103">h1-in-moniker</span></span>

## <a name="warning"></a><span data-ttu-id="bc15a-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="bc15a-104">Warning</span></span>

`H1s are not allowed in moniker sections. Each article should have one and only one H1.`

<span data-ttu-id="bc15a-105">H1 désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="bc15a-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="bc15a-106">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="bc15a-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="bc15a-107">Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="bc15a-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="bc15a-108">Vous ne pouvez avoir qu’un seul titre H1 dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="bc15a-108">You can only have one H1 in each file.</span></span> <span data-ttu-id="bc15a-109">Les titres H1 ne sont pas autorisés dans les sections de moniker, car ils peuvent facilement provoquer des titres H1 en doublon ou manquants, selon la configuration de la gestion de versions.</span><span class="sxs-lookup"><span data-stu-id="bc15a-109">H1s aren't allowed in moniker sections, because H1s in monikers can easily cause duplicate or missing H1s depending on how versioning is configured.</span></span>

<span data-ttu-id="bc15a-110">Vous pouvez également obtenir ce message si une section de moniker contient une ligne de signe « égal » constituant un double soulignement, comme ceci : `=======`.</span><span class="sxs-lookup"><span data-stu-id="bc15a-110">You might also get this message if a moniker section contains a line of equals signs making a double underline, like this: `=======`.</span></span> <span data-ttu-id="bc15a-111">Il s’agit d’une syntaxe Markdown alternative pour un titre H1.</span><span class="sxs-lookup"><span data-stu-id="bc15a-111">This is an alternative Markdown syntax for an H1.</span></span> <span data-ttu-id="bc15a-112">Il apparaît aussi souvent dans les conflits de fusion :</span><span class="sxs-lookup"><span data-stu-id="bc15a-112">It's also commonly seen in merge conflicts:</span></span>

```markdown
<<<<<<< HEAD
...
=======
...
>>>>>>> 1d82c7efe18f86136247fb366df5030843199c19
```

## <a name="resolution"></a><span data-ttu-id="bc15a-113">Résolution</span><span class="sxs-lookup"><span data-stu-id="bc15a-113">Resolution</span></span>

<span data-ttu-id="bc15a-114">Pour résoudre ce problème, supprimez les titres H1 de toutes les sections de moniker et vérifiez que le titre H1 en haut de l’article est approprié pour toutes les sections de moniker.</span><span class="sxs-lookup"><span data-stu-id="bc15a-114">To fix this issue, remove H1s from all moniker sections, and make sure the H1 at the top of the article is appropriate for all moniker sections.</span></span> <span data-ttu-id="bc15a-115">Notez que passer des niveaux de titre, comme faire suivre H1 de H3, n’est pas autorisé.</span><span class="sxs-lookup"><span data-stu-id="bc15a-115">Note that skipping heading levels, such as following H1 with H3, isn't allowed.</span></span>

<span data-ttu-id="bc15a-116">Si un titre H1 dans une section de moniker est en fait un double soulignement (`=======`), supprimez-le ou remplacez-le par un titre de mot-dièse, comme `##`, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="bc15a-116">If an H1 in a moniker section is actually a double underline (`=======`), remove it or replace it with a hashtag heading, such as `##`, as appropriate.</span></span> <span data-ttu-id="bc15a-117">Si le double soulignement est impliqué dans un conflit de fusion, veillez également à supprimer les marqueurs de début et de fin du conflit de fusion, et le texte obsolète.</span><span class="sxs-lookup"><span data-stu-id="bc15a-117">If the double underline is part of a merge conflict, make sure to also remove the merge conflict beginning and ending markers and the obsolete text.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
