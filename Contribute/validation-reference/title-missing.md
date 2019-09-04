---
title: title-missing
description: Explication et résolution du problème de génération de documents title-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/6/2019
ms.prod: non-product-specific
ms.openlocfilehash: cfe942be4285bb22f5fa08fa882077ea790fd2c4
ms.sourcegitcommit: dd751d0cb5b11f81a64ef62f3c83fd17cc5f0541
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2019
ms.locfileid: "70236570"
---
# <a name="title-missing"></a>title-missing

## <a name="warning"></a>Avertissement

`Missing attribute: title. Add a title string (19 - 59 characters) to show in search engine results.`

## <a name="resolution"></a>Résolution

Ajoutez une chaîne de texte à afficher dans les résultats de la recherche. En règle générale, les titres doivent comprendre entre 19 et 59 caractères, être distincts du H1 de l’article et inclure des noms de produit pertinents. Vous ne devez pas inclure « | Microsoft Docs » dans votre titre, car c’est automatiquement ajouté par Docs et ignoré si vous l’ajoutez explicitement. Si vous souhaitez ajouter un autre nom de produit, comme «  - Azure », à tous les titres d’un ensemble de contenu, définissez la valeur des métadonnées `titleSuffix` globalement ou pour un dossier.

Vous pouvez obtenir un aperçu de votre titre dans Google sur [https://moz.com/learn/seo/title-tag](https://moz.com/learn/seo/title-tag).

Si vous êtes un employé Microsoft, consultez [Principes de base de SEO](https://review.docs.microsoft.com/en-us/help/contribute/contribute-how-to-write-seo-basics?branch=master) dans le Guide du contributeur interne pour plus d’informations sur des titres pertinents et l’optimisation du référencement d'un site auprès d'un moteur de recherche (SEO).

[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
