---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: Liens spécifiques aux paramètres régionaux
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841258"
---
# <a name="locale-specific-links"></a><span data-ttu-id="717e7-102">Liens spécifiques aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="717e7-102">Locale-specific links</span></span>

<span data-ttu-id="717e7-103">Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="717e7-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="717e7-104">Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit.</span><span class="sxs-lookup"><span data-stu-id="717e7-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="717e7-105">Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.</span><span class="sxs-lookup"><span data-stu-id="717e7-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="717e7-106">Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="717e7-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="717e7-107">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="717e7-107">The following is an example.</span></span>

<span data-ttu-id="717e7-108">Avant :</span><span class="sxs-lookup"><span data-stu-id="717e7-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="717e7-109">Après :</span><span class="sxs-lookup"><span data-stu-id="717e7-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="717e7-110">Les sites suivants sont dans la portée de cette validation :</span><span class="sxs-lookup"><span data-stu-id="717e7-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="717e7-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="717e7-111">azure.microsoft.com</span></span>
- <span data-ttu-id="717e7-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="717e7-112">docs.microsoft.com</span></span>
- <span data-ttu-id="717e7-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="717e7-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="717e7-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="717e7-114">technet.microsoft.com</span></span>