---
title: ms-author-missing
description: Explication et résolution du problème de génération de documents ms-author-missing
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6b313bd6b168b913d82721607126fcd4e6255009
ms.sourcegitcommit: 57eb071bdc55ef71fa3f8ac979326c3f8fbe9c45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "72246253"
---
# <a name="ms-author-missing"></a>ms-author-missing

## <a name="warning"></a>Avertissement

`Missing attribute: ms.author. Add the current author's Microsoft alias.`

## <a name="resolution"></a>Résolution

Ajoutez l’alias Microsoft de l’auteur actuel pour `ms.author`. Notez que ce doit être le propriétaire *actuel* de l’article, pas l’auteur d’origine si l’appartenance a changé. Nous recommandons que l’auteur désigné soit un employé à plein temps ou une liste de distribution d’équipe, plutôt qu’un fournisseur à court terme. 

Si l’alias est une liste de distribution, il doit également figurer dans la liste verte `ms.author`.

Vous trouverez les valeurs valides des listes de distribution `ms.author` sur [ce site interne de Microsoft](https://docsmetadatatool.azurewebsites.net/allowlists).

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
