---
title: Remplacement automatique des guillemets courbes - Docs Authoring Pack
description: Découvrez comment remplacer automatiquement les guillemets courbes avec l’extension Visual Studio Code Docs Authoring Pack.
author: IEvangelist
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: dapine
ms.openlocfilehash: 048f244324d7dde540c78e6631ccb5abbed3e431
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336701"
---
# <a name="smart-quote-replacement"></a>Remplacement des guillemets courbes

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a>Récapitulatif

Les développeurs de contenu sont responsables de la création de certaines des fonctionnalités les plus avancées de la technologie et de l’intelligence modernes. Pourtant, nos outils actuels préfèrent l’utilisation de « guillemets droits » dans Markdown. À l’opposé nous trouvons naturellement les « guillemets courbes ». Les guillemets courbes sont courants avec les typographies idéales, mais ne sont pas privilégiés par Markdown et le rendu du code HTML.

Quand vous travaillez sur un document Microsoft Word, par exemple, vous avez peut-être remarqué que quand vous maintenez enfoncée la touche <kbd>Maj</kbd> et que vous tapez un <kbd>"</kbd> Microsoft Word remplace rapidement le caractère `"` par un caractère guillemet courbe équivalent `“`.

| Description        | Unicode  | Guillemet courbe | Remplacement |
|--------------------|----------|-------------|-------------|
| Guillemet double gauche  | `\u201c` | `“`         | `"`         |
| Guillemet double droit | `\u201d` | `”`         | `"`         |
| Guillemet simple gauche  | `\u2018` | `‘`         | `'`         |
| Guillemet simple droit | `\u2019` | `’`         | `'`         |

Dans un fichier Markdown ( *\*.md*), quand vous collez du texte ou que vous mettez à jour du contenu, cette fonctionnalité évalue activement le contenu et remplace automatiquement les valeurs en conséquence.

> [!NOTE]
> La fonctionnalité de remplacement des guillemets courbes remplace également d’autres caractères, tels que les caractères `©, ™, ®, •`, d’indice et d’exposant, entre autres. C’est utile lors du collage de texte à partir de documents Word.

## <a name="preferences"></a>Préférences

Cette fonctionnalité est facultative, mais prend par défaut la valeur `true`. Pour activer ou désactiver cette fonctionnalité :

1. Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).
1. Activez/désactivez le paramètre dans la section **Markdown : Replace Smart Quotes** (Markdown : Remplacer les guillemets courbes).

## <a name="in-action"></a>En action

Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité.

[![Démonstration de remplacement des guillemets courbes](media/replace-smart-quotes.gif)](media/replace-smart-quotes.gif#lightbox)
