---
title: Mises à jour des métadonnées - Docs Authoring Pack
description: Découvrez comment mettre à jour les métadonnées à partir de l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 391ea6c523d1f1b82b21883cea5e3428e86633e9
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336632"
---
# <a name="update-metadata"></a>Mettre à jour les métadonnées

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

Dans un fichier Markdown ( *\*.md*), deux éléments de menu contextuel sont propres aux métadonnées. Quand vous cliquez avec le bouton droit n’importe où dans l’éditeur de texte, vous voyez quelque chose similaire aux éléments de menu suivants :

:::image type="content" source="media/update-metadata-menu.png" alt-text="Menu contextuel de mise à jour des métadonnées":::

## <a name="update-msdate-metadata-value"></a>Mettre à jour la valeur de métadonnées `ms.date`

La sélection de l’option **Update `ms.date` Metadata Value** (Mettre à jour la valeur de métadonnées `ms.date`) permet de définir la valeur `ms.date` actuelle des fichiers Markdown sur la date du jour. Si le document n’a pas de champ de métadonnées `ms.date`, aucune action n’est effectuée.

## <a name="update-implicit-metadata-values"></a>Mettre à jour les valeurs de métadonnées implicites

La sélection de l’option **Update implicit metadata values** (Mettre à jour les valeurs de métadonnées implicites) permet de rechercher et de remplacer toutes les valeurs de métadonnées possibles qui peuvent être spécifiées implicitement. Les valeurs de métadonnées sont spécifiées implicitement dans le fichier *docfx.json*, sous le nœud `build/fileMetadata`. Chaque paire clé-valeur du nœud `fileMetadata` représente les valeurs par défaut des métadonnées. Par exemple, un fichier Markdown dans le répertoire *top-level/sub-folder* qui omet la valeur de métadonnées `ms.author` peut spécifier implicitement une valeur par défaut à utiliser dans le nœud `fileMetadata`.

```json
{
    "build": {
        "fileMetadata": {
            "ms.author": {
                "top-level/sub-folder/**/**.md": "dapine"
            }
        }
    }
}
```

Dans ce cas, tous les fichiers Markdown prennent implicitement la valeur de métadonnées `ms.author: dapine`. La fonctionnalité agit sur ces paramètres implicites qui se trouvent dans le fichier *docfx.json*. Si un fichier Markdown contient des métadonnées dont les valeurs sont explicitement définies sur une valeur autre que les valeurs implicites, elles sont substituées.

Considérez les métadonnées de fichier Markdown suivantes, ce fichier Markdown se trouvant dans **top-level/sub-folder/includes/example.md** :

```markdown
---
ms.author: someone-else
---

# Content
```

Si l’option **Update implicit metadata values** (Mettre à jour les valeurs de métadonnées implicites) était exécutée sur ce fichier, avec le contenu supposé de *docfx.json* ci-dessus, la valeur de métadonnées deviendrait `ms.author: dapine`.

```markdown
---
ms.author: dapine
---

# Content
```

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démonstration de la mise à jour des métadonnées](media/update-metadata.gif)](media/update-metadata.gif#lightbox)
