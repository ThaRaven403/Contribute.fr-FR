---
title: Titres Markdown
description: Décrit la configuration requise pour les titres Markdown.
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084486"
---
# <a name="markdown-headings"></a>Titres Markdown

Les exigences de validation suivantes s’appliquent aux titres dans les fichiers Markdown OPS.

## <a name="h1"></a>H1

`H1` désigne le premier titre dans un fichier Markdown. Lors de la publication sur docs.microsoft.com, le titre H1 s’affiche en haut de la page dans une grande taille de police.

Un titre H1 est créé en commençant une ligne par un seul signe dièse (`#`) suivi d’un espace, puis du texte du titre. Par exemple, le titre H1 de cet article est :

```md
# Markdown headings
```

Les règles suivantes s’appliquent aux titres H1 :

- Un titre H1 doit être présent dans le fichier.
- Il ne peut y avoir qu’un seul titre H1.
- Le titre H1 doit avoir un contenu.

  ```markdown
  # 
  This is not allowed.
  ```
- Il doit y avoir un espace entre le signe `#` et le contenu de le titre H1. Un titre H1 sans espace ne s’affiche pas comme un titre sur la page publiée.

  ```markdown
  #This looks bad on the site.
  ```
- Le titre H1 doit être le premier contenu du fichier après l’en-tête de métadonnées YML. Aucun contenu, comme du texte ou des images, n’est autorisé entre la fin de l’en-tête YML et le titre H1.

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- L’élément HTML des titres de premier niveau, `<h1>`, ne doit pas être utilisé. Utilisez la syntaxe Markdown (`# `).
- H1 ne doit pas contenir plus de 100 caractères. Il s’agit d’une règles de style.

## <a name="h2---h6"></a>H2 - H6

Les titres H2 (`## `) à H6 (`###### `) sont autorisés dans OPS. Utilisez les en-têtes Markdown, et non pas du code HTML (`<h2>` - `<h6>`), pour créer des titres.
