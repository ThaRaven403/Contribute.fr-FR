---
title: included-file-redirected
description: Explication et résolution du problème de génération Docs included-file-redirected
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459070"
---
# <a name="included-file-redirected"></a><span data-ttu-id="e652c-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="e652c-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="e652c-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="e652c-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="e652c-105">Résolution</span><span class="sxs-lookup"><span data-stu-id="e652c-105">Resolution</span></span>

<span data-ttu-id="e652c-106">Restructurez votre contenu de façon à ne pas inclure un fichier redirigé.</span><span class="sxs-lookup"><span data-stu-id="e652c-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="e652c-107">Par exemple, créez un fichier pour ajouter ou supprimer la référence incluse, et établissez un lien vers le contenu ou écrivez-le inline.</span><span class="sxs-lookup"><span data-stu-id="e652c-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
