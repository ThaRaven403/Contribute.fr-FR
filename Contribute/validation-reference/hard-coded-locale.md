---
title: hard-coded-locale
description: Explication et résolution du problème de génération Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427405"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="50de8-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="50de8-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="50de8-104">Avertissement</span><span class="sxs-lookup"><span data-stu-id="50de8-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="50de8-105">Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="50de8-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="50de8-106">Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit.</span><span class="sxs-lookup"><span data-stu-id="50de8-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="50de8-107">Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.</span><span class="sxs-lookup"><span data-stu-id="50de8-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="50de8-108">Les sites suivants sont dans la portée de cette validation :</span><span class="sxs-lookup"><span data-stu-id="50de8-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="50de8-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="50de8-109">azure.microsoft.com</span></span>
- <span data-ttu-id="50de8-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="50de8-110">docs.microsoft.com</span></span>
- <span data-ttu-id="50de8-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="50de8-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="50de8-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="50de8-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="50de8-113">Résolution</span><span class="sxs-lookup"><span data-stu-id="50de8-113">Resolution</span></span>

<span data-ttu-id="50de8-114">Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="50de8-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="50de8-115">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="50de8-115">The following is an example.</span></span>

<span data-ttu-id="50de8-116">Avant :</span><span class="sxs-lookup"><span data-stu-id="50de8-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="50de8-117">Après :</span><span class="sxs-lookup"><span data-stu-id="50de8-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]