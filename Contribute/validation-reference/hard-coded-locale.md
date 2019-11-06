---
title: hard-coded-locale
description: Explication et résolution du problème de génération Docs hard-coded-locale.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/18/2019
ms.prod: non-product-specific
ms.openlocfilehash: 1ab511398cbd622906ccb0a67e2b24968ee29374
ms.sourcegitcommit: 55624c641bea5367bcfa08655c085bc950e8beae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166829"
---
# <a name="hard-coded-locale"></a>hard-coded-locale

> [!IMPORTANT]
> Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels. **Elle va devenir un « Avertissement » le 20/12/2019**.

## <a name="suggestion"></a>Suggestion

`Link '{URL}' contains locale code '{code}'. For localizability, remove '{code}' from links to most Microsoft sites.`

Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft. Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit. Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.

Les sites suivants sont dans la portée de cette validation :

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com (à l’exception de social.msdn.com, qui doit avoir des paramètres régionaux pour être sûr qu’il est lié au forum approprié)
- technet.microsoft.com

## <a name="resolution"></a>Résolution

Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft. Voici un exemple.

Avant :

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Après :

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

> [!TIP]
> L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft. Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`. Pour exécuter le script :
>
> 1. Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.
> 1. Appuyez sur Alt+M pour ouvrir le menu de Markdown.
> 1. Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
