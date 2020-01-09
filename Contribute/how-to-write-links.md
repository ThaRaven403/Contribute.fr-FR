---
title: Guide pratique pour utiliser des liens dans la documentation
description: Cet article vous aide à créer des liens vers du contenu situé sur docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: gewarren
ms.author: gewarren
ms.date: 10/31/2018
ms.openlocfilehash: 970f80b4e6ce795e0e2f15192d31680d7de6d35b
ms.sourcegitcommit: a812d716b31084926b886b93923f9b84c9b23429
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/18/2019
ms.locfileid: "75188322"
---
# <a name="use-links-in-documentation"></a>Utiliser des liens dans la documentation

Cet article décrit comment utiliser des liens hypertexte à partir de pages hébergées sur docs.microsoft.com. Vous pouvez facilement ajouter des liens dans la syntaxe Markdown en tenant compte de quelques conventions. Les liens pointent vers du contenu situé dans la même page, dans d’autres pages voisines ou vers des sites et des URL externes.

Le back-end du site docs.microsoft.com utilise OPS (Open Publishing Services) qui prend en charge Markdown conforme avec [CommonMark](https://commonmark.org/) analysé via le moteur [Markdig](https://github.com/lunet-io/markdig). Ce type Markdown est essentiellement compatible avec [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), car la plupart des documents sont stockés dans GitHub et peuvent être modifiés à cet endroit. Des fonctionnalités sont ajoutées via des extensions Markdown.

> [!IMPORTANT]
> Tous les liens doivent être sécurisés (`https` et `http`) lorsque la cible le permet (dans la grande majorité des cas).

## <a name="link-text"></a>Texte du lien

Les mots que vous incluez dans le texte doivent être conviviaux. En d’autres termes, il doit s’agir de mots simples ou du titre de la page vers laquelle vous établissez le lien.

> [!IMPORTANT]
> N’utilisez pas de texte de type « cliquez ici ». Ce n’est pas bon pour l’optimisation du référencement d’un site auprès d’un moteur de recherche et cela ne décrit pas correctement la cible.

**Correct :**

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

**Incorrect :**

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a>Liens d'un article à un autre

Pour créer un lien inline d’un article technique Docs vers un autre dans le même *docset*, utilisez la syntaxe de lien suivante :

- Un article a un lien vers un autre article du même répertoire :

  `[link text](article-name.md)`

- Un article a un lien vers un article du répertoire parent du répertoire actif :

  `[link text](../article-name.md)`

- Un article a un lien vers un article d’un sous-répertoire du répertoire actif :

  `[link text](directory/article-name.md)`

- Un article a un lien vers un article d’un sous-répertoire du répertoire parent du répertoire actif :

  `[link text](../directory/article-name.md)`

> [!NOTE]
> Aucun des exemples précédents n’utilise de `~/` dans le lien. Pour créer un lien vers un chemin absolu qui commence à la racine du dépôt, commencez le lien avec `/`. L’ajout d’un `~/` produit des liens non valides quand vous accédez aux dépôts sources sur GitHub. En commençant par une `/`, le problème est résolu.

Pour créer un lien vers un article d’un autre docset, même si le fichier se trouve dans le même dépôt, utilisez la syntaxe suivante :

`[link text](/docset-root/directory/article-name)`
   
Par exemple, si un article dont l’URL racine est `https://docs.microsoft.com/dotnet` a un lien vers un article dont l’URL racine est `https://docs.microsoft.com/visualstudio`, le lien ressemble à `[link text](/visualstudio/directory/article-name)`.

> [!TIP]
> Les articles du même *docset* ont le même fragment d’URL après « docs.microsoft.com ». Par exemple, `https://docs.microsoft.com/dotnet/core/get-started` et `https://docs.microsoft.com/dotnet/framework/install` se trouvent dans le même docset, alors que `https://docs.microsoft.com/dotnet/core/get-started` et `https://docs.microsoft.com/visualstudio/whats-new` se trouvent dans des docsets différents.

## <a name="links-to-anchors"></a>Liens vers ancres

Vous n’avez pas besoin de créer des ancres. Elles sont automatiquement générées au moment de la publication pour tous les en-têtes H2. Il vous suffit de créer des liens vers les sections H2.

- Pour faire un lien vers un en-tête au sein du même article :

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- Pour créer un lien vers une ancre d’un autre article :

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a>Liens des includes

Les fichiers include étant situés dans un autre répertoire, vous devez utiliser des chemins d'accès relatifs plus longs. Pour faire un lien vers un article à partir d'un fichier include, utilisez ce format :

   ```markdown
   [link text](../articles/folder/article-name.md)
   ```

## <a name="links-in-selectors"></a>Liens dans les sélecteurs

Un sélecteur est un composant de navigation qui apparaît dans un article de documentation sous forme de liste déroulante. Quand un lecteur sélectionne une valeur dans la liste déroulante, le navigateur ouvre l’article sélectionné. En général, la liste du sélecteur contient des liens vers des articles qui ont un rapport étroit avec celui-ci, par exemple traitant du même sujet dans différents langages de programmation, ou vers une série d’articles connexe. 

Si vous avez des sélecteurs intégrés dans un include, utilisez la structure de liens suivante :

   ```markdown
   > [AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]
   - [(Text1 | Example1 )](../articles/folder/article-name1.md)
   - [(Text1 | Example2 )](../articles/folder/article-name2.md)
   - [(Text2 | Example3 )](../articles/folder/article-name3.md)
   - [(Text2 | Example4 )](../articles/folder/article-name4.md) -->
   ```

## <a name="reference-style-links"></a>Liens de type référence

Vous pouvez utiliser des liens de type référence pour rendre votre contenu source plus facile à lire. Les liens de type référence remplacent la syntaxe de lien inline par une syntaxe simplifiée vous permettant de déplacer les URL longues à la fin de l’article. Voici l'exemple de [Daring Fireball](https://daringfireball.net/projects/markdown/) :

Texte intégré :

   ```markdown
   I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].
   ```

Liens de référence à la fin de l'article :

   ```markdown
   <!--Reference links in article-->
   [1]: http://google.com/
   [2]: http://search.yahoo.com/
   [3]: http://search.msn.com/
   ```
   
Veillez à inclure l’espace après le signe deux-points, avant le lien. Lorsque vous liez d'autres articles techniques, si vous oubliez d'inclure l'espace, le lien sera rompu dans l’article publié.

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a>Liens vers des pages qui ne font pas partie de l’ensemble de documentation technique

Pour établir un lien vers une page sur une autre propriété de Microsoft (par exemple la page de tarifs, la page du contrat SLA ou toute autre page qui n’est pas un article de documentation), utilisez une URL absolue, mais omettez les paramètres régionaux. Le but ici est que les liens fonctionnent dans GitHub et sur le site rendu :

   ```markdown
   [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)
   ```
   
## <a name="links-to-third-party-sites"></a>Liens vers des sites tiers

Une expérience utilisateur idéale minimise l'envoi d'utilisateurs vers d'autres sites. Basez donc les liens vers des sites tiers, dont nous avons parfois besoin, sur ces informations :

- **Responsabilité** : Établissez un lien vers du contenu tiers quand il s’agit des informations que le tiers est tenu de partager. Par exemple, il ne revient pas à Microsoft d’expliquer aux utilisateurs comment utiliser les outils pour développeurs d’Android. Cette tâche incombe à Google. Si besoin, nous pouvons expliquer comment utiliser les outils Android *avec* Azure, mais l'explication de l'utilisation des outils eux-mêmes est le travail de Google.
- **Validation des PM** : Demandez à Microsoft de valider le contenu tiers. En établissant un lien, nous donnons des indications de notre confiance et de nos obligations si les utilisateurs suivent les instructions.
- **Révisions d’actualisation** : Vérifiez que les informations tierces sont toujours actuelles, correctes et pertinentes, et que le lien n’a pas changé.
- **Hors site** : Informez les utilisateurs qu’ils vont vers un autre site. Si le contexte ne l’indique pas explicitement, ajoutez une phrase pour cela, Par exemple : « Les prérequis comprennent les outils pour développeurs d'Android, que vous pouvez télécharger sur le site d'Android Studio ».
- **Étapes suivantes** : Vous pouvez ajouter un lien vers, par exemple, un blog MVP dans une section « Étapes suivantes ». Encore une fois, assurez-vous juste que les utilisateurs comprennent qu’ils vont quitter le site.
- **Juridique** : Nous sommes légalement couverts sous **Liens vers des sites tiers** dans les **Conditions d’utilisation** en pied de page de chaque page ms.com.

## <a name="links-to-azure-powershell-reference-content"></a>Liens vers le contenu de la référence Azure PowerShell

Le contenu de la référence Azure PowerShell a subi plusieurs changements depuis novembre 2016. Utilisez les instructions suivantes pour faire un lien vers ce contenu depuis d'autres articles sur docs.microsoft.com.

Structure de l’URL :

* Pour les applets de commande :
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* Pour les rubriques conceptuelles :
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

La partie `<moniker-name>` est facultative. Si elle est omise, vous êtes dirigé vers la dernière version du contenu. La partie `<service-name>` correspond à l’un des exemples présentés dans les URL de base suivantes :

- Contenu Azure PowerShell (AzureRM) : [https://docs.microsoft.com/powershell/azure/](https://docs.microsoft.com/powershell/azure/)
- Contenu Azure PowerShell (ASM) : [https://docs.microsoft.com/powershell/azure/_servicemanagement_](https://docs.microsoft.com/powershell/azure/servicemanagement)
- Contenu Azure Active Directory (AzureAD) PowerShell : [https://docs.microsoft.com/powershell/azure/_active-directory_](https://docs.microsoft.com/powershell/azure/active-directory)
- Azure Service Fabric PowerShell : [https://docs.microsoft.com/powershell/azure/_service-fabric_](https://docs.microsoft.com/powershell/azure/service-fabric)
- Azure Information Protection PowerShell : [https://docs.microsoft.com/powershell/azure/_aip_](https://docs.microsoft.com/powershell/azure/aip)
- Azure Elastic DB Jobs PowerShell : [https://docs.microsoft.com/powershell/azure/_elasticdbjobs_](https://docs.microsoft.com/powershell/azure/elasticdbjobs)

Quand vous utilisez ces URL, vous êtes redirigé vers la dernière version du contenu. De cette façon, vous n’avez pas besoin de spécifier de version moniker. Vous n’avez pas non plus de liens vers du contenu conceptuel à mettre à jour quand la version change.

Pour créer le bon lien, trouvez la page vers laquelle vous voulez créer un lien dans votre navigateur, copiez l’URL et supprimez le code régional, par exemple **en-us**.

Exemple de Markdown :

```markdown
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](https://docs.microsoft.com/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](https://docs.microsoft.com/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](https://docs.microsoft.com/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](https://docs.microsoft.com/powershell/azure/install-azurerm-ps)
```
