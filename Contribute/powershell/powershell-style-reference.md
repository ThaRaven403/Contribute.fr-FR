---
title: Guide spécifique pour l’écriture d’informations de référence sur les applets de commande
description: Cet article fournit des règles spécifiques pour la mise en forme des exemples de code PowerShell. Cela s’applique aux articles conceptuels avec des exemples ainsi qu’aux informations de référence sur les applets de commande.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 793a3c02ae0edf192416ae514585d5161e8c1f98
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290285"
---
# <a name="updating-reference-articles"></a>Mise à jour des articles de référence

Les articles de référence sur les applets de commande ont une structure spécifique. Cette structure est définie par [PlatyPS][].
PlatyPS est l’outil que nous utilisons pour générer l’aide sur les applets de commande pour les modules PowerShell. PlatyPS crée le fichier Markdown de base pour une applet de commande. Une fois les fichiers Markdown modifiés, PlatyPS est utilisé pour créer les fichiers d’aide MAML utilisés par l’applet de commande `Get-Help`.

PlatyPS un schéma codé en dur pour les informations de référence des applets de commande qui sont écrites dans le code. Le document [platyPS.schema.md][] décrit cette structure. Les violations du schéma entraînent des erreurs de génération, qui doivent être corrigées avant que nous puissions accepter votre contribution.

## <a name="general-guidelines"></a>Recommandations générales

- Ne supprimez aucune des structures d’en-tête. PlatyPS attend un ensemble spécifique d’en-têtes.
- Les en-têtes **Input type** et **Output type** doivent avoir un type. Si l’applet de commande ne prend pas d’entrée ou retourne une valeur, utilisez la valeur « None ».
- Les blocs de code délimités sont autorisés uniquement dans la section [Examples](#format-for-examples).
- Les étendues de code inline peuvent être utilisées dans n’importe quel paragraphe.

## <a name="formatting-about_-files"></a>Mise en forme des fichiers About_

Les fichiers `About_*` sont désormais traités par [Pandoc][] et non plus par PlatyPS. Les fichiers `About_*` sont mis en forme de façon à obtenir la meilleure compatibilité avec toutes les versions de PowerShell et avec les outils de publication.
Ne pas modifiez la mise en forme des fichiers `about_*` sans en parler à une personne responsable du dépôt.

Instructions de mise en forme de base :

- Limitez les lignes à 80 caractères
- Les blocs de code, les citations et les tableaux sont limités à 76 caractères, car Pandoc les indente de quatre espaces lors de la conversion
- Les tableaux doivent tenir dans 76 caractères
  - Renvoyez manuellement à la ligne le contenu des cellules sur plusieurs lignes
  - Utilisez des caractères `|` d’ouverture et de fermeture sur chaque ligne
  - Consultez un exemple fonctionnel dans [about_Comparison_Operators][about-example]
- Lors de l’utilisation des caractères spéciaux `\`, `$`, `` ` `` et `<` de Pandoc
  - dans un en-tête, placez ces caractères en échappement en utilisant un caractère `\` au début
  - Dans un paragraphe, ces caractères doivent être placés dans des étendues de code. Par exemple :

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a>Format pour les exemples

Dans le schéma PlatyPS, l’en-tête **EXAMPLES** est un en-tête H2, et chaque exemple est un en-tête H3.

Dans un exemple, le schéma n’autorise pas la séparation des blocs de code par des paragraphes. Le schéma valide est :

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

Numérotez chaque exemple et ajoutez un titre court.

Par exemple :

~~~markdown
### Example 1: Get cmdlets, functions, and aliases

This example gets the PowerShell cmdlets, functions, and aliases that are installed on the
computer.

```powershell
Get-Command
```
~~~


[PlatyPS]: https://github.com/powershell/platyps
[platyPS.schema.md]: https://github.com/PowerShell/platyPS/blob/master/platyPS.schema.md
[issue1806]: https://github.com/PowerShell/PowerShell-Docs/issues/1806
[about-example]: https://github.com/MicrosoftDocs/PowerShell-Docs/blob/staging/reference/6/Microsoft.PowerShell.Core/About/about_Comparison_Operators.md
[Pandoc]: https://pandoc.org