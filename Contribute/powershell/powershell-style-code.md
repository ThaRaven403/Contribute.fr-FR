---
title: Guide spécifique pour l’écriture des exemples de scripts
description: Cet article fournit des règles spécifiques pour la mise en forme des exemples de code PowerShell. Cela s’applique aux articles conceptuels avec des exemples ainsi qu’aux informations de référence sur les applets de commande.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: f036ece21d139df0be1d677dc536023910c9d20b
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290262"
---
# <a name="formatting-code-samples"></a><span data-ttu-id="3d682-104">Mise en forme des exemples de code</span><span class="sxs-lookup"><span data-stu-id="3d682-104">Formatting code samples</span></span>

<span data-ttu-id="3d682-105">La documentation existante a utilisé plusieurs styles au fil du temps, et les règles de mise en forme ont été modifiées plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="3d682-105">The existing documentation has used multiple styles, over time, and the formatting rules have changed multiple times.</span></span> <span data-ttu-id="3d682-106">Nous essayons d’établir un style cohérent pour les blocs de code PowerShell et leur résultat dans notre documentation.</span><span class="sxs-lookup"><span data-stu-id="3d682-106">We are trying to establish a consistent style for PowerShell code blocks and output in our documentation.</span></span>

<span data-ttu-id="3d682-107">Markdown prend en charge deux styles de code différents :</span><span class="sxs-lookup"><span data-stu-id="3d682-107">Markdown supports two different code styles:</span></span>

