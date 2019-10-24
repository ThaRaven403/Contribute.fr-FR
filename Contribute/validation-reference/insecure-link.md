---
title: insecure-link
description: Explication et résolution du problème de génération Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: c22404e624ae85369d7b0b95f44e37d51f847368
ms.sourcegitcommit: ab31cbb17c64a06cab4ffb37b157fd812417a499
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2019
ms.locfileid: "72587672"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels. **Elle va devenir un « Avertissement » le 20/12/2019**.

## <a name="suggestion"></a>Suggestion

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Ce message signifie que vous avez utilisé un lien Markdown explicite avec `http` ou que vous avez utilisé une URL brute, comme `www.microsoft.com`. Les URL brutes sont converties en liens non sécurisés quand elles sont publiées sur Docs ; elles ne doivent pas être utilisées.

## <a name="resolution"></a>Résolution

Changez toutes les URL vers des sites Microsoft pour qu’elles utilisent `https` au lieu de `http`.

Si votre lien est une URL brute, remplacez-le par un lien Markdown explicite commençant par `https`.

> [!TIP]
> L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft. Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`. Pour exécuter le script :
>
> 1. Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.
> 1. Appuyez sur Alt+M pour ouvrir le menu de Markdown.
> 1. Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
