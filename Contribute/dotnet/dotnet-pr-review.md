---
title: Processus de révision des demandes de tirage (pull request) pour les documents .NET
description: Les webhooks de fusion des demandes de tirage ne sont pas activés sur les documents .NET. Cet article décrit le processus des demandes de tirage pour ces référentiels
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 01/04/2019
ms.openlocfilehash: 80877a93dc410454c939bcd5be5588861682ed11
ms.sourcegitcommit: 5ef2dc72e2ff8bddf873415a3f4b816eb16029dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/03/2020
ms.locfileid: "80625117"
---
# <a name="pull-request-review-process-for-the-net-docs-repositories"></a>Processus de révisions des demandes de tirage pour les référentiels de documents .NET

Beaucoup de référentiels n’ont pas les webhooks de fusion des demandes de tirage activés, ce qui fusionne automatiquement les demandes de tirage mineures. Cet article décrit le processus de révision des demandes de tirage dans ce cas de figure. Le processus de révision des demandes de tirage a été conçu dans les objectifs suivants :

1. publier du contenu de haute qualité produit par notre équipe, les membres de l’équipe produit et les membres de la communauté ;
1. faire parvenir des commentaires opportuns et exploitables aux auteurs, de manière cohérente ;
1. faciliter la discussion entre les auteurs et les réviseurs.

Les processus continueront d’évoluer au fil des innovations produites par les équipes et au fur et à mesure du développement de la plateforme.

## <a name="reviewers"></a>Réviseurs

Un des membres de l’équipe chargée du contenu vérifie chaque demande de tirage. Les membres de l’équipe chargée du contenu peuvent demander une validation de l’exactitude technique aux membres de l’équipe responsable du produit. L’équipe chargée du contenu utilise la fonctionnalité de responsabilité du code de GitHub pour demander automatiquement des révisions à ses membres. Dans le cadre de ce processus, un réviseur a la possibilité d’affecter d’autres collaborateurs à la vérification des demandes de tirage internes. Les demandes de validation des membres de l’équipe apparaissent dans la même file d’attente que celles des membres de la communauté.

Les membres de la communauté peuvent eux aussi vérifier les demandes de tirage et faire des commentaires. Toutefois, au moins un membre de l’équipe principale chargée du contenu doit approuver chacune des demandes de tirage avant la fusion.

## <a name="review-process"></a>Processus de révision

Les révisions suivent l’un des trois processus suivants, en fonction de la demande de tirage :

- **Petites demandes de tirage** : les petites demandes de tirage corrigent un seul bogue : fautes de frappe, liens rompus, petites modifications de code ou autres changements similaires.
- **Contributions majeures** : les contributions majeures correspondent à des modifications significatives apportées à un article existant, à des créations d’articles ou à des modifications apportées à plusieurs articles.
- **Travail en cours** : les auteurs peuvent demander une révision en cours de route en ouvrant une demande de tirage comportant la balise « [TEC] » dans le titre. La balise « TEC » est l’abréviation de « Travail en cours ». 

Le traitement utilisé par le robot CLA (Contributor License Agreement) est une bonne indication de la distinction entre « petites » et « grandes » contributions. Les demandes de tirage qui ne réclament pas de signature du contrat CLA sont probablement « petites ». Les demandes de tirage qui exigent le contrat CLA ont de bonnes chances d’être « grandes ».

### <a name="small-prs"></a>Petites demandes de tirage

Les modifications des petites demandes de tirage sont révisées dans un souci d’exactitude et vérifiées à l’aide de la build sur le site de révision. Du fait de leur taille réduite, ces demandes de tirage ne déclenchent pas de révision de la totalité de l’article. 

Il peut arriver que les réviseurs remarquent d’autres petites modifications susceptibles d’améliorer l’article. Si ces modifications sont également limitées, suggérez-les en commentaires de révision. Si les modifications proposées sont de nature à déclencher une révision de plus grande envergure, signalez le problème et réglez-le plus tard. 

### <a name="larger-changes"></a>Modifications majeures

Les grandes demandes de tirage font l’objet d’une révision plus poussée. Les éléments suivants sont vérifiés :

- La demande de tirage doit comporter un exemple de code, dans la source et sous forme de fichier .zip téléchargeable.
- L’exemple de code se compile et s’exécute correctement.
- L’article explique clairement les objectifs au lecteur, et ces objectifs sont atteints.
- Cet article respecte les [consignes de style et de grammaire](dotnet-style-guide.md) et nos [directives sur la voix et le ton](dotnet-voice-tone.md).
- Tous les liens doivent se résoudre correctement.

Les membres de l’équipe chargée du contenu examineront la demande de tirage et soumettront la révision, accompagnée de commentaires. Si seuls des changements mineurs sont demandés, les membres de l’équipe ont la possibilité d’« approuver » la demande de tirage avec les commentaires. L’auteur pourra ensuite traiter les commentaires et fusionner la demande de tirage. La plupart des révisions impliquent des modifications ; une fois celles-ci effectuées, le réviseur effectuera une nouvelle vérification.

Si les modifications nécessitent une validation technique, le réviseur de l’équipe chargée du contenu demandera une vérification au membre de l’équipe produit concerné.

### <a name="review-wip-pull-requests"></a>Vérifier les demandes de tirage « TEC »

Dans certains cas, les nouveaux auteurs souhaitent recevoir des commentaires plus tôt dans le processus. Ils peuvent ouvrir une demande de tirage en ajoutant l’étiquette « [TEC] » dans le titre. Ils peuvent demander une révision anticipée en commentaires.

Ces évaluations anticipées ne sont pas aussi complètes qu’une révision totale de demande de tirage. L’équipe chargée du contenu fera des commentaires, mais n’utilisera pas la fonctionnalité de révision de GitHub pour « approuver » ou « demander des modifications ». Ces révisions anticipées se concentrent sur la structure de l’article : le plan, le contenu général et les exemples. Ces révisions ne comportent pas de vérification approfondie de la grammaire et des liens.

## <a name="respond-to-reviews"></a>Répondre aux révisions

L’auteur met à jour la demande de tirage pour répondre aux commentaires, en les marquant de la réaction « +1 » pour indiquer qu’ils ont été traités. Si l’auteur n’est pas d’accord avec le commentaire, ou le traite différemment, il ajoute un commentaire expliquant la modification effectuée.

L’auteur @-mentions le réviseur d’origine dans un commentaire pour demander une nouvelle révision. 

## <a name="response-time-expectations"></a>Temps de réponse attendus

Les membres de l’équipe chargée du contenu vérifient généralement les nouvelles demandes de tirage en moins de deux jours ouvrés. Si la révision prend plus de temps, un des membres de l’équipe ajoutera un commentaire pour accuser réception de la demande de tirage et définir les attentes.

Après soumission de la révision, les auteurs doivent s’efforcer de répondre aux commentaires sous une semaine maximum. Les bénévoles ne seront peut-être pas en mesure de répondre à ces attentes en raison d’autres engagements. Dans ce cas, les membres de l’équipe demandent si l’auteur de la communauté mettra à jour la demande de tirage. Si ce n’est pas le cas, le membre de l’équipe met à jour et fusionne la demande de tirage à sa place.
