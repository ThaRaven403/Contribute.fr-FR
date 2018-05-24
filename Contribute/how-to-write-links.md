---
title: Guide pratique pour utiliser des liens dans la documentation
description: Cet article vous aide à créer des liens vers du contenu situé sur docs.microsoft.com.
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 06/29/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1699e57ac6a4dc4c5a1ef099ea183b3cbc6307cd
ms.sourcegitcommit: e046e7aad8ed22bffe5380d63a9d40f0baeecc57
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2018
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="8dcad-103">Utilisation de liens dans la documentation</span><span class="sxs-lookup"><span data-stu-id="8dcad-103">Using links in documentation</span></span>
<span data-ttu-id="8dcad-104">Cet article décrit comment utiliser des liens hypertexte à partir de pages hébergées sur docs.microsoft.com. Vous pouvez facilement ajouter des liens dans la syntaxe Markdown en tenant compte de quelques conventions.</span><span class="sxs-lookup"><span data-stu-id="8dcad-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com. Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="8dcad-105">Les liens pointent vers du contenu situé dans la même page, dans d’autres pages voisines ou sur des sites et des URL externes.</span><span class="sxs-lookup"><span data-stu-id="8dcad-105">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="8dcad-106">Le backend du site docs.microsoft.com utilise OPS (Open Publishing Services) qui implémente DFM (DocFX Flavored Markdown).</span><span class="sxs-lookup"><span data-stu-id="8dcad-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="8dcad-107">DFM, hautement compatible avec GFM (GitHub Flavored Markdown), propose des fonctionnalités supplémentaires par le biais d’extensions Markdown.</span><span class="sxs-lookup"><span data-stu-id="8dcad-107">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dcad-108">Tous les liens doivent être sécurisés (`https` et `http`) lorsque la cible le permet (dans la grande majorité des cas).</span><span class="sxs-lookup"><span data-stu-id="8dcad-108">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="8dcad-109">Texte du lien</span><span class="sxs-lookup"><span data-stu-id="8dcad-109">Link text</span></span>

<span data-ttu-id="8dcad-110">Les mots que vous incluez dans le texte doivent être conviviaux.</span><span class="sxs-lookup"><span data-stu-id="8dcad-110">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="8dcad-111">En d’autres termes, il doit s’agir de mots simples ou du titre de la page vers laquelle vous établissez le lien.</span><span class="sxs-lookup"><span data-stu-id="8dcad-111">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dcad-112">N’utilisez pas de texte de type « cliquez ici ».</span><span class="sxs-lookup"><span data-stu-id="8dcad-112">Do not use "click here."</span></span> <span data-ttu-id="8dcad-113">C'est une mauvaise pratique pour le référencement et cela ne décrit pas correctement la cible.</span><span class="sxs-lookup"><span data-stu-id="8dcad-113">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="8dcad-114">**Correct :**</span><span class="sxs-lookup"><span data-stu-id="8dcad-114">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="8dcad-115">**Incorrect :**</span><span class="sxs-lookup"><span data-stu-id="8dcad-115">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="8dcad-116">Liens d'un article à un autre</span><span class="sxs-lookup"><span data-stu-id="8dcad-116">Links from one article to another</span></span>

<span data-ttu-id="8dcad-117">Pour créer un lien inline d’un article technique Docs à un autre dans le même docset, utilisez la syntaxe de lien suivante :</span><span class="sxs-lookup"><span data-stu-id="8dcad-117">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="8dcad-118">Un article dans un répertoire fait un lien vers un autre article du même répertoire :</span><span class="sxs-lookup"><span data-stu-id="8dcad-118">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="8dcad-119">Un article fait un lien d'un sous-répertoire d'un article vers le répertoire racine :</span><span class="sxs-lookup"><span data-stu-id="8dcad-119">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="8dcad-120">Un article dans le répertoire racine fait un lien vers un article dans un sous-répertoire :</span><span class="sxs-lookup"><span data-stu-id="8dcad-120">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="8dcad-121">Un article dans un sous-répertoire fait un lien vers un article d'un autre sous-répertoire :</span><span class="sxs-lookup"><span data-stu-id="8dcad-121">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="8dcad-122">Un lien d’un article à un autre dans différents docsets (même s’ils sont dans le même dépôt) : `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="8dcad-122">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>
  
