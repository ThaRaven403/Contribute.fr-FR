---
title: Inclure du code dans la documentation
description: Découvrez comment inclure des extraits et des éléments de code dans des articles à publier sur docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 03/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 4aa34196f59a69651dd19add35a0351dd9b5d59b
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336489"
---
# <a name="how-to-include-code-in-docs"></a>Inclure du code dans la documentation

Il existe plusieurs façons d’inclure du code dans un article publié sur docs.microsoft.com :

* Éléments individuels (mots) dans une ligne.

  Voici un exemple de style `code`.

  Utilisez le format de code quand vous faites référence à des variables et des paramètres nommés dans un bloc de code proche dans votre texte. Le format de code peut également être utilisé pour les propriétés, les méthodes, les classes et les mots clés de langage. Pour plus d’informations, consultez [Éléments de code](#code-elements) plus loin dans cet article.

* Blocs de code dans le fichier Markdown de l’article.

  ```markdown
      ```csharp
      public static void Log(string message)
      {
          _logger.LogInformation(message);
      }
      ```
  ```

  Utilisez des blocs de code inline quand il est peu pratique d’afficher le code par référence à un fichier de code. Pour plus d’informations, consultez [Blocs de code](#inline-code-blocks) plus loin dans cet article.

* Blocs de code par référence à un fichier de code dans le dépôt local.

  ```markdown
  :::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
  ```

  Pour plus d’informations, consultez [Références à des extraits de code au sein du référentiel](#in-repo-snippet-references) plus loin dans cet article.

* Blocs de code par référence à un fichier de code dans un autre dépôt.

  ```markdown
  :::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
  ```
  
  Pour plus d’informations, consultez [Références à des extraits de code en dehors du référentiel](#out-of-repo-snippet-references) plus loin dans cet article.
  
* Blocs de code qui permettent à l’utilisateur d’exécuter du code dans le navigateur.

   ```markdown
  :::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
  ```

  Pour plus d’informations, consultez [Extraits de code interactif](#interactive-code-snippets) plus loin dans cet article.

Non seulement l’article décrit le Markdown pour chacune de ces manières d’inclure du code, mais il offre également une [aide générale pour tous les blocs de code](#code-blocks).

## <a name="code-elements"></a>Éléments de code

Un « élément de code » est un mot clé d’un langage de programmation, un nom de classe, un nom de propriété, etc. Il n’est pas toujours évident de savoir ce qui peut être considéré comme du code. Par exemple, les noms de package NuGet doivent être traités comme du code. En cas de doute, consultez la page [Instructions de mise en forme du texte](text-formatting-guidelines.md).

### <a name="inline-code-style"></a>Style code inline

Pour inclure un élément de code dans le texte de l’article, encadrez-le avec des accents graves (\`) pour indiquer le style code.
Le style code inline ne doit pas utiliser le format des trois accents graves.

|Markdown |Rendu |
|---------|---------|
|Par défaut, Entity Framework interprète une propriété nommée \`Id\` ou \`ClassnameID\` comme étant la clé primaire.|Par défaut, Entity Framework interprète une propriété nommée `Id` ou `ClassnameID` comme étant la clé primaire.|

Lorsqu’un article est localisé (traduit dans d’autres langues), le texte mis en forme comme du code reste inchangé. Si vous souhaitez empêcher la localisation sans utiliser le style code, consultez [Chaînes non localisées](markdown-reference.md#non-localized-strings).

### <a name="bold-style"></a>Style gras

D’anciens guides de style permettent de spécifier du code inline en gras. Le style gras est possible lorsque le style code est si gênant qu’il ferait perdre en lisibilité. Par exemple, un tableau Markdown comportant principalement des éléments de code risque de paraître trop chargé avec du style code partout. Si vous choisissez d’utiliser le style gras, utilisez la [syntaxe des chaînes non localisées](markdown-reference.md#non-localized-strings) pour que le code ne soit pas localisé.

### <a name="links"></a>Liens

Un lien vers la documentation de référence peut être plus utile que le format de code dans certains contextes. Si vous utilisez un lien, n’appliquez pas de format de code au texte du lien. Il risquerait masquer le fait que le texte est un lien.

Si vous utilisez un lien et que vous faites référence au même élément ultérieurement dans le même contexte, définissez les instances suivantes en tant que format de code plutôt que liens.

### <a name="placeholders"></a>Espaces réservés

Si vous souhaitez que l’utilisateur remplace une section du code affiché par ses propres valeurs, utilisez le texte de l’espace réservé délimité par des crochets pointus ou des accolades. Par exemple, `az group delete -n <ResourceGroupName>`. Expliquez que les crochets ou les accolades doivent être supprimés lors du remplacement par des valeurs réelles.

## <a name="code-blocks"></a>Blocs de code

La syntaxe pour inclure du code dans un document dépend de l’endroit où se trouve le code :

* [Dans le fichier Markdown de l’article](#inline-code-blocks)
* [Dans un fichier de code du même référentiel](#in-repo-snippet-references)
* [Dans un fichier de code d’un autre référentiel](#out-of-repo-snippet-references)

Voici les instructions qui s’appliquent aux trois types de blocs de code :

* [Automatiser la validation du code.](#code-validation)
* [Mettre en surbrillance les principales lignes de code.](#highlighting)
* [Éviter les barres de défilement horizontales.](#horizontal-scroll-bars)

### <a name="screenshots"></a>Captures d’écran

Toutes les méthodes listées dans la section précédente produisent des blocs de code utilisables :

* Vous pouvez effectuer des opérations de copier-coller à partir de ces derniers.
* Ils sont indexés par les moteurs de recherche.
* Ils sont accessibles aux lecteurs d’écran.

Ce ne sont là que quelques raisons pour lesquelles les captures d’écran IDE ne sont pas recommandées comme méthode d’inclusion de code dans un article. Utilisez des captures d’écran IDE pour le code uniquement si vous affichez des informations sur l’IDE lui-même, comme IntelliSense. N’utilisez pas de captures d’écran uniquement pour montrer la coloration et la mise en surbrillance.

### <a name="code-validation"></a>Validation du code

Certains référentiels ont implémenté des processus qui compilent automatiquement tous les exemples de code pour rechercher les erreurs. C’est le cas du dépôt .NET. Pour plus d’informations, consultez [Contribution](https://github.com/dotnet/docs/blob/master/CONTRIBUTING.md) dans le référentiel .NET.

Si vous incluez des blocs de code à partir d’un autre dépôt, collaborez avec les propriétaires sur une stratégie de maintenance du code afin que votre code inclus ne plante pas ou n’expire pas au fur et à mesure que sont fournies de nouvelles versions des bibliothèques utilisées par le code.

### <a name="highlighting"></a>Mettre en surbrillance

Les extraits de code comportent généralement plus de code qu’il n’en faut, afin d’indiquer le contexte. La lisibilité s’en trouve améliorée si les lignes principales sur lesquelles porte l’extrait de code sont mises en surbrillance, comme dans cet exemple :

![Exemple montrant du code mis en surbrillance](media/code-in-docs/highlighted-code.png)

Vous ne pouvez pas mettre en surbrillance du code intégré au fichier Markdown de l’article. Cela ne fonctionne que pour les extraits de code fournis par référence à un fichier de code.

### <a name="horizontal-scroll-bars"></a>Barres de défilement horizontales

Scindez les longues lignes afin d’éviter d’avoir des barres de défilement horizontales. Les barres de défilement rendent les blocs de code difficiles à lire. Ils sont particulièrement problématiques sur les blocs de code très longs pour lesquels il serait impossible de voir en même temps la barre de défilement et la ligne que l’on souhaite lire.

Une bonne pratique pour minimiser les barres de défilement horizontales sur les blocs de code consiste à scinder les lignes de code de plus de 85 caractères. Toutefois, gardez à l’esprit que la présence ou l’absence d’une barre de défilement n’est pas le seul critère de lisibilité. Si la scission d’une ligne avant 85 caractères nuit à la lisibilité ou à la commodité du copier-coller, n’hésitez pas à aller au-delà des 85 caractères.

## <a name="inline-code-blocks"></a>Blocs de code inline

Utilisez des blocs de code inline uniquement quand il est peu pratique d’afficher le code par référence à un fichier de code. Le code inline est généralement plus difficile à tester et à maintenir à jour qu’un fichier de code qui fait partie d’un projet complet.  En outre, le code inline peut omettre le contexte qui pourrait aider le développeur à comprendre et à utiliser le code. Ces considérations s’appliquent principalement aux langages de programmation. Les blocs de code inline peuvent également être utilisés pour les sorties et les entrées (telles que JSON), les langages de requête (tels que SQL) et les langages de script (tels que PowerShell).
  
Il y a deux façons d’indiquer qu’une section de texte d’un fichier de l’article est un bloc de code : en *la délimitant* par trois accents graves (\`\`\`) ou en la mettant en retrait. La délimitation est recommandée, car elle permet de spécifier le langage. Évitez d’utiliser la mise en retrait, car il est trop facile de se tromper et il peut être difficile pour un autre rédacteur de comprendre votre intention quand il doit modifier votre article.

Les indicateurs de langage sont placés immédiatement après les accents graves du début, comme dans l’exemple suivant :

Markdown

```markdown
    ```json
    {
        "aggregator": {
            "batchSize": 1000,
            "flushTimeout": "00:00:30"
        }
    }
    ```
```

Rendu

```json
{
    "aggregator": {
        "batchSize": 1000,
        "flushTimeout": "00:00:30"
    }
}
```

Pour plus d’informations sur les valeurs possibles des indicateurs de langage, consultez la page [Alias et noms de langage](http://highlightjs.readthedocs.io/en/latest/css-classes-reference.html#language-names-and-aliases).

Si vous utilisez un mot de langage ou d’environnement après les trois accents graves (\`\`\`) qui ne sont pas pris en charge, ce mot apparaît dans la barre de titre de la section de code sur la page affichée. Dans la mesure du possible, utilisez un indicateur de langage ou d’environnement dans vos blocs de code inline.

> [!NOTE]
> Si vous copiez et collez du code à partir d’un document Word, assurez-vous qu’il n’a pas de « guillemets courbes », qui ne sont pas valides dans le code (par exemple, `“` et `’`). Si c’est le cas, remplacez-les par des guillemets normaux (`'` et `"`). Vous pouvez également utiliser la [fonctionnalité de remplacement des guillemets courbes](docs-authoring/smart-quote-replacement.md) du Docs Authoring Pack.

## <a name="in-repo-snippet-references"></a>Références à des extraits de code au sein du référentiel

La meilleure façon d’inclure des extraits de code pour les langages de programmation dans la documentation est de faire référence à un fichier de code. Cette méthode vous donne la possibilité de mettre en évidence des lignes de code et de rendre le contexte plus vaste de l’extrait de code disponible sur GitHub pour les développeurs. Vous pouvez inclure du code à l’aide du format triple deux-points (:\:\:) manuellement ou dans Visual Studio Code à l’aide de [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Dans Visual Studio Code, cliquez sur <kbd>Alt + M</kbd> ou sur <kbd>Option + M</kbd> et sélectionnez Snippet (Extrait).
2. Une fois Snippet sélectionné, vous êtes invité à choisir entre Full Search (Recherche complète), Scoped Search (Recherche délimitée) et Cross-Repository Reference (Référence interdépôts). Pour effectuer une recherche locale, sélectionnez Full Search (Recherche complète).
3. Entrez un terme de recherche pour rechercher le fichier. Une fois le fichier trouvé, sélectionnez-le.
4. Ensuite, sélectionnez une option pour déterminer la ou les lignes de code à inclure dans l’extrait. Les options disponibles sont : **ID**, **Range** (Plage) et **None** (Aucune).
5. En fonction de votre sélection à l’étape 4, indiquez une valeur si nécessaire.

Afficher la totalité du fichier de code :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs":::
```

Afficher une partie du fichier de code en spécifiant les numéros de ligne :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Afficher une partie du fichier de code en spécifiant le nom de l’extrait :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Les sections suivantes expliquent ces exemples :

* [Utiliser un chemin d’accès relatif au fichier de code](#path-to-code-file)
* [Inclure uniquement les numéros de ligne sélectionnés](#selected-line-numbers)
* [Faire référence à un extrait de code nommé](#named-snippet)
* [Mettre en surbrillance les lignes sélectionnées](#highlighting-selected-lines)

Pour plus d’informations, consultez [Informations de référence sur la syntaxe des extraits](#snippet-syntax-reference) plus loin dans cet article.

### <a name="path-to-code-file"></a>Chemin d’accès au fichier de code

Exemple :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

L’exemple est issu du dépôt de la documentation ASP.NET, le fichier de l’article [aspnetcore/data/ef-mvc/crud.md](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/crud.md). La référence au fichier de code est un chemin d’accès relatif à [aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs](https://github.com/aspnet/Docs/blob/master/aspnetcore/data/ef-mvc/intro/samples/cu/Controllers/StudentsController.cs) dans le même référentiel.

### <a name="selected-line-numbers"></a>Numéros de ligne sélectionnés

Exemple :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26":::
```

Cet exemple affiche uniquement les lignes 2-24 et 26 du fichier de code *StudentController.cs*.

Préférez les extraits de code nommés aux numéros de ligne codés en dur, comme l’explique la section suivante.

### <a name="named-snippet"></a>Extrait de code nommé

Exemple :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" id="snippet_Create":::
```

Utilisez uniquement des lettres et des traits de soulignement dans le nom.

L’exemple affiche la section `snippet_Create` du fichier de code. Dans cet exemple, le code C# du fichier de code contient des balises d’extrait de code dans les commentaires :

```cs
// code excluded from the snippet
// <snippet_Create>
// code included in the snippet
// </snippet_Create>
// code excluded from the snippet
```

Dans la mesure du possible, faites référence à une section nommée au lieu de spécifier les numéros de ligne. Les références aux numéros de ligne sont fragiles, car les fichiers de code évoluent inévitablement, ce qui modifie les numéros de ligne.
Ces modifications ne font pas forcément l’objet de notifications. Votre article finit par ne plus afficher les bonnes lignes, sans que vous en ayez connaissance.

### <a name="highlighting-selected-lines"></a>Mise en surbrillance des lignes sélectionnées

Exemple :

```markdown
:::code language="csharp" source="intro/samples/cu/Controllers/StudentsController.cs" range="2-24,26" highlight="2,5":::
```

L’exemple met en surbrillance les lignes 2 et 5, à partir du début de l’extrait de code affiché. Les numéros de ligne à mettre en surbrillance ne sont pas comptés à partir du début du fichier de code. En d’autres termes, les lignes 3 et 6 du fichier de code sont mises en surbrillance.

## <a name="out-of-repo-snippet-references"></a>Références à des extraits de code en dehors du référentiel

Si vous souhaitez faire référence à un fichier de code qui se trouve dans un autre dépôt, configurez le dépôt de code en tant que *dépôt dépendant*. Ce faisant, vous lui donnerez un nom. Ce nom fonctionnera alors comme un nom de dossier pour les références au code.

Supposons que le référentiel de documents soit *Azure/azure-docs*, et le référentiel de code *Azure/azure-fonctions-durable-extension*.

Dans le dossier racine de *azure-docs*, ajoutez la section suivante dans *. openpublishing.publish.config.json* :

```json
    {
      "path_to_root": "samples-durable-functions",
      "url": "https://github.com/Azure/azure-functions-durable-extension",
      "branch": "master",
      "branch_mapping": {}
    },
```

Maintenant, quand vous faites référence à *samples-durable-functions* comme s’il s’agissait d’un dossier dans *azure-docs*, vous faites en réalité référence au dossier racine du dépôt *azure-functions-durable-extension*.

Vous pouvez inclure du code à l’aide du format triple deux-points (:\:\:) manuellement ou dans Visual Studio Code à l’aide de [docs.microsoft.com Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack).

1. Dans Visual Studio Code, cliquez sur <kbd>Alt + M</kbd> ou sur <kbd>Option + M</kbd> et sélectionnez Snippet (Extrait).
2. Une fois Snippet sélectionné, vous êtes invité à choisir entre Full Search (Recherche complète), Scoped Search (Recherche délimitée) et Cross-Repository Reference (Référence interdépôts). Pour effectuer une recherche dans plusieurs dépôts, sélectionnez Cross-Repository Reference.
3. Une sélection de dépôts figurant dans *.openpublishing.publish.config.json* s’affiche. Sélectionnez un dépôt.
4. Entrez un terme de recherche pour rechercher le fichier. Une fois le fichier trouvé, sélectionnez-le.
5. Ensuite, sélectionnez une option pour déterminer la ou les lignes de code à inclure dans l’extrait. Les options disponibles sont : **ID**, **Range** (Plage) et **None** (Aucune).
6. En fonction de votre sélection à l’étape 5, indiquez une valeur.

Votre référence à l’extrait se présente ainsi :

```markdown
:::code language="csharp" source="~/samples-durable-functions/samples/csx/shared/Location.csx" highlight="2,5":::
```

Dans le référentiel *azure-functions-durable-extension*, ce fichier de code se trouve dans le dossier *samples/csx/shared*. Comme indiqué [précédemment](#highlighting-selected-lines), les numéros de ligne pour la mise en surbrillance sont relatifs au début de l’extrait de code et non au début du fichier.

> [!NOTE]
> Le nom que vous attribuez au dépôt dépendant est relatif à la racine du dépôt principal, mais le tilde (~) fait référence à la racine du docset. La racine du docset est déterminée par `build_source_folder` dans *.openpublishing.publish.config.json*. Le chemin de l’extrait de code dans l’exemple précédent fonctionne dans le dépôt azure-docs, car `build_source_folder` fait référence à la racine du dépôt (`.`). Si `build_source_folder` avait pour valeur `articles`, le chemin commencerait par `~/../samples-durable-functions` au lieu de `~/samples-durable-functions`.

## <a name="interactive-code-snippets"></a>Extraits de code interactif

### <a name="inline-interactive-code-blocks"></a>Blocs de code interactifs inline

Pour les langages suivants, les extraits de code peuvent être exécutables dans la fenêtre du navigateur :

* Azure Cloud Shell
* Azure PowerShell Cloud Shell
* C# REPL

Lorsque le mode interactif est activé, les zones de code qui s’affichent ont un bouton **Essayer** ou **Exécuter**. Par exemple :

```markdown
    ```azurepowershell-interactive
    New-AzResourceGroup -Name myResourceGroup -Location westeurope
    ```
```

s’affiche ainsi :

```azurepowershell-interactive
New-AzResourceGroup -Name myResourceGroup -Location westeurope
```

Si vous voulez activer cette fonctionnalité pour un bloc de code donné, utilisez un identificateur de langage spécial. Les options disponibles sont les suivantes :

* `azurepowershell-interactive` : active Azure PowerShell Cloud Shell, comme dans l’exemple précédent
* `azurecli-interactive` : active Azure Cloud Shell
* `csharp-interactive` :active C# REPL

Avec Azure Cloud Shell et PowerShell Cloud Shell, les utilisateurs ne peuvent exécuter des commandes que sur leur propre compte Azure.

### <a name="code-snippets-included-by-reference"></a>Extraits de code inclus par référence

Il est possible d’activer le mode interactif pour les extraits de code inclus par référence. Voici quelques exemples :

```markdown
:::code source="PowerShell.ps1" interactive="cloudshell-powershell":::
```

```markdown
:::code source="Bash.sh" interactive="cloudshell-bash":::
```

Pour activer cette fonctionnalité pour un bloc de code donné, utilisez l’attribut `interactive`. Les valeurs d’attribut disponibles sont les suivantes :

* `cloudshell-powershell` : active Azure PowerShell Cloud Shell, comme dans l’exemple précédent
* `cloudshell-bash` : active Azure Cloud Shell
* `try-dotnet` : active Try .NET
* `try-dotnet-class` : active Try .NET avec génération de modèles automatique de classe
* `try-dotnet-method` : active Try .NET avec génération de modèles automatique de méthode

Avec Azure Cloud Shell et PowerShell Cloud Shell, les utilisateurs ne peuvent exécuter des commandes que sur leur propre compte Azure.

## <a name="snippet-syntax-reference"></a>Informations de référence sur la syntaxe des extraits

Syntaxe :

```md
:::code language="<language>" source="<path>" <attribute>="<attribute-value>":::
```

> [!IMPORTANT]
> Cette syntaxe est une extension de bloc Markdown. Elle doit être utilisée seule, sur sa propre ligne.

* `<language>` (*facultatif*)
  * Langage de l’extrait de code. Pour plus d’informations, consultez la section [Langages pris en charge](#supported-languages) plus loin dans cet article.

* `<path>` (*obligatoire*)
  * Chemin relatif dans le système de fichiers qui indique le fichier d’extrait de code à référencer.

* `<attribute>` et `<attribute-value>` (*facultatif*)
  * Utilisés ensemble pour spécifier la manière dont le code doit être récupéré à partir du fichier et dont il doit être affiché :
    * `range` : `1,3-5` plage de lignes. Cet exemple inclut les lignes 1, 3, 4 et 5.
    * `id` : `snippet_Create` ID de l’extrait à insérer à partir du fichier de code. Cette valeur ne peut pas coexister avec la plage.
    * `highlight` : `2-4,6` Plage et/ou nombres de lignes à mettre en surbrillance dans l’extrait de code généré. La numérotation est relative aux lignes affichées (comme spécifié par la plage ou l’ID), pas au fichier.
    * `interactive`: `cloudshell-powershell`, `cloudshell-bash`, `try-dotnet`, `try-dotnet-class`, `try-dotnet-method` Valeur de chaîne qui détermine les types d’interactivité activés.
    * Pour plus d’informations sur la représentation des balises de noms dans les fichiers sources d’extrait de code selon les langages, consultez les [Instructions DocFX](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).

## <a name="supported-languages"></a>Langages pris en charge

Le [Docs Authoring Pack](how-to-write-docs-auth-pack.md) comprend une fonctionnalité qui permet d’effectuer la complétion des instructions et de valider les identificateurs de langage disponibles pour les blocs de limites de code.

### <a name="fenced-code-blocks"></a>Blocs de code délimités

| Name                           | Alias valides                                                                  |
|--------------------------------|--------------------------------------------------------------------------------|
| CLI .NET Core                  | `dotnetcli`                                                                    |
| 1C                             | `1c`                                                                           |
| ABNF                           | `abnf`                                                                         |
| Journaux d’accès                    | `accesslog`                                                                    |
| Ada                            | `ada`                                                                          |
| Assembleur ARM                  | `armasm`, `arm`                                                                |
| Assembleur AVR                  | `avrasm`                                                                       |
| ActionScript                   | `actionscript`, `as`                                                           |
| Alan                           | `alan`, `i`                                                                    |
| AngelScript                    | `angelscript`, `asc`                                                           |
| ANTLR                          | `antlr`                                                                        |
| Apache                         | `apache`, `apacheconf`                                                         |
| AppleScript                    | `applescript`, `osascript`                                                     |
| Arcade                         | `arcade`                                                                       |
| AsciiDoc                       | `asciidoc`, `adoc`                                                             |
| AspectJ                        | `aspectj`                                                                      |
| ASPX                           | `aspx`                                                                         |
| ASP.NET (C#)                   | `aspx-csharp`                                                                  |
| ASP.NET (VB)                   | `aspx-vb`                                                                      |
| AutoHotkey                     | `autohotkey`                                                                   |
| AutoIt                         | `autoit`                                                                       |
| Awk                            | `awk`, `mawk`, `nawk`, `gawk`                                                  |
| Axapta                         | `axapta`                                                                       |
| AzCopy                         | `azcopy`                                                                       |
| Azure CLI                      | `azurecli`                                                                     |
| Azure CLI (Interactive)        | `azurecli-interactive`                                                         |
| Azure PowerShell               | `azurepowershell`                                                              |
| Azure Powershell (Interactive) | `azurepowershell-interactive`                                                  |
| Bash                           | `bash`, `sh`, `zsh`                                                            |
| Basic                          | `basic`                                                                        |
| BNF                            | `bnf`                                                                          |
| C                              | `c`                                                                            |
| C#                             | `csharp`, `cs`                                                                 |
| C# (Interactive)               | `csharp-interactive`                                                           |
| C++                            | `cpp`, `c`, `cc`, `h`, `c++`, `h++`, `hpp`                                     |
| C++/CX                         | `cppcx`                                                                        |
| C++/WinRT                      | `cppwinrt`                                                                     |
| C/AL                           | `cal`                                                                          |
| Script d’objet cache            | `cos`, `cls`                                                                   |
| CMake                          | `cmake`, `cmake.in`                                                            |
| Coq                            | `coq`                                                                          |
| CSP                            | `csp`                                                                          |
| CSS                            | `css`                                                                          |
| Cap'n Proto                    | `capnproto`, `capnp`                                                           |
| Clojure                        | `clojure`, `clj`                                                               |
| CoffeeScript                   | `coffeescript`, `coffee`, `cson`, `iced`                                       |
| Crmsh                          | `crmsh`, `crm`, `pcmk`                                                         |
| Crystal                        | `crystal`, `cr`                                                                |
| Cypher (Neo4j)                 | `cypher`                                                                       |
| D                              | `d`                                                                            |
| DAX Power BI                   | `dax`                                                                          |
| Fichier de zone DNS                  | `dns`, `zone`, `bind`                                                          |
| DOS                            | `dos`, `bat`, `cmd`                                                            |
| Dart                           | `dart`                                                                         |
| Delphi                         | `delphi`, `dpr`, `dfm`, `pas`, `pascal`, `freepascal`, `lazarus`, `lpr`, `lfm` |
| Diff                           | `diff`, `patch`                                                                |
| Django                         | `django`, `jinja`                                                              |
| Dockerfile                     | `dockerfile`, `docker`                                                         |
| dsconfig                       | `dsconfig`                                                                     |
| DTS (arborescence des appareils)              | `dts`                                                                          |
| Dust                           | `dust`, `dst`                                                                  |
| Dylan                          | `dylan`                                                                        |
| EBNF                           | `ebnf`                                                                         |
| Elixir                         | `elixir`                                                                       |
| Elm                            | `elm`                                                                          |
| Erlang                         | `erlang`, `erl`                                                                |
| Excel                          | `excel`, `xls`, `xlsx`                                                         |
| Extempore                      | `extempore`, `xtlang`, `xtm`                                                   |
| F#                             | `fsharp`, `fs`                                                                 |
| FIX                            | `fix`                                                                          |
| Fortran                        | `fortran`, `f90`, `f95`                                                        |
| G-Code                         | `gcode`, `nc`                                                                  |
| Gams                           | `gams`, `gms`                                                                  |
| GAUSS                          | `gauss`, `gss`                                                                 |
| GDScript                       | `godot`, `gdscript`                                                            |
| Gherkin                        | `gherkin`                                                                      |
| GN for Ninja                   | `gn`, `gni`                                                                    |
| Go                             | `go`, `golang`                                                                 |
| Golo                           | `golo`, `gololang`                                                             |
| Gradle                         | `gradle`                                                                       |
| Groovy                         | `groovy`                                                                       |
| HTML                           | `html`, `xhtml`                                                                |
| HTTP                           | `http`, `https`                                                                |
| Haml                           | `haml`                                                                         |
| Handlebars                     | `handlebars`, `hbs`, `html.hbs`, `html.handlebars`                             |
| Haskell                        | `haskell`, `hs`                                                                |
| Haxe                           | `haxe`, `hx`                                                                   |
| Hy                             | `hy`, `hylang`                                                                 |
| Ini                            | `ini`                                                                          |
| Inform7                        | `inform7`, `i7`                                                                |
| IRPF90                         | `irpf90`                                                                       |
| JSON                           | `json`                                                                         |
| Java                           | `java`, `jsp`                                                                  |
| JavaScript                     | `javascript`, `js`, `jsx`                                                      |
| Kotlin                         | `kotlin`, `kt`                                                                 |
| Kusto                          | `kusto`                                                                        |
| Leaf                           | `leaf`                                                                         |
| Lasso                          | `lasso`, `ls`, `lassoscript`                                                   |
| Less                           | `less`                                                                         |
| LDIF                           | `ldif`                                                                         |
| Lisp                           | `lisp`                                                                         |
| LiveCode Server                | `livecodeserver`                                                               |
| LiveScript                     | `livescript`, `ls`                                                             |
| Lua                            | `lua`                                                                          |
| Makefile                       | `makefile`, `mk`, `mak`                                                        |
| Markdown                       | `markdown`, `md`, `mkdown`, `mkd`                                              |
| Mathematica                    | `mathematica`, `mma`, `wl`                                                     |
| Matlab                         | `matlab`                                                                       |
| Maxima                         | `maxima`                                                                       |
| Maya Embedded Language         | `mel`                                                                          |
| Mercury                        | `mercury`                                                                      |
| mIRC Scripting Language        | `mirc`, `mrc`                                                                  |
| Mizar                          | `mizar`                                                                        |
| Format MOF (Managed Object Format)          | `mof`                                                                          |
| Mojolicious                    | `mojolicious`                                                                  |
| Monkey                         | `monkey`                                                                       |
| Moonscript                     | `moonscript`, `moon`                                                           |
| MS Graph (Interactive)         | `msgraph-interactive`                                                          |
| N1QL                           | `n1ql`                                                                         |
| NSIS                           | `nsis`                                                                         |
| Nginx                          | `nginx`, `nginxconf`                                                           |
| Nimrod                         | `nimrod`, `nim`                                                                |
| Nix                            | `nix`                                                                          |
| OCaml                          | `ocaml`, `ml`                                                                  |
| Objective C                    | `objectivec`, `mm`, `objc`, `obj-c`                                            |
| OpenGL Shading Language        | `glsl`                                                                         |
| OpenSCAD                       | `openscad`, `scad`                                                             |
| Oracle Rules Language          | `ruleslanguage`                                                                |
| Oxygene                        | `oxygene`                                                                      |
| PF                             | `pf`, `pf.conf`                                                                |
| PHP                            | `php`, `php3`, `php4`, `php5`, `php6`                                          |
| Parser3                        | `parser3`                                                                      |
| Perl                           | `perl`, `pl`, `pm`                                                             |
| Plaintext no highlight         | `plaintext`                                                                    |
| Pony                           | `pony`                                                                         |
| PostgreSQL & PL/pgSQL          | `pgsql`, `postgres`, `postgresql`                                              |
| PowerShell                     | `powershell`, `ps`                                                             |
| PowerShell (Interactive)       | `powershell-interactive`                                                       |
| Processing                     | `processing`                                                                   |
| Prolog                         | `prolog`                                                                       |
| Propriétés                     | `properties`                                                                   |
| Protocol Buffers               | `protobuf`                                                                     |
| Puppet                         | `puppet`, `pp`                                                                 |
| Python                         | `python`, `py`, `gyp`                                                          |
| Résultats de profileur Python        | `profile`                                                                      |
| Q#                             | `qsharp`                                                                       |
| Q                              | `k`, `kdb`                                                                     |
| QML                            | `qml`                                                                          |
| R                              | `r`                                                                            |
| Razor CSHTML                   | `cshtml`, `razor`, `razor-cshtml`                                              |
| ReasonML                       | `reasonml`, `re`                                                               |
| RenderMan RIB                  | `rib`                                                                          |
| RenderMan RSL                  | `rsl`                                                                          |
| Roboconf                       | `graph`, `instances`                                                           |
| Robot Framework                | `robot`, `rf`                                                                  |
| Fichiers de spécifications RPM                 | `rpm-specfile`, `rpm`, `spec`, `rpm-spec`, `specfile`                          |
| Ruby                           | `ruby`, `rb`, `gemspec`, `podspec`, `thor`, `irb`                              |
| Rust                           | `rust`, `rs`                                                                   |
| SAS                            | `SAS`, `sas`                                                                   |
| SCSS                           | `scss`                                                                         |
| SQL                            | `sql`                                                                          |
| STEP Part 21                   | `p21`, `step`, `stp`                                                           |
| Scala                          | `scala`                                                                        |
| Scheme                         | `scheme`                                                                       |
| Scilab                         | `scilab`, `sci`                                                                |
| Shape Expressions              | `shexc`                                                                        |
| Interpréteur de commandes                          | `shell`, `console`                                                             |
| Smali                          | `smali`                                                                        |
| Smalltalk                      | `smalltalk`, `st`                                                              |
| Solidity                       | `solidity`, `sol`                                                              |
| Stan                           | `stan`                                                                         |
| Stata                          | `stata`                                                                        |
| Texte structuré                | `iecst`, `scl`, `stl`, `structured-text`                                       |
| Stylus                         | `stylus`, `styl`                                                               |
| SubUnit                        | `subunit`                                                                      |
| Supercollider                  | `supercollider`, `sc`                                                          |
| Swift                          | `swift`                                                                        |
| Tcl                            | `tcl`, `tk`                                                                    |
| Terraform (HCL)                | `terraform`, `tf`, `hcl`                                                       |
| Test Anything Protocol         | `tap`                                                                          |
| TeX                            | `tex`                                                                          |
| Thrift                         | `thrift`                                                                       |
| TOML                           | `toml`                                                                         |
| TP                             | `tp`                                                                           |
| Twig                           | `twig`, `craftcms`                                                             |
| TypeScript                     | `typescript`, `ts`                                                             |
| VB.NET                         | `vbnet`, `vb`                                                                  |
| VBScript                       | `vbscript`, `vbs`                                                              |
| VHDL                           | `vhdl`                                                                         |
| Vala                           | `vala`                                                                         |
| Verilog                        | `verilog`, `v`                                                                 |
| Vim Script                     | `vim`                                                                          |
| X++                            | `xpp`                                                                          |
| Langage assembleur x86                   | `x86asm`                                                                       |
| XL                             | `xl`, `tao`                                                                    |
| XQuery                         | `xquery`, `xpath`, `xq`                                                        |
| XAML                           | `xaml`                                                                         |
| XML                            | `xml`, `xhtml`, `rss`, `atom`, `xjb`, `xsd`, `xsl`, `plist`                    |
| YAML                           | `yml`, `yaml`                                                                  |
| Zephir                         | `zephir`, `zep`                                                                |

> [!TIP]
> La [fonctionnalité de complétion des langages de développement](docs-authoring/dev-lang-completion.md) de Docs Authoring Pack utilise le premier alias valide quand plusieurs alias sont disponibles.

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur la mise en forme du texte pour les types de contenu autres que le code, consultez [instructions de mise en forme du texte](text-formatting-guidelines.md).
