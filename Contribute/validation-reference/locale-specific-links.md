---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653548"
---
# <a name="locale-specific-links"></a><span data-ttu-id="5dcf5-101">Liens spécifiques aux paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="5dcf5-101">Locale-specific links</span></span>

<span data-ttu-id="5dcf5-102">Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dcf5-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="5dcf5-103">Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit.</span><span class="sxs-lookup"><span data-stu-id="5dcf5-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="5dcf5-104">Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.</span><span class="sxs-lookup"><span data-stu-id="5dcf5-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="5dcf5-105">Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5dcf5-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="5dcf5-106">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="5dcf5-106">The following is an example.</span></span>

<span data-ttu-id="5dcf5-107">Avant :</span><span class="sxs-lookup"><span data-stu-id="5dcf5-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="5dcf5-108">Après :</span><span class="sxs-lookup"><span data-stu-id="5dcf5-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="5dcf5-109">Les sites suivants sont dans la portée de cette validation :</span><span class="sxs-lookup"><span data-stu-id="5dcf5-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="5dcf5-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5dcf5-110">azure.microsoft.com</span></span>
- <span data-ttu-id="5dcf5-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5dcf5-111">docs.microsoft.com</span></span>
- <span data-ttu-id="5dcf5-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5dcf5-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="5dcf5-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5dcf5-113">technet.microsoft.com</span></span>