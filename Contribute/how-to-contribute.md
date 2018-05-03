---
title: Marche à suivre pour contribuer à docs.microsoft.com
description: Cet article décrit les différentes façons dont vous pouvez contribuer au contenu de docs.microsoft.com.
author: billwagner
ms.author: wiwagn
manager: wpickett
ms.date: 01/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: bc6f9c314eda5f0d950da049374a7a157f16782a
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="how-to-contribute-to-docsmicrosoftcom"></a>Marche à suivre pour contribuer à docs.microsoft.com

Il existe plusieurs façons de contribuer à l’amélioration du contenu proposé sur [docs.microsoft.com](https://docs.microsoft.com) :

- Vous pouvez [signaler des problèmes](#create-issues) pour recommander de nouveaux articles, ou améliorer des articles existants.
- Vous pouvez [modifier rapidement](#quick-edits) des articles pour apporter des modifications mineures dans l’éditeur en ligne GitHub.
- Vous pouvez [vérifier les brouillons de nouveaux articles](#review-new-articles) pour garantir la qualité et l’exactitude des informations techniques.
- Vous pouvez [créer de nouveaux articles](#create-new-articles) pour les différentes rubriques dont vous souhaitez enrichir le contenu.
- Vous pouvez [mettre à jour](#update-samples) ou [créer](#create-samples) des exemples afin d’améliorer le code et renforcer ainsi les concepts importants.

Dans cet article, vous découvrirez les différentes façons de collaborer et apprendrez à effectuer chacune de ces tâches, tout en bénéficiant de liens vers de plus amples informations sur ces tâches.

Nos référentiels publics sont hébergés sur [GitHub](https://wwww.GitHub.com).  Vous devez créer un compte sur GitHub pour participer à nos référentiels de documentation.

Vous aurez également besoin d’un éditeur de texte pour mettre à jour les documents. Nous vous conseillons d’utiliser [Visual Studio Code](https://www.visualstudio.com/code). Vous devez posséder des connaissances de base sur la syntaxe [Markdown](https://daringfireball.net/projects/markdown/syntax).

Si vous ajoutez ou modifiez des exemples, vous aurez besoin d’un environnement de développement. Nous vous recommandons [Visual Studio](https://www.visualstudio.com) sur PC et Mac, ou [Visual Studio Code](https://www.visualstudio.com/code) sur toutes les plateformes.

## <a name="create-issues"></a>Signaler des problèmes

Si vous trouvez des omissions ou des imprécisions dans un article, signalez un problème concernant cet article. Le moyen le plus simple de trouver le bon emplacement consiste à cliquer sur le bouton « Modifier » dans votre navigateur pour accéder à la source de l’article dans le référentiel GitHub public correspondant. De là, vous pouvez récupérer l’URL de la source de l’article à partir de votre barre d’adresse. Cliquez sur « Create Issue » (Signaler un problème) pour signaler un problème concernant l’article.

> [!NOTE]
> Si vous détectez des problèmes que vous pouvez résoudre par de petites modifications, notamment les fautes de frappe ou de grammaire, vous pouvez gagner du temps et nous [envoyer le correctif](#quick-edits) en utilisant le navigateur pour modifier la source.

La plupart de nos référentiels publics contiennent des modèles de nouveaux problèmes qui vous guideront pour fournir les informations nécessaires à la résolution du problème.

Vous pouvez également signaler de nouveaux problèmes si vous ne trouvez pas les informations souhaitées. Le processus est identique : vous signalez un nouveau problème sur un des référentiels de documents publics. Dites-nous ce que vous recherchiez, ce que vous vouliez faire, et pourquoi les articles que vous avez trouvés n’ont pas répondu à vos attentes.

## <a name="review-new-articles"></a>Vérifier les nouveaux articles

Si vous travaillez sur un nouveau logiciel (éventuellement en version CTP ou bêta), nous sommes probablement en train de préparer les documents tandis que vous explorez la technologie. Vous trouverez les documents en cours de préparation dans nos référentiels publics. N’hésitez pas à nous faire part de vos commentaires pour nous permettre d’améliorer nos documents avant leur publication.

Les nouveaux articles sont examinés de façon publique par le biais du processus de [flux GitHub](https://guides.github.com/introduction/flow/). Parcourez l’un de nos référentiels de documents pour consulter les demandes de tirage (PR) en cours. Vos commentaires et révisions concernant ces demandes de tirage sont les bienvenus. Vous nous aidez ainsi à améliorer le contenu dès notre première version, au lieu d’attendre les commentaires une fois le document en ligne.

Nous recherchons des moyens d’améliorer la précision technique, la clarté des descriptions et la grammaire.

## <a name="quick-edits"></a>Modifications rapides

Les modifications rapides permettent d’appliquer de petits correctifs à l’aide de l’éditeur de type navigateur. Si vous trouvez de petites fautes d’orthographe ou de grammaire ou des API mal orthographiées, vous pouvez effectuer la modification et soumettre une demande de tirage sans signaler un nouveau problème.

Dans n’importe quel article, cliquez sur le bouton « Modifier » (généralement en haut à droite de la page), apportez vos modifications, puis cliquez sur « Submit PR » (Envoyer PR) en bas de la page. Nous allons examiner la demande de tirage puis la fusionner, comme nous le faisons chaque jour.

## <a name="create-new-articles"></a>Créer de nouveaux articles

Si certains sujets vous passionnent et que vous souhaitez les partager avec d’autres personnes, vous pouvez créer des articles et soumettre une demande de tirage.

Nous savons que la création de nouveaux articles prend du temps et c’est pourquoi nous apprécions votre travail et vos contributions. Nous tenons à être impliqués suffisamment tôt dans votre processus afin de s’assurer que vous suivez bien nos instructions et notre style. Nous recommandons de procéder comme suit :

1. [Signalez un problème](#create-issues) en décrivant les informations manquantes et votre solution pour y remédier.
1. Commentez le problème en nous indiquant que vous souhaitez le corriger, puis soumettez un plan et un résumé de l’article.
1. Nous y répondrons en soumettant des suggestions. Nos réponses peuvent inclure des liens vers des articles connexes, des demandes pour obtenir autres exemples ou plus d’informations sur le plan de l’article.
1. Une fois que nous nous sommes mis d’accord sur le plan, dupliquez le référentiel et commencez à travailler.
1. Dès le début du processus, ouvrez une demande de tirage en ajoutant « [WIP] » (travail en cours) au début du titre.
1. Un des contributeurs modérateurs vous fournira ses premiers commentaires.
1. Poursuivez votre travail, en @-mention la personne qui a examiné votre première ébauche lorsque vous souhaitez obtenir une nouvelle évaluation.
1. Supprimez la mention « [WIP] » lorsque vous êtes prêt pour l’examen final.
1. Répondre aux commentaires
1. Les contributeurs modérateurs fusionneront votre demande de tirage.

Il existe quelques points intéressants à développer dans cette liste. En règle générale, nous suivons le processus du [flux GitHub](https://guides.github.com/introduction/flow/) pour examiner le contenu le plut tôt possible. De cette façon, nous nous mettons d’accord sur la place d’un article dans la table des matières, l’utilité de ce nouvel article pour le lecteur, et la portée des exemples que vous allez créer. Nous pouvons ainsi apporter toutes les modifications nécessaires le plus tôt possible, pour vous éviter de travailler sur un contenu qui sera finalement obsolète.

## <a name="update-samples"></a>Mettre à jour les exemples

Certains exemples ont peut-être créés il y a plusieurs versions, à l’aide de méthodes qui ne sont plus recommandées. Vous pouvez nous aider à mettre à jour ces exemples. Peut-être estimez-vous sinon qu’une simple modification du nom de la variable pourrait améliorer la clarté d’une explication.

L’exemple de code affiché avec chaque article fait partie de programmes créés et souvent testés dans notre système CI.

Pour effectuer de petites mises à jour, recherchez la source dans le référentiel approprié, modifiez le code dans le navigateur puis soumettez une demande de tirage. Notre système CI intégrera les modifications, puis nous fusionnerons la demande de tirage une fois terminée.

Pour apporter des modifications à une plus grande échelle, dupliquez le référentiel et effectuez vos modifications dans votre environnement de développement favori. Veillez à inclure quelques tests pour vous assurer que vos modifications fonctionnent comme prévu. Soumettez une demande de tirage afin que nous l’examinions.

Chaque fois que vous modifiez du code, respectez les conventions de code existantes pour l’exemple de code en question. Les normes de codage de nos référentiels d’exemples reflèteront celles des équipes produit correspondantes. Consultez les instructions spécifiques à chaque référentiel.

> [!NOTE]
> Nous nous efforçons de suivre ces consignes nous-mêmes. Certains exemples sont antérieurs à nos normes actuelles et n’ont pas encore été mis à jour. Nous travaillons actuellement pour faire en sorte que tous les exemples de code en cours d’exécution proviennent d’exemples fonctionnels et testés.

## <a name="create-samples"></a>Créer des exemples

Vous pouvez également créer de nouveaux exemples qui illustrent des scénarios ou des concepts. Chaque exemple doit être accompagné d’un article qui présente les informations clés.

Si votre nouvel exemple complète un article existant, ajoutez une référence à cet exemple dans l’article. Sinon, vous pouvez collaborer avec nous pour [rédiger l’article](#create-new-articles) qui accompagnera l’exemple.

Dans tous les cas, notre exemple de code respecte les conventions de codage utilisées par les équipes produit connexes. La seule exception concerne le fait que nous sommes susceptibles d’utiliser des variables explicites plutôt que des variables implicites (déclarées avec `var`) par souci de clarté lorsque ces déclarations sont incluses dans l’article.

Suivez le processus d’exemple décrit dans la section précédente consacrée aux [nouveaux articles](#create-new-articles) pour nous permettre d’examiner le code dès le début du processus de développement.
