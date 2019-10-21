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
# <a name="formatting-code-samples"></a>Mise en forme des exemples de code

La documentation existante a utilisé plusieurs styles au fil du temps, et les règles de mise en forme ont été modifiées plusieurs fois. Nous essayons d’établir un style cohérent pour les blocs de code PowerShell et leur résultat dans notre documentation.

Markdown prend en charge deux styles de code différents :

- Étendues de code (inline) : marquées par un seul caractère d’accent grave (`` ` ``). Utilisées à l’intérieur d’un paragraphe, plutôt que comme bloc autonome. Elles sont le plus souvent utilisées autour des noms des applets de commande. Consultez [Mise en forme des éléments de la syntaxe des commandes](powershell-style-basic-markdown.md#formatting-command-syntax-elements).
- Blocs de code : bloc de plusieurs lignes entouré de chaînes de trois accents graves (`` ``` ``).

## <a name="using-code-blocks"></a>Utilisation des blocs de code

Markdown permet l’indentation pour représenter un bloc de code, mais ce modèle peut être problématique et doit être évité. Tous les blocs de code doivent être entourés d’une délimitation de code. Une délimitation de code est un bloc de code entouré de chaînes de trois accents graves (`` ``` ``). Les marqueurs de délimitation de code doivent se trouver sur leur propre ligne avant et après l’exemple de code. Le marqueur au début du bloc de code peut avoir une étiquette de langage facultative. Le système de publication OPS de Microsoft utilise l’étiquette de langage pour prendre en charge la fonctionnalité de mise en surbrillance de la syntaxe.

OPS ajoute également un bouton de **Copie** qui copie le contenu du bloc de code dans le Presse-papiers. Ceci vous permet de coller rapidement le code dans un script pour tester l’exemple de code. Cependant, tous les exemples de notre documentation ne sont pas destinés à être exécutés de cette façon. Certains blocs de code peuvent être la simple illustration d’un concept PowerShell ou une représentation abstraite de la syntaxe.

Deux types de blocs de code sont utilisés dans notre documentation :

1. Exemples illustratifs
2. Exemples exécutables

## <a name="formatting-illustrative-examples"></a>Mise en forme des exemples illustratifs

Des exemples illustratifs sont utilisés pour expliquer un concept PowerShell. Ils ne sont pas destinés à être copiés dans le Presse-papiers pour être exécutés. Ils sont le plus souvent utilisés pour des exemples simples qui sont faciles à taper.
Ils sont également utilisés pour des exemples de syntaxe là où vous illustrez la syntaxe d’une commande.

Les exemples illustratifs utilisent une délimitation de code « nue » pour marquer le début et la fin du bloc de code. Le bloc de code peut contenir un exemple de résultat de la commande illustrée.

### <a name="syntax-block"></a>Bloc de syntaxe

Cet exemple illustre tous les paramètres possibles de l’applet de commande `Get-Command`.

~~~markdown
```
Get-Command [-Verb <String[]>] [-Noun <String[]>] [-Module <String[]>]
  [-FullyQualifiedModule <ModuleSpecification[]>] [-TotalCount <Int32>] [-Syntax] [-ShowCommandInfo]
  [[-ArgumentList] <Object[]>] [-All] [-ListImported] [-ParameterName <String[]>]
  [-ParameterType <PSTypeName[]>] [<CommonParameters>]
```
~~~

Cet exemple décrit l’instruction `for` en termes généralisés :

~~~markdown
```
for (<init>; <condition>; <repeat>)
{<statement list>}
```
~~~

### <a name="simple-illustration-example"></a>Exemple d’illustration simple

Voici un exemple illustrant des opérateurs de comparaison de PowerShell :

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

Notez que cet exemple utilise l’invite PowerShell simplifiée et montre la sortie obtenue. Dans ce cas, nous ne prévoyons pas que le lecteur copie cet exemple et l’exécute.

## <a name="formatting-executable-examples"></a>Mise en forme des exemples exécutables

Les exemples plus complexes, ou les exemples dont la copie et l’exécution sont jugées utiles, doivent utiliser le balisage de style de bloc suivant :

~~~markdown
```powershell
<PowerShell code goes here>
```
~~~

La sortie affichée par les commandes PowerShell doit être placée dans un bloc de code **Output** (Sortie) pour empêcher la mise en surbrillance de la syntaxe. Par exemple :

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

L’étiquette de code **Output**  n’est pas un « langage » officiel pris en charge par le système de mise en surbrillance de la syntaxe.
Cette étiquette est cependant pratique, car OPS ajoute l’étiquette « Output » à la zone de code sur la page web.
La syntaxe de cette zone de code « Output » n’est donc pas mise en surbrillance.

## <a name="coding-style-rules"></a>Règles de style pour le code

### <a name="avoid-line-continuation-in-code-samples"></a>Éviter les continuations de ligne dans les exemples de code

Évitez d’utiliser les caractères de continuation de ligne (`` ` ``) dans les exemples de code PowerShell. Ils sont difficiles à voir et peuvent provoquer des problèmes s’il existe des espaces supplémentaires à la fin de la ligne.

- Utilisez le « splatting » de PowerShell pour réduire la longueur des lignes pour les applets de commande qui ont un grand nombre de paramètres.
- Tirez parti des possibilités naturelles de saut de ligne de PowerShell, par exemple après les caractères de barre verticale (`|`), les accolades ouvrantes, les parenthèses et les crochets.

### <a name="avoid-using-powershell-prompts-in-examples"></a>Évitez d’utiliser les invites PowerShell dans les exemples.

L’utilisation de la chaîne d’invite est déconseillée et doit être limitée aux scénarios qui sont destinés à illustrer l’utilisation de la ligne de commande. Les invites sont nécessaires pour les exemples qui illustrent des commandes modifiant l’invite ou quand le chemin affiché est significatif pour le scénario illustré.

- Les invites PowerShell ne doivent être utilisées que dans les exemples illustratifs. Pour la plupart de ces exemples, la chaîne d’invite doit être « `PS>` ». Cette invite est indépendante des indicateurs spécifiques au système d’exploitation.
- Les invites ne doivent **PAS** être utilisées dans les exemples exécutables.

L’exemple suivant montre comment l’invite change lors de l’utilisation du fournisseur de Registre.

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

### <a name="do-not-use-aliases-in-examples"></a>N’utilisez pas d’alias dans les exemples

Vous devez toujours utiliser le nom complet de toutes les applets de commande et de tous les paramètres, sauf si vous parlez spécifiquement de l’alias. Les noms des applets de commande et des paramètres doivent utiliser l’écriture dans la casse Pascal appropriée qui est définie dans le code.

### <a name="using-parameters-in-examples"></a>Utilisation de paramètres dans les exemples

Évitez d’utiliser des paramètres positionnels D’une façon générale, vous devez toujours inclure le nom du paramètre dans un exemple, même si le paramètre est positionnel. Ceci réduit le risque de confusion dans vos exemples.