- <span data-ttu-id="3d682-108">Étendues de code (inline) : marquées par un seul caractère d’accent grave (`` ` ``).</span><span class="sxs-lookup"><span data-stu-id="3d682-108">Code spans (inline) - marked by a single backtick (`` ` ``) character.</span></span> <span data-ttu-id="3d682-109">Utilisées à l’intérieur d’un paragraphe, plutôt que comme bloc autonome.</span><span class="sxs-lookup"><span data-stu-id="3d682-109">Used inline in a paragraph rather than as a standalone block.</span></span> <span data-ttu-id="3d682-110">Elles sont le plus souvent utilisées autour des noms des applets de commande.</span><span class="sxs-lookup"><span data-stu-id="3d682-110">Most commonly used around cmdlet names.</span></span> <span data-ttu-id="3d682-111">Consultez [Mise en forme des éléments de la syntaxe des commandes](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span><span class="sxs-lookup"><span data-stu-id="3d682-111">See [Formatting command syntax elements](powershell-style-basic-markdown.md#formatting-command-syntax-elements).</span></span>
- <span data-ttu-id="3d682-112">Blocs de code : bloc de plusieurs lignes entouré de chaînes de trois accents graves (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="3d682-112">Code blocks - a multi-line block surrounded by triple-backtick (`` ``` ``) strings.</span></span>

## <a name="using-code-blocks"></a><span data-ttu-id="3d682-113">Utilisation des blocs de code</span><span class="sxs-lookup"><span data-stu-id="3d682-113">Using code blocks</span></span>

<span data-ttu-id="3d682-114">Markdown permet l’indentation pour représenter un bloc de code, mais ce modèle peut être problématique et doit être évité.</span><span class="sxs-lookup"><span data-stu-id="3d682-114">Markdown allows for indentation to signify a code block, but this pattern can be problematic and should be avoided.</span></span> <span data-ttu-id="3d682-115">Tous les blocs de code doivent être entourés d’une délimitation de code.</span><span class="sxs-lookup"><span data-stu-id="3d682-115">All code blocks should be contained in a code fence.</span></span> <span data-ttu-id="3d682-116">Une délimitation de code est un bloc de code entouré de chaînes de trois accents graves (`` ``` ``).</span><span class="sxs-lookup"><span data-stu-id="3d682-116">A code fence is a block of code surrounded by triple-backtick (`` ``` ``) strings.</span></span> <span data-ttu-id="3d682-117">Les marqueurs de délimitation de code doivent se trouver sur leur propre ligne avant et après l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="3d682-117">The code fence markers must be on their own line before and after the code sample.</span></span> <span data-ttu-id="3d682-118">Le marqueur au début du bloc de code peut avoir une étiquette de langage facultative.</span><span class="sxs-lookup"><span data-stu-id="3d682-118">The marker at the start of the code block may have an optional language label.</span></span> <span data-ttu-id="3d682-119">Le système de publication OPS de Microsoft utilise l’étiquette de langage pour prendre en charge la fonctionnalité de mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3d682-119">Microsoft's Open Publishing System (OPS) uses the language label to support the syntax highlighting feature.</span></span>

<span data-ttu-id="3d682-120">OPS ajoute également un bouton de **Copie** qui copie le contenu du bloc de code dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="3d682-120">OPS also adds a **Copy** button that copies the contents of the code block to the clipboard.</span></span> <span data-ttu-id="3d682-121">Ceci vous permet de coller rapidement le code dans un script pour tester l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="3d682-121">This allows you to quickly paste the code into a script for testing the code example.</span></span> <span data-ttu-id="3d682-122">Cependant, tous les exemples de notre documentation ne sont pas destinés à être exécutés de cette façon.</span><span class="sxs-lookup"><span data-stu-id="3d682-122">However, not all examples in our documentation are intended to be run that way.</span></span> <span data-ttu-id="3d682-123">Certains blocs de code peuvent être la simple illustration d’un concept PowerShell ou une représentation abstraite de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3d682-123">Some code blocks may be a simple illustration of a PowerShell concept or an abstract representation of syntax.</span></span>

<span data-ttu-id="3d682-124">Deux types de blocs de code sont utilisés dans notre documentation :</span><span class="sxs-lookup"><span data-stu-id="3d682-124">There are two types code blocks used in our documentation:</span></span>

1. <span data-ttu-id="3d682-125">Exemples illustratifs</span><span class="sxs-lookup"><span data-stu-id="3d682-125">Illustrative examples</span></span>
2. <span data-ttu-id="3d682-126">Exemples exécutables</span><span class="sxs-lookup"><span data-stu-id="3d682-126">Executable examples</span></span>

## <a name="formatting-illustrative-examples"></a><span data-ttu-id="3d682-127">Mise en forme des exemples illustratifs</span><span class="sxs-lookup"><span data-stu-id="3d682-127">Formatting illustrative examples</span></span>

<span data-ttu-id="3d682-128">Des exemples illustratifs sont utilisés pour expliquer un concept PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d682-128">Illustrative examples are used to explain a PowerShell concept.</span></span> <span data-ttu-id="3d682-129">Ils ne sont pas destinés à être copiés dans le Presse-papiers pour être exécutés.</span><span class="sxs-lookup"><span data-stu-id="3d682-129">They are not meant to be copied to the clipboard for execution.</span></span> <span data-ttu-id="3d682-130">Ils sont le plus souvent utilisés pour des exemples simples qui sont faciles à taper.</span><span class="sxs-lookup"><span data-stu-id="3d682-130">These are most commonly used for simple examples that are easy to type.</span></span>
<span data-ttu-id="3d682-131">Ils sont également utilisés pour des exemples de syntaxe là où vous illustrez la syntaxe d’une commande.</span><span class="sxs-lookup"><span data-stu-id="3d682-131">They are also used for syntax examples where you are illustrating the syntax of a command.</span></span>

<span data-ttu-id="3d682-132">Les exemples illustratifs utilisent une délimitation de code « nue » pour marquer le début et la fin du bloc de code.</span><span class="sxs-lookup"><span data-stu-id="3d682-132">Illustrative examples use a "naked" code fence to mark the beginning and end of the code block.</span></span> <span data-ttu-id="3d682-133">Le bloc de code peut contenir un exemple de résultat de la commande illustrée.</span><span class="sxs-lookup"><span data-stu-id="3d682-133">The code block may contain example output from the command being illustrated.</span></span>

### <a name="syntax-block"></a><span data-ttu-id="3d682-134">Bloc de syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d682-134">Syntax block</span></span>

<span data-ttu-id="3d682-135">Cet exemple illustre tous les paramètres possibles de l’applet de commande `Get-Command`.</span><span class="sxs-lookup"><span data-stu-id="3d682-135">This example illustrates all the possible parameters of the `Get-Command` cmdlet.</span></span>

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

<span data-ttu-id="3d682-136">Cet exemple décrit l’instruction `for` en termes généralisés :</span><span class="sxs-lookup"><span data-stu-id="3d682-136">This example describes the `for` statement in generalized terms:</span></span>

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a><span data-ttu-id="3d682-137">Exemple d’illustration simple</span><span class="sxs-lookup"><span data-stu-id="3d682-137">Simple illustration example</span></span>

<span data-ttu-id="3d682-138">Voici un exemple illustrant des opérateurs de comparaison de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3d682-138">Here is an example illustrating PowerShell comparison operators:</span></span>

~~~markdown
```
PS> 2 -eq 2
True

PS> 2 -eq 3
False

PS>  1,2,3 -eq 2
2

PS> "abc" -eq "abc"
True

PS> "abc" -eq "abc", "def"
False

PS> "abc", "def" -eq "abc"
abc
```
~~~

<span data-ttu-id="3d682-139">Notez que cet exemple utilise l’invite PowerShell simplifiée et montre la sortie obtenue.</span><span class="sxs-lookup"><span data-stu-id="3d682-139">Note that this example has the simplified PowerShell prompt and shows the resulting output.</span></span> <span data-ttu-id="3d682-140">Dans ce cas, nous ne prévoyons pas que le lecteur copie cet exemple et l’exécute.</span><span class="sxs-lookup"><span data-stu-id="3d682-140">In this case, we don't intend the reader to copy and run this example.</span></span>

## <a name="formatting-executable-examples"></a><span data-ttu-id="3d682-141">Mise en forme des exemples exécutables</span><span class="sxs-lookup"><span data-stu-id="3d682-141">Formatting executable examples</span></span>

<span data-ttu-id="3d682-142">Les exemples plus complexes, ou les exemples dont la copie et l’exécution sont jugées utiles, doivent utiliser le balisage de style de bloc suivant :</span><span class="sxs-lookup"><span data-stu-id="3d682-142">More complex examples or examples that are intended to be useful to copy and execute should use the following block-style markup:</span></span>

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

<span data-ttu-id="3d682-143">La sortie affichée par les commandes PowerShell doit être placée dans un bloc de code **Output** (Sortie) pour empêcher la mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3d682-143">The output displayed by PowerShell commands should be enclosed in an **Output** code block to prevent syntax highlighting.</span></span> <span data-ttu-id="3d682-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3d682-144">For example:</span></span>

~~~markdown
```powershell
Get-Command -Module Microsoft.PowerShell.Security
```

```Output
CommandType  Name                        Version    Source
-----------  ----                        -------    ------
Cmdlet       ConvertFrom-SecureString    3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       ConvertTo-SecureString      3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-CmsMessage              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-Credential              3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Get-PfxCertificate          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       New-FileCatalog             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Protect-CmsMessage          3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-Acl                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-AuthenticodeSignature   3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Set-ExecutionPolicy         3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Test-FileCatalog            3.0.0.0    Microsoft.PowerShell.Security
Cmdlet       Unprotect-CmsMessage        3.0.0.0    Microsoft.PowerShell.Security
```
~~~

<span data-ttu-id="3d682-145">L’étiquette de code **Output**  n’est pas un « langage » officiel pris en charge par le système de mise en surbrillance de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3d682-145">The **Output** code label is not an official "language" supported by the syntax highlighting system.</span></span>
<span data-ttu-id="3d682-146">Cette étiquette est cependant pratique, car OPS ajoute l’étiquette « Output » à la zone de code sur la page web.</span><span class="sxs-lookup"><span data-stu-id="3d682-146">However, this label is useful because OPS adds the "Output" label to the code box on the web page.</span></span>
<span data-ttu-id="3d682-147">La syntaxe de cette zone de code « Output » n’est donc pas mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="3d682-147">And this "Output" code box has no syntax highlighting.</span></span>

## <a name="coding-style-rules"></a><span data-ttu-id="3d682-148">Règles de style pour le code</span><span class="sxs-lookup"><span data-stu-id="3d682-148">Coding style rules</span></span>

### <a name="avoid-line-continuation-in-code-samples"></a><span data-ttu-id="3d682-149">Éviter les continuations de ligne dans les exemples de code</span><span class="sxs-lookup"><span data-stu-id="3d682-149">Avoid line continuation in code samples</span></span>

<span data-ttu-id="3d682-150">Évitez d’utiliser les caractères de continuation de ligne (`` ` ``) dans les exemples de code PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d682-150">Avoid using line continuation characters (`` ` ``) in PowerShell code examples.</span></span> <span data-ttu-id="3d682-151">Ils sont difficiles à voir et peuvent provoquer des problèmes s’il existe des espaces supplémentaires à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="3d682-151">These are hard to see and can cause problems if there are extra spaces at the end of the line.</span></span>

- <span data-ttu-id="3d682-152">Utilisez le « splatting » de PowerShell pour réduire la longueur des lignes pour les applets de commande qui ont un grand nombre de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3d682-152">Use PowerShell splatting to reduce line length for cmdlets that have a lot of parameters.</span></span>
- <span data-ttu-id="3d682-153">Tirez parti des possibilités naturelles de saut de ligne de PowerShell, par exemple après les caractères de barre verticale (`|`), les accolades ouvrantes, les parenthèses et les crochets.</span><span class="sxs-lookup"><span data-stu-id="3d682-153">Take advantage of PowerShell's natural line break opportunities, like after pipe (`|`) characters, opening braces, parentheses, and brackets.</span></span>

### <a name="avoid-using-powershell-prompts-in-examples"></a><span data-ttu-id="3d682-154">Évitez d’utiliser les invites PowerShell dans les exemples.</span><span class="sxs-lookup"><span data-stu-id="3d682-154">Avoid using PowerShell prompts in examples</span></span>

<span data-ttu-id="3d682-155">L’utilisation de la chaîne d’invite est déconseillée et doit être limitée aux scénarios qui sont destinés à illustrer l’utilisation de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3d682-155">Use of the prompt string is discouraged and should be limited to scenarios that are meant to illustrate command line usage.</span></span> <span data-ttu-id="3d682-156">Les invites sont nécessaires pour les exemples qui illustrent des commandes modifiant l’invite ou quand le chemin affiché est significatif pour le scénario illustré.</span><span class="sxs-lookup"><span data-stu-id="3d682-156">Prompts are required for examples that illustrate commands that alter the prompt or when the path displayed is significant to the scenario being illustrated.</span></span>

- <span data-ttu-id="3d682-157">Les invites PowerShell ne doivent être utilisées que dans les exemples illustratifs.</span><span class="sxs-lookup"><span data-stu-id="3d682-157">PowerShell prompts should only be used in illustrative examples.</span></span> <span data-ttu-id="3d682-158">Pour la plupart de ces exemples, la chaîne d’invite doit être « `PS>` ».</span><span class="sxs-lookup"><span data-stu-id="3d682-158">For most of these examples, the prompt string should be "`PS>`".</span></span> <span data-ttu-id="3d682-159">Cette invite est indépendante des indicateurs spécifiques au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3d682-159">This prompt is independent of OS-specific indicators.</span></span>
- <span data-ttu-id="3d682-160">Les invites ne doivent **PAS** être utilisées dans les exemples exécutables.</span><span class="sxs-lookup"><span data-stu-id="3d682-160">Prompts should **NOT** be used in executable examples.</span></span>

<span data-ttu-id="3d682-161">L’exemple suivant montre comment l’invite change lors de l’utilisation du fournisseur de Registre.</span><span class="sxs-lookup"><span data-stu-id="3d682-161">The following example illustrates how the prompt changes when using the Registry provider.</span></span>

```powershell
PS C:\> cd HKCU:\System\
PS HKCU:\System\> dir

    Hive: HKEY_CURRENT_USER\System

Name                   Property
----                   --------
CurrentControlSet
GameConfigStore        GameDVR_Enabled                       : 1
                       GameDVR_FSEBehaviorMode               : 2
                       Win32_AutoGameModeDefaultProfile      : {2, 0, 1, 0...}
                       Win32_GameModeRelatedProcesses        : {1, 0, 1, 0...}
                       GameDVR_HonorUserFSEBehaviorMode      : 0
                       GameDVR_DXGIHonorFSEWindowsCompatible : 0
```

### <a name="do-not-use-aliases-in-examples"></a><span data-ttu-id="3d682-162">N’utilisez pas d’alias dans les exemples</span><span class="sxs-lookup"><span data-stu-id="3d682-162">Do not use aliases in examples</span></span>

<span data-ttu-id="3d682-163">Vous devez toujours utiliser le nom complet de toutes les applets de commande et de tous les paramètres, sauf si vous parlez spécifiquement de l’alias.</span><span class="sxs-lookup"><span data-stu-id="3d682-163">You should always use the full name of all cmdlets and parameters unless you are specifically talking about the alias.</span></span> <span data-ttu-id="3d682-164">Les noms des applets de commande et des paramètres doivent utiliser l’écriture dans la casse Pascal appropriée qui est définie dans le code.</span><span class="sxs-lookup"><span data-stu-id="3d682-164">Cmdlet and parameter names must use the proper Pascal-case spelling defined in the code.</span></span>

### <a name="using-parameters-in-examples"></a><span data-ttu-id="3d682-165">Utilisation de paramètres dans les exemples</span><span class="sxs-lookup"><span data-stu-id="3d682-165">Using parameters in examples</span></span>

<span data-ttu-id="3d682-166">Évitez d’utiliser des paramètres positionnels</span><span class="sxs-lookup"><span data-stu-id="3d682-166">Avoid using positional parameters.</span></span> <span data-ttu-id="3d682-167">D’une façon générale, vous devez toujours inclure le nom du paramètre dans un exemple, même si le paramètre est positionnel.</span><span class="sxs-lookup"><span data-stu-id="3d682-167">In general, you should use always include the parameter name in an example, even if the parameter positional.</span></span> <span data-ttu-id="3d682-168">Ceci réduit le risque de confusion dans vos exemples.</span><span class="sxs-lookup"><span data-stu-id="3d682-168">This reduces the chance of confusion in your examples.</span></span>
