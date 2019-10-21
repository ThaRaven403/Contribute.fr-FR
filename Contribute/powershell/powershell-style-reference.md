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
# <a name="updating-reference-articles"></a><span data-ttu-id="dbf3e-104">Mise à jour des articles de référence</span><span class="sxs-lookup"><span data-stu-id="dbf3e-104">Updating reference articles</span></span>

<span data-ttu-id="dbf3e-105">Les articles de référence sur les applets de commande ont une structure spécifique.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-105">Cmdlet reference articles have a specific structure.</span></span> <span data-ttu-id="dbf3e-106">Cette structure est définie par [PlatyPS][].</span><span class="sxs-lookup"><span data-stu-id="dbf3e-106">This structure is defined by [PlatyPS][].</span></span>
<span data-ttu-id="dbf3e-107">PlatyPS est l’outil que nous utilisons pour générer l’aide sur les applets de commande pour les modules PowerShell.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-107">PlatyPS is the tool we use to generate cmdlet help for PowerShell modules.</span></span> <span data-ttu-id="dbf3e-108">PlatyPS crée le fichier Markdown de base pour une applet de commande.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-108">PlatyPS creates the base Markdown file for a cmdlet.</span></span> <span data-ttu-id="dbf3e-109">Une fois les fichiers Markdown modifiés, PlatyPS est utilisé pour créer les fichiers d’aide MAML utilisés par l’applet de commande `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-109">After editing the Markdown files, PlatyPS is used create the MAML help files used by the `Get-Help` cmdlet.</span></span>

<span data-ttu-id="dbf3e-110">PlatyPS un schéma codé en dur pour les informations de référence des applets de commande qui sont écrites dans le code.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-110">PlatyPS has a hard-coded schema for cmdlet reference that is written into the code.</span></span> <span data-ttu-id="dbf3e-111">Le document [platyPS.schema.md][] décrit cette structure.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-111">The [platyPS.schema.md][] document attempts to describe this structure.</span></span> <span data-ttu-id="dbf3e-112">Les violations du schéma entraînent des erreurs de génération, qui doivent être corrigées avant que nous puissions accepter votre contribution.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-112">Schema violations cause build errors that must be fixed before we can accept your contribution.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="dbf3e-113">Recommandations générales</span><span class="sxs-lookup"><span data-stu-id="dbf3e-113">General guidelines</span></span>

- <span data-ttu-id="dbf3e-114">Ne supprimez aucune des structures d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-114">Do not remove any of the header structures.</span></span> <span data-ttu-id="dbf3e-115">PlatyPS attend un ensemble spécifique d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-115">PlatyPS expects a specific set of headers.</span></span>
- <span data-ttu-id="dbf3e-116">Les en-têtes **Input type** et **Output type** doivent avoir un type.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-116">The **Input type** and **Output type** headers must have a type.</span></span> <span data-ttu-id="dbf3e-117">Si l’applet de commande ne prend pas d’entrée ou retourne une valeur, utilisez la valeur « None ».</span><span class="sxs-lookup"><span data-stu-id="dbf3e-117">If the cmdlet does not take input or return a value then use the value "None".</span></span>
- <span data-ttu-id="dbf3e-118">Les blocs de code délimités sont autorisés uniquement dans la section [Examples](#format-for-examples).</span><span class="sxs-lookup"><span data-stu-id="dbf3e-118">Fenced code blocks are only allowed in the [Examples](#format-for-examples) section.</span></span>
- <span data-ttu-id="dbf3e-119">Les étendues de code inline peuvent être utilisées dans n’importe quel paragraphe.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-119">Inline code spans can be used in any paragraph.</span></span>

## <a name="formatting-about_-files"></a><span data-ttu-id="dbf3e-120">Mise en forme des fichiers About_</span><span class="sxs-lookup"><span data-stu-id="dbf3e-120">Formatting About_ files</span></span>

<span data-ttu-id="dbf3e-121">Les fichiers `About_*` sont désormais traités par [Pandoc][] et non plus par PlatyPS.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-121">`About_*` files are now processed by [Pandoc][], instead of PlatyPS.</span></span> <span data-ttu-id="dbf3e-122">Les fichiers `About_*` sont mis en forme de façon à obtenir la meilleure compatibilité avec toutes les versions de PowerShell et avec les outils de publication.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-122">`About_*` files are formatted for the best compatibility across with all versions of PowerShell and with the publishing tools.</span></span>
<span data-ttu-id="dbf3e-123">Ne pas modifiez la mise en forme des fichiers `about_*` sans en parler à une personne responsable du dépôt.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-123">Please do not alter the formatting of `about_*` files without checking in with a repository maintainer.</span></span>

<span data-ttu-id="dbf3e-124">Instructions de mise en forme de base :</span><span class="sxs-lookup"><span data-stu-id="dbf3e-124">Basic formatting guidelines:</span></span>

- <span data-ttu-id="dbf3e-125">Limitez les lignes à 80 caractères</span><span class="sxs-lookup"><span data-stu-id="dbf3e-125">Limit lines to 80 characters</span></span>
- <span data-ttu-id="dbf3e-126">Les blocs de code, les citations et les tableaux sont limités à 76 caractères, car Pandoc les indente de quatre espaces lors de la conversion</span><span class="sxs-lookup"><span data-stu-id="dbf3e-126">Code blocks, block quotes, and tables are limited to 76 characters because Pandoc indents these by four spaces during conversion</span></span>
- <span data-ttu-id="dbf3e-127">Les tableaux doivent tenir dans 76 caractères</span><span class="sxs-lookup"><span data-stu-id="dbf3e-127">Tables need fit within 76 characters</span></span>
  - <span data-ttu-id="dbf3e-128">Renvoyez manuellement à la ligne le contenu des cellules sur plusieurs lignes</span><span class="sxs-lookup"><span data-stu-id="dbf3e-128">Manually wrap contents of cells across multiple lines</span></span>
  - <span data-ttu-id="dbf3e-129">Utilisez des caractères `|` d’ouverture et de fermeture sur chaque ligne</span><span class="sxs-lookup"><span data-stu-id="dbf3e-129">Use opening and closing `|` characters on each line</span></span>
  - <span data-ttu-id="dbf3e-130">Consultez un exemple fonctionnel dans [about_Comparison_Operators][about-example]</span><span class="sxs-lookup"><span data-stu-id="dbf3e-130">See a working example in [about_Comparison_Operators][about-example]</span></span>
- <span data-ttu-id="dbf3e-131">Lors de l’utilisation des caractères spéciaux `\`, `$`, `` ` `` et `<` de Pandoc</span><span class="sxs-lookup"><span data-stu-id="dbf3e-131">When using Pandoc's special characters `\`,`$`,`` ` ``, and `<`</span></span>
  - <span data-ttu-id="dbf3e-132">dans un en-tête, placez ces caractères en échappement en utilisant un caractère `\` au début</span><span class="sxs-lookup"><span data-stu-id="dbf3e-132">Within a header - these characters must be escaped using a leading `\` character</span></span>
  - <span data-ttu-id="dbf3e-133">Dans un paragraphe, ces caractères doivent être placés dans des étendues de code.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-133">Within a paragraph - these characters should be put into code spans.</span></span> <span data-ttu-id="dbf3e-134">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dbf3e-134">For example:</span></span>

    ~~~markdown
    ### The purpose of the \$foo variable

    The `$foo` variable is used to store ...
    ~~~

## <a name="format-for-examples"></a><span data-ttu-id="dbf3e-135">Format pour les exemples</span><span class="sxs-lookup"><span data-stu-id="dbf3e-135">Format for examples</span></span>

<span data-ttu-id="dbf3e-136">Dans le schéma PlatyPS, l’en-tête **EXAMPLES** est un en-tête H2, et chaque exemple est un en-tête H3.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-136">In the PlatyPS schema, the **EXAMPLES** header is an H2 header and each example is an H3 header.</span></span>

<span data-ttu-id="dbf3e-137">Dans un exemple, le schéma n’autorise pas la séparation des blocs de code par des paragraphes.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-137">Within an example, the schema does not allow code blocks to be separated by paragraphs.</span></span> <span data-ttu-id="dbf3e-138">Le schéma valide est :</span><span class="sxs-lookup"><span data-stu-id="dbf3e-138">The valid schema is:</span></span>

```
### Example #X title

0 or more paragraphs
1 or more code blocks
0 or more paragraphs.
```

<span data-ttu-id="dbf3e-139">Numérotez chaque exemple et ajoutez un titre court.</span><span class="sxs-lookup"><span data-stu-id="dbf3e-139">Number each example and add a brief title.</span></span>

<span data-ttu-id="dbf3e-140">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="dbf3e-140">For example:</span></span>

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