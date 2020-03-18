---
title: Instructions de mise en forme du texte
description: Découvrez comment utiliser le style gras, italique, code et autres dans les articles publiés sur le site docs.microsoft.com.
author: tdykstra
ms.author: tdykstra
ms.date: 01/30/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 7b6927918c81fdc41e3c3887f94339b225e2a6e6
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336500"
---
# <a name="text-formatting-guidelines"></a>Instructions de mise en forme du texte

L’utilisation cohérente et appropriée du style gras, italique et code pour les éléments de texte améliore la lisibilité et permet d’éviter les confusions.

## <a name="bold"></a>Gras

Utilisez le gras pour les éléments de l’interface utilisateur, comme les sélections de menu, les noms de boîte de dialogue et les noms de champ d’entrée.

### <a name="examples"></a>Exemples

* **Appliquez** : Dans l’**Explorateur de solutions**, cliquez avec le bouton droit sur le nœud du projet et sélectionnez **Ajouter > Nouvel élément**.
* **N’appliquez pas** : Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le nœud du projet et sélectionnez Ajouter > Nouvel élément.
* **N’appliquez pas** : Dans l’*Explorateur de solutions*, cliquez avec le bouton droit sur le nœud du projet et sélectionnez *Ajouter > Nouvel élément*.

## <a name="italics"></a>Italique

Utilisez l’italique pour :

* Présentation de nouveaux termes avec une définition ou une explication.
* Les noms de fichier, les noms de dossier, les chemins.
* Entrée utilisateur.

### <a name="examples"></a>Exemples

* **Appliquez** : Dans App Service, une application s’exécute dans un *plan App Service*. Un plan App Service définit un ensemble de ressources de calcul nécessaires à l’exécution d’une application web.
* **N’appliquez pas** : Dans App Service, une application s’exécute dans un « plan App Service ». Un plan App Service définit un ensemble de ressources de calcul nécessaires à l’exécution d’une application web.
* **Appliquez** : Remplacez le code dans *HttpTriggerCSharp.cs* par le code suivant.
* **N’appliquez pas** : Remplacez le code présent dans `HttpTriggerCSharp.cs` par le code suivant.
* **Appliquez** : Entrez *ContosoUniversity* pour **Nom**, puis sélectionnez **Ajouter**.
* **N’appliquez pas** : Entrez « ContosoUniversity » pour **Nom**, puis sélectionnez **Ajouter**.

## <a name="code-style"></a>Style code

Utiliser le style code pour :

* Les éléments de code, comme les noms de méthode, les noms de propriétés et les mots clés du langage.
* Commandes SQL
* Les noms de package NuGet
* Les commandes de ligne de commande
* Les noms de table et de colonne des bases de données
* Noms de ressources qui ne doivent pas être localisés (tels que les noms de machine virtuelle)
* Les URL que vous ne souhaitez pas cliquables

**Pourquoi ?** Les anciens guides de style spécifient le gras pour la plupart de ces éléments de texte. Toutefois, la plupart des articles sont localisés et le style code indique au traducteur de conserver cette partie du texte non traduite.