## <a name="links-to-anchors"></a><span data-ttu-id="8dcad-123">Liens vers ancres</span><span class="sxs-lookup"><span data-stu-id="8dcad-123">Links to anchors</span></span>

<span data-ttu-id="8dcad-124">Vous n’avez pas besoin de créer des ancres.</span><span class="sxs-lookup"><span data-stu-id="8dcad-124">You do not have to create anchors.</span></span> <span data-ttu-id="8dcad-125">Elles sont automatiquement générées au moment de la publication pour tous les en-têtes H2.</span><span class="sxs-lookup"><span data-stu-id="8dcad-125">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="8dcad-126">Il vous suffit de créer des liens vers les sections H2.</span><span class="sxs-lookup"><span data-stu-id="8dcad-126">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="8dcad-127">Pour faire un lien vers un en-tête au sein du même article :</span><span class="sxs-lookup"><span data-stu-id="8dcad-127">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="8dcad-128">Pour faire un lien vers une ancre dans un autre article du même sous-répertoire :</span><span class="sxs-lookup"><span data-stu-id="8dcad-128">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="8dcad-129">Pour faire un lien vers une ancre dans un autre sous-répertoire du service :</span><span class="sxs-lookup"><span data-stu-id="8dcad-129">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="8dcad-130">Liens des includes</span><span class="sxs-lookup"><span data-stu-id="8dcad-130">Links from includes</span></span>

<span data-ttu-id="8dcad-131">Les fichiers include étant situés dans un autre répertoire, vous devez utiliser des chemins d'accès relatifs plus longs.</span><span class="sxs-lookup"><span data-stu-id="8dcad-131">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="8dcad-132">Pour faire un lien vers un article à partir d'un fichier include, utilisez ce format :</span><span class="sxs-lookup"><span data-stu-id="8dcad-132">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="8dcad-133">Liens dans les sélecteurs</span><span class="sxs-lookup"><span data-stu-id="8dcad-133">Links in selectors</span></span>

<span data-ttu-id="8dcad-134">Si vous avez des sélecteurs intégrés dans un include (comme c’est le cas pour l’équipe de documentation Azure), utilisez la structure de liens suivante :</span><span class="sxs-lookup"><span data-stu-id="8dcad-134">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="8dcad-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="8dcad-135">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="8dcad-136">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="8dcad-136">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="8dcad-137">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="8dcad-137">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="8dcad-138">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="8dcad-138">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="8dcad-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="8dcad-139">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="8dcad-140">Liens de type référence</span><span class="sxs-lookup"><span data-stu-id="8dcad-140">Reference-style links</span></span>

