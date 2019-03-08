---
title: h1-missing
description: Explication et résolution du problème de génération Docs h1-missing.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459116"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>Avertissement

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police. Un titre H1 est créé en commençant une ligne par un signe dièse (#) suivi d’un espace, puis du texte du titre.

## <a name="resolution"></a>Résolution

Pour résoudre ce problème, ajoutez un titre H1 comme premier contenu après le bloc de métadonnées YML dans votre fichier :

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> Cette règle ne s’applique pas aux fichiers inclus. Si vous obtenez des avertissements H1 sur des fichiers inclus, vous devez plus probablement déplacer vos fichiers inclus dans un dossier `includes`. Le dossier `includes` peut être à n’importe quel niveau dans le chemin du fichier. En fonction du chemin, la génération Docs reconnaît le fichier comme fichier inclus et les validations H1 ne sont pas exécutées.

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]