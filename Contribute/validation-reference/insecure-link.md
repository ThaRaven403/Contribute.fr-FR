---
title: insecure-link
description: Explication et résolution du problème de génération Docs insecure-link
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 10/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4735d47cdf2029d2c613c9b333a393c7d978c58e
ms.sourcegitcommit: 423d9b8145a11426c91f45510b2d77319838eb27
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74528841"
---
# <a name="insecure-link"></a>insecure-link

> [!IMPORTANT]
> Initialement, cette règle était activée en tant que « Suggestion » pour donner aux équipes en charge du contenu le temps de juger l’impact et de développer un plan de nettoyage de leurs référentiels. **Elle va devenir un « Avertissement » le 20/12/2019**.

## <a name="suggestion"></a>Suggestion

`Link '{URL}' is insecure. Links to Microsoft sites must use 'https' instead of 'http'.`

Ce message signifie que vous avez utilisé un lien Markdown explicite avec `http` ou que vous avez utilisé une URL brute, comme `www.microsoft.com`. Les URL brutes sont converties en liens non sécurisés quand elles sont publiées sur Docs ; elles ne doivent pas être utilisées.

## <a name="resolution"></a>Résolution

Changez toutes les URL vers des sites Microsoft pour qu’elles utilisent `https` au lieu de `http`.

Si votre lien est une URL brute, remplacez-le par un lien Markdown explicite commençant par `https`, comme :

```md
`[www.microsoft.com](https://www.microsoft.com)`.
```

> [!TIP]
> L’extension Docs Markdown pour VS Code comprend un script de nettoyage pour les liens Microsoft. Le script vérifie que tous les liens vers des sites Microsoft dans un dépôt commencent par `https` au lieu de `http`, et qu’ils ne contiennent pas de codes de paramètres régionaux, comme `en-us`. Pour exécuter le script :
>
> 1. Installez l’extension [Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) pour VS Code.
> 1. Appuyez sur Alt+M pour ouvrir le menu de Markdown.
> 1. Sélectionnez **Cleanup** (Nettoyage), puis **Microsoft links** (Liens Microsoft).

Dans certains cas, vous devrez certainement documenter des adresses web, telles que des noms de domaine complets, qui ne sont pas censées être des liens cliquables. Elles doivent être mises en forme en tant que code inline, comme :

```md
`www.microsoft.com:90`
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