<span data-ttu-id="8dcad-141">Vous pouvez utiliser des liens de type référence pour rendre votre contenu source plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="8dcad-141">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="8dcad-142">Les liens de type référence remplacent la syntaxe de lien inline par une syntaxe simplifiée vous permettant de déplacer les URL longues à la fin de l’article.</span><span class="sxs-lookup"><span data-stu-id="8dcad-142">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="8dcad-143">Voici l'exemple de [Daring Fireball](https://daringfireball.net/projects/markdown/) :</span><span class="sxs-lookup"><span data-stu-id="8dcad-143">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="8dcad-144">Texte intégré :</span><span class="sxs-lookup"><span data-stu-id="8dcad-144">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="8dcad-145">Liens de référence à la fin de l'article :</span><span class="sxs-lookup"><span data-stu-id="8dcad-145">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="8dcad-146">Veillez à inclure l’espace après le signe deux-points, avant le lien.</span><span class="sxs-lookup"><span data-stu-id="8dcad-146">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="8dcad-147">Lorsque vous liez d'autres articles techniques, si vous oubliez d'inclure l'espace, le lien sera rompu dans l’article publié.</span><span class="sxs-lookup"><span data-stu-id="8dcad-147">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="8dcad-148">Liens vers des pages qui ne font pas partie de l’ensemble de documentation technique</span><span class="sxs-lookup"><span data-stu-id="8dcad-148">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="8dcad-149">Pour établir un lien vers une page sur une autre propriété de Microsoft (par exemple la page de tarifs, la page du contrat SLA ou toute autre page qui n’est pas un article de documentation), utilisez une URL absolue, mais omettez les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="8dcad-149">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="8dcad-150">Le but ici est que les liens fonctionnent dans GitHub et sur le site rendu :</span><span class="sxs-lookup"><span data-stu-id="8dcad-150">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="8dcad-151">Liens vers des sites tiers</span><span class="sxs-lookup"><span data-stu-id="8dcad-151">Links to third-party sites</span></span>

<span data-ttu-id="8dcad-152">Une expérience utilisateur idéale minimise l'envoi d'utilisateurs vers d'autres sites.</span><span class="sxs-lookup"><span data-stu-id="8dcad-152">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="8dcad-153">Basez donc les liens vers des sites tiers, dont nous avons parfois besoin, sur ces informations :</span><span class="sxs-lookup"><span data-stu-id="8dcad-153">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="8dcad-154">**Responsabilité** : Établissez un lien vers du contenu tiers quand il s’agit des informations que le tiers est tenu de partager.</span><span class="sxs-lookup"><span data-stu-id="8dcad-154">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="8dcad-155">Par exemple, il ne revient pas à Microsoft d’expliquer aux utilisateurs comment utiliser les outils pour développeurs d’Android. Cette tâche incombe à Google.</span><span class="sxs-lookup"><span data-stu-id="8dcad-155">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="8dcad-156">Si besoin, nous pouvons expliquer comment utiliser les outils Android *avec* Azure, mais l'explication de l'utilisation des outils eux-mêmes est le travail de Google.</span><span class="sxs-lookup"><span data-stu-id="8dcad-156">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="8dcad-157">**Validation des PM** : Demandez à Microsoft de valider le contenu tiers.</span><span class="sxs-lookup"><span data-stu-id="8dcad-157">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="8dcad-158">En établissant un lien, nous donnons des indications de notre confiance et de nos obligations si les utilisateurs suivent les instructions.</span><span class="sxs-lookup"><span data-stu-id="8dcad-158">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="8dcad-159">**Révisions d’actualisation** : Vérifiez que les informations tierces sont toujours actuelles, correctes et pertinentes, et que le lien n’a pas changé.</span><span class="sxs-lookup"><span data-stu-id="8dcad-159">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="8dcad-160">**Hors site** : Informez les utilisateurs qu’ils vont vers un autre site.</span><span class="sxs-lookup"><span data-stu-id="8dcad-160">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="8dcad-161">Si le contexte ne l’indique pas explicitement, ajoutez une phrase pour cela,</span><span class="sxs-lookup"><span data-stu-id="8dcad-161">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="8dcad-162">par exemple « Les conditions requises comprennent les outils pour développeurs d’Android, que vous pouvez télécharger sur le site d’Android Studio ».</span><span class="sxs-lookup"><span data-stu-id="8dcad-162">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="8dcad-163">**Étapes suivantes** : Vous pouvez ajouter un lien vers, par exemple, un blog MVP dans une section « Étapes suivantes ».</span><span class="sxs-lookup"><span data-stu-id="8dcad-163">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="8dcad-164">Encore une fois, assurez-vous juste que les utilisateurs comprennent qu’ils vont quitter le site.</span><span class="sxs-lookup"><span data-stu-id="8dcad-164">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="8dcad-165">**Juridique**  : Nous sommes légalement couverts sous **Liens vers des sites tiers** dans les **Conditions d’utilisation** en pied de page de chaque page ms.com.</span><span class="sxs-lookup"><span data-stu-id="8dcad-165">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="8dcad-166">Liens vers MSDN ou TechNet</span><span class="sxs-lookup"><span data-stu-id="8dcad-166">Links to MSDN or TechNet</span></span>