Le style code peut apparaître *inline* (entouré de \`) ou dans des blocs de code *délimités* (entouré de \`\`\`) englobant plusieurs lignes. Placez les extraits de code et les chemins plus longs dans des blocs de code délimités.

### <a name="examples-using-inline-styles"></a>Exemples utilisant des styles intralignes

* **Appliquez** : Par défaut, Entity Framework interprète une propriété nommée `Id` ou `ClassnameID` comme étant la clé primaire.
* **N’appliquez pas** : Par défaut, Entity Framework interprète une propriété nommée *Id* ou *ClassnameID* comme étant la clé primaire.
* **Appliquez** : Le package `Microsoft.EntityFrameworkCore` prend en charge l’exécution d’EF Core.
* **N’appliquez pas** : Le package *Microsoft.EntityFrameworkCore* prend en charge l’exécution d’EF Core.

### <a name="examples-of-fenced-code-blocks"></a>Exemples de blocs de code délimités

* **Appliquez** : Aucune commande n’est envoyée à la base de données par des instructions qui changent juste `IQueryable`, comme le code suivant :

  ```markdown
      ```csharp
      var students = context.Students.Where(s => s.LastName == "Davolio")
      ```
  ```

* **N’appliquez pas** : Aucune commande n’est envoyée à la base de données par des instructions qui changent juste **IQueryable**, comme **var students = context.Students.Where(s => s.LastName == "Davolio")** .

* **Appliquez** : Par exemple, pour exécuter le script `Get-ServiceLog.ps1` dans le répertoire `C:\Scripts`, tapez :

  ```markdown
      ```powershell
      C:\Scripts\Get-ServiceLog.ps1
      ```
  ```

* **N’appliquez pas** : Par exemple, pour exécuter le script **Get-ServiceLog.ps1** dans le répertoire **C:\Scripts**, tapez : "C:\Scripts\Get-ServiceLog.ps1."

* **Tous** les blocs de code délimités doivent avoir une balise de langue approuvée. Pour obtenir la liste des balises de langue de prise en charge, consultez [Inclure du code dans la documentation](./code-in-docs.md#supported-languages).

## <a name="headings-and-link-text"></a>Titres et texte des liens

N’appliquez aucun style intraligne italique, gras ou code aux titres ni aux liens hypertexte.

**Pourquoi ?**

Les personnes se fient au texte de lien hypertexte standard pour identifier les éléments de texte comme des liens cliquables. Par exemple, le style code appliqué à un lien peut masquer le fait que le texte est un lien. Les titres ont leur propre style et leur en ajouter d’autres ne donne pas un bon résultat.

### <a name="examples"></a>Exemples

* **Appliquez** : Le fichier *function.json* est généré par le package NuGet [Microsoft.NET.Sdk.Functions](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).
* **N’appliquez pas** : Le fichier *function.json* est généré par le package NuGet [`Microsoft.NET.Sdk.Functions`](http://www.nuget.org/packages/Microsoft.NET.Sdk.Functions).

* **Appliquez** :

  ```markdown
  ### The Microsoft.NET.Sdk.Functions package
  ```

* **N’appliquez pas** :

  ```markdown
  ### The `Microsoft.NET.Sdk.Functions` package
  ```

## <a name="keys-and-keyboard-shortcuts"></a>Touches et raccourcis clavier

Quand vous faites référence à des touches ou à des combinaisons de touches, respectez les conventions suivantes :

* Mettez en majuscule la première lettre des noms de touches.
* N’appliquez aucun style intraligne italique, gras ou code.
* Utilisez « + » pour combiner des touches qui sont enfoncées en même temps.

### <a name="examples"></a>Exemples

* **Appliquez** : Sélectionnez Alt+Ctrl+S.
* **N’appliquez pas** : Appuyez sur **ALT+CTRL+S**.
* **N’appliquez pas** : Appuyez sur `ALT+CTRL+S`.

Pour plus d’informations, consultez [Description des interactions avec l’interface utilisateur](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2700&topicid=26472).

## <a name="exceptions"></a>Exceptions

Les instructions sur les styles ne sont pas des règles strictes. Dans les contextes où elles nuisent à la lisibilité, opérez différemment. Par exemple, un tableau HTML avec principalement des éléments de code peut paraître trop chargé avec du style code partout. Vous pouvez choisir le style gras dans ce contexte.

Si vous choisissez un style de texte de remplacement où le code est normalement appelé, assurez-vous que le texte peut être traduit dans les versions localisées de l’article. Le style code est le seul style qui empêche systématiquement la traduction du texte. Pour les scénarios où vous souhaitez empêcher la localisation sans utiliser le style code, consultez [Chaînes non localisées](markdown-reference.md#non-localized-strings).
