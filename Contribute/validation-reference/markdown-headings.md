---
title: Titres Markdown
description: Décrit la configuration requise pour les titres Markdown.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084486"
---
# <a name="markdown-headings"></a><span data-ttu-id="d105f-103">Titres Markdown</span><span class="sxs-lookup"><span data-stu-id="d105f-103">Markdown headings</span></span>

<span data-ttu-id="d105f-104">Les exigences de validation suivantes s’appliquent aux titres dans les fichiers Markdown OPS.</span><span class="sxs-lookup"><span data-stu-id="d105f-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="d105f-105">H1</span><span class="sxs-lookup"><span data-stu-id="d105f-105">H1</span></span>

<span data-ttu-id="d105f-106">`H1` désigne le premier titre dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="d105f-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="d105f-107">Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="d105f-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="d105f-108">Un titre H1 est créé en commençant une ligne par un seul signe dièse (`#`) suivi d’un espace, puis du texte du titre.</span><span class="sxs-lookup"><span data-stu-id="d105f-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="d105f-109">Par exemple, le titre H1 de cet article est :</span><span class="sxs-lookup"><span data-stu-id="d105f-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="d105f-110">Les règles suivantes s’appliquent aux titres H1 :</span><span class="sxs-lookup"><span data-stu-id="d105f-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="d105f-111">Un titre H1 doit être présent dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d105f-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="d105f-112">Il ne peut y avoir qu’un seul titre H1.</span><span class="sxs-lookup"><span data-stu-id="d105f-112">There can only be one H1.</span></span>
- <span data-ttu-id="d105f-113">Le titre H1 doit avoir un contenu.</span><span class="sxs-lookup"><span data-stu-id="d105f-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="d105f-114">Il doit y avoir un espace entre le signe `#` et le contenu de le titre H1.</span><span class="sxs-lookup"><span data-stu-id="d105f-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="d105f-115">Un titre H1 sans espace ne s’affiche pas comme un titre sur la page publiée.</span><span class="sxs-lookup"><span data-stu-id="d105f-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="d105f-116">Le titre H1 doit être le premier contenu du fichier après l’en-tête de métadonnées YML.</span><span class="sxs-lookup"><span data-stu-id="d105f-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="d105f-117">Aucun contenu, comme du texte ou des images, n’est autorisé entre la fin de l’en-tête YML et le titre H1.</span><span class="sxs-lookup"><span data-stu-id="d105f-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="d105f-118">L’élément HTML des titres de premier niveau, `<h1>`, ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="d105f-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="d105f-119">Utilisez la syntaxe Markdown (`# `).</span><span class="sxs-lookup"><span data-stu-id="d105f-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="d105f-120">H1 ne doit pas contenir plus de 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="d105f-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="d105f-121">Il s’agit d’une règles de style.</span><span class="sxs-lookup"><span data-stu-id="d105f-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="d105f-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="d105f-122">H2 - H6</span></span>

<span data-ttu-id="d105f-123">Les titres H2 (`## `) à H6 (`###### `) sont autorisés dans OPS.</span><span class="sxs-lookup"><span data-stu-id="d105f-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="d105f-124">Utilisez les en-têtes Markdown, et non pas du code HTML (`<h2>` - `<h6>`), pour créer des titres.</span><span class="sxs-lookup"><span data-stu-id="d105f-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