<span data-ttu-id="8dcad-167">Quand vous devez créer un lien vers MSDN ou TechNet, utilisez le lien complet vers la rubrique, et supprimez les paramètres régionaux « en-us » du lien.</span><span class="sxs-lookup"><span data-stu-id="8dcad-167">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="8dcad-168">Liens vers le contenu de la référence Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8dcad-168">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="8dcad-169">Le contenu de la référence Azure PowerShell a subi plusieurs changements depuis novembre 2016.</span><span class="sxs-lookup"><span data-stu-id="8dcad-169">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="8dcad-170">Utilisez les instructions suivantes pour faire un lien vers ce contenu depuis d'autres articles sur docs.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8dcad-170">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="8dcad-171">Structure de l’URL :</span><span class="sxs-lookup"><span data-stu-id="8dcad-171">Structure of the URL:</span></span>

* <span data-ttu-id="8dcad-172">Pour les applets de commande :</span><span class="sxs-lookup"><span data-stu-id="8dcad-172">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="8dcad-173">Pour les rubriques conceptuelles :</span><span class="sxs-lookup"><span data-stu-id="8dcad-173">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="8dcad-174">La portion &lt;moniker-name&gt; est facultative.</span><span class="sxs-lookup"><span data-stu-id="8dcad-174">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="8dcad-175">Si elle est omise, vous êtes dirigé vers la dernière version du contenu.</span><span class="sxs-lookup"><span data-stu-id="8dcad-175">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="8dcad-176">La partie &lt;service-name&gt; correspond à l’un des exemples présentés dans les URL de base suivantes :</span><span class="sxs-lookup"><span data-stu-id="8dcad-176">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="8dcad-177">Contenu Azure PowerShell (AzureRM) : https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="8dcad-177">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="8dcad-178">Contenu Azure PowerShell (ASM) : https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="8dcad-178">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="8dcad-179">Contenu Azure Active Directory (AzureAD) PowerShell : https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="8dcad-179">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="8dcad-180">Azure Service Fabric PowerShell : https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="8dcad-180">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="8dcad-181">Azure Information Protection PowerShell : https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="8dcad-181">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="8dcad-182">Azure Elastic DB Jobs PowerShell : https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="8dcad-182">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="8dcad-183">Quand vous utilisez ces URL, vous êtes redirigé vers la dernière version du contenu.</span><span class="sxs-lookup"><span data-stu-id="8dcad-183">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="8dcad-184">De cette façon, vous n’avez pas besoin de spécifier de version moniker.</span><span class="sxs-lookup"><span data-stu-id="8dcad-184">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="8dcad-185">Vous n’avez pas non plus de liens vers du contenu conceptuel à mettre à jour quand la version change.</span><span class="sxs-lookup"><span data-stu-id="8dcad-185">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="8dcad-186">Pour créer le lien approprié, trouvez la page vers laquelle vous voulez établir un lien dans votre navigateur et copiez l’URL.</span><span class="sxs-lookup"><span data-stu-id="8dcad-186">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="8dcad-187">Ensuite, supprimez « https://docs.microsoft.com » et les informations sur les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="8dcad-187">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="8dcad-188">Quand vous créez un lien depuis une table des matières, vous devez utiliser l’URL complète sans les informations de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="8dcad-188">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="8dcad-189">Exemple de Markdown :</span><span class="sxs-lookup"><span data-stu-id="8dcad-189">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
