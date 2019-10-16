---
title: Bases de Git et GitHub pour la documentation
description: Cet article propose une vue d’ensemble de Git, du dépôt GitHub et de la façon dont le contenu est organisé. Il décrit aussi les conventions de nommage utilisées pour docs.microsoft.com.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 06/30/2017
ms.openlocfilehash: 5154b80102069f1d5526b744637f8ba854f1fe3f
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288445"
---
# <a name="git-and-github-essentials-for-docs"></a>Bases de Git et GitHub pour le contenu Docs

## <a name="overview"></a>Vue d'ensemble

En tant que contributeur au contenu de Docs, vous interagissez avec divers outils et processus. Vous travaillez en parallèle avec d’autres contributeurs sur le même projet, peut-être exactement le même contenu, voire en même temps. Tout cela est possible avec les logiciels Git et GitHub.

Git est un système de gestion de versions open source. Il facilite ce type de collaboration sur les projets avec une *gestion distribuée des versions* des fichiers qui résident dans les *dépôts*. En substance, Git permet d’intégrer des flux de travail effectués par plusieurs contributeurs au fil du temps, pour un référentiel donné.

GitHub est un service d’hébergement web de référentiels Git, comme ceux utilisés pour stocker le contenu de [docs.microsoft.com](https://docs.microsoft.com). Pour un projet donné, GitHub héberge le dépôt principal, à partir duquel les contributeurs peuvent faire des copies pour leur propre travail.

## <a name="git"></a>Git

Si vous connaissez les systèmes de gestion de versions centralisés (comme Team Foundation Server, SharePoint ou Visual SourceSafe), vous remarquerez que Git a un flux de travail de contribution unique et une terminologie propre pour prendre en charge son modèle distribué. Par exemple, il n'y a pas le verrouillage de fichiers normalement associé aux opérations de verrouillage/déverrouillage. En fait, Git s’intéresse aux changements à un niveau encore plus fin, en comparant les fichiers octet par octet.

Git utilise également une structure hiérarchisée pour stocker et gérer le contenu d’un projet :

- *Référentiel* : Ou *dépôt*, il s’agit de l’unité de stockage la plus haute. Un référentiel contient une ou plusieurs branches.
- *Branche* : Unité de stockage qui contient les fichiers et dossiers qui composent le jeu de contenu d’un projet. Les branches servent à séparer les flux de travail (généralement appelés « versions »). Les contributions sont toujours apportées et limitées à une branche spécifique. Tous les dépôts contiennent une branche par défaut (la branche « principale ») et une ou plusieurs branches destinées à être à nouveau fusionnées avec la branche principale. La branche principale sert de version actuelle et de « seule source de vérité » pour le projet. Il s’agit du parent à partir duquel toutes les autres branches dans le dépôt sont créées.

Les contributeurs interagissent avec Git pour mettre à jour et manipuler des dépôts au niveau local et au niveau de GitHub :

- Localement au moyen d’outils tels que la console Git Bash, qui prend en charge les commandes Git pour la gestion des dépôts locaux et la communication avec les dépôts GitHub.
- Par l’intermédiaire de [www.github.com](https://www.github.com), qui intègre Git pour gérer le rapprochement des contributions qui reviennent vers le dépôt principal.

## <a name="github"></a>GitHub

> [!NOTE]
> Même si les instructions de Docs sont basées sur l’utilisation de GitHub, certaines équipes utilisent Visual Studio Team Services pour héberger les dépôts Git. Le client Visual Studio Team Explorer fournit une interface graphique utilisateur permettant d’interagir avec les dépôts Team Services, comme alternative à l’utilisation des commandes Git en ligne de commande.
> </br>
> De plus, nombre des instructions ci-dessous ont été élaborées pour servir de bonnes pratiques sur la base d’années d’expérience dans l’hébergement de contenu de service Azure dans GitHub. Elles peuvent être requises dans certains dépôts Docs.

Tous les flux de travail commencent et se terminent au niveau GitHub, où est stocké le dépôt principal de tout projet Docs. Les contributeurs créent des copies pour leur propre utilisation, qui sont réparties sur plusieurs ordinateurs. Elles sont finalement réintégrées plus tard dans le dépôt GitHub principal du projet.

### <a name="directory-organization"></a>Organisation des répertoires

Comme évoqué précédemment, une branche de projet par défaut/principale sert de version actuelle du contenu pour le projet. Le contenu de la branche principale (et les branches à partir de celle-ci) est approximativement aligné sur l’organisation des articles dans les pages Docs correspondantes. Les sous-répertoires sont utilisés pour la séparation du contenu similaire (comme les services), du contenu multimédia (comme les fichiers image) et les fichiers « include » qui permettent la réutilisation du contenu.

Vous trouverez généralement un répertoire `articles` principal à la racine du dépôt. Il contient un ensemble de sous-répertoires. Les articles des sous-répertoires sont au format Markdown, avec l’extension *.md*. Certains dépôts qui prennent en charge plusieurs services utilisent un sous-répertoire `/articles` générique, comme le dépôt [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs). D’autres peuvent utiliser un nom propre au service, comme le dépôt [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs), qui utilise `/IntuneDocs`.

Au sein de la racine de ce répertoire, vous pouvez trouver des articles généraux qui se rapportent au service ou produit global. Généralement, vous trouverez une autre série de sous-répertoires, qui correspondent aux fonctionnalités/services ou à des scénarios courants. Par exemple, les articles Azure « machine virtuelle » se trouvent dans le sous-répertoire `/virtual-machines` et les articles Intune « comprendre et explorer » se trouvent dans le sous-répertoire `/understand-explore`.

### <a name="media-subdirectory"></a>Sous-répertoire multimédia

Chaque répertoire d’articles contient un sous-répertoire `/media` pour les fichiers multimédias associés. Ces fichiers incluent des images utilisées par des articles avec des références d’images.

### <a name="includes-subdirectory"></a>Sous-répertoire d'includes

Chaque fois que du contenu réutilisable est partagé entre plusieurs articles, il est placé dans un sous-répertoire `/includes` du répertoire `articles` principal. Dans un fichier Markdown qui utilise le fichier include, une extension Markdown include correspondante est placée là où le fichier include doit être référencé.

Voir [Guide d'utilisation de Markdown : Includes](how-to-write-use-markdown.md#include-files) pour plus de conseils.

### <a name="markdown-file-template"></a>Modèle de fichier Markdown

Par souci pratique, le répertoire racine de chaque dépôt contient généralement un fichier modèle Markdown appelé `template.md`. Vous pouvez l’utiliser comme « fichier de démarrage » si vous devez créer un article et l’envoyer au dépôt. Ce fichier contient :

- Un **en-tête de métadonnées** en haut du fichier, délimité par deux lignes constituées de 3 traits d’union. Il contient les différentes balises utilisées pour le suivi des informations relatives à l’article. Les métadonnées d’articles activent certaines fonctionnalités, telles que l’attribution de l’auteur, l’attribution du contributeur, les vues miniatures et les descriptions des articles. Elles comprennent aussi les optimisations du référencement d’un site auprès d’un moteur de recherche, ainsi que la création de rapports sur les processus utilisés par Microsoft pour évaluer les performances du contenu. Les métadonnées sont donc très importantes !
- Une **section des métadonnées** qui décrit les balises et les valeurs des métadonnées. Si vous ne connaissez pas les valeurs à utiliser pour la section des métadonnées, vous pouvez la laisser vide ou insérer un commentaire commençant par un hashtag (#). Il sera révisé ou complété par le réviseur de la demande de tirage du dépôt.
- Plusieurs **exemples d’utilisation de fichiers Markdown** pour mettre en forme les éléments d’un article.
- Des **instructions générales sur l’utilisation des extensions Markdown**, qui peuvent être utilisées pour différents types d’alertes.
- Des exemples **d’intégration de la vidéo** à l’aide d’un iframe.
- Des **instructions générales sur l’utilisation des extensions docs.microsoft.com**, qui peuvent être utilisées pour des contrôles spéciaux, tels que des boutons ou des sélecteurs.

## <a name="pull-requests"></a>Requêtes de tirage (Pull)

Une *demande de tirage (pull request)* offre un moyen pratique à un contributeur de proposer un ensemble de modifications à appliquer à la branche par défaut. Les modifications (aussi appelées *validations*) sont stockées dans la branche d’un contributeur, ce qui permet à GitHub de commencer par modéliser l’impact de leur *fusion* dans la branche par défaut. Une requête de tirage sert également de mécanisme pour fournir au contributeur des commentaires lors d'un processus de génération/validation, par l'examinateur des requêtes de tirage, pour résoudre les éventuels problèmes ou questions avant la fusion des modifications avec la branche par défaut.

Il existe deux méthodes de contribution par demande de tirage, selon la taille des modifications suggérées. Nous aborderons tout cela en détail plus tard, dans la section [Flux de travail de GitHub](how-to-write-workflows-major.md) de ce guide.

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
