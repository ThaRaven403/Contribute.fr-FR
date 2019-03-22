---
ms.openlocfilehash: fa7cd177f6c4a3c4862677dbfa89f63a91e7f464
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987810"
---
# <a name="tabbed-conceptual"></a>Conception à onglets

> [!IMPORTANT]
> La syntaxe conceptuelle à onglets ayant été dépréciée, n’ajoutez pas de nouveaux onglets. Les validations décrites dans cet article s’appliquent aux ensembles de contenus autorisés à utiliser une conception à onglets jusqu’à ce qu’une fonctionnalité de remplacement soit disponible.

## <a name="tab-syntax"></a>Syntaxe des onglets

La syntaxe des onglets est la suivante :

Onglet à un niveau :

`# [Tab Display Name](#tab/tab-id)`

Onglet dépendant facultatif :

`# [Tab Display Name](#tab/tab-id/tab-condition)`

Exemple d’une section d’onglets à un niveau avec deux onglets et le terminateur de groupe d’onglets (---) :

```markdown
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

Les onglets peuvent éventuellement contenir des onglets secondaires (ou onglets de dépendance). Les onglets dépendent alors de la sélection dans un autre ensemble d’onglets. Voici un exemple :

```markdown
# [Azure CLI](#tab/azure-cli/linux)

Azure CLI content for Linux...

# [Azure CLI](#tab/azure-cli/windows)

Azure CLI content for Windows...

# [PowerShell](#tab/azure-powershell/linux)

PowerShell content for Linux...

# [PowerShell](#tab/azure-powershell/windows)

PowerShell content for Windows...

---
```

Les validations suivantes s’appliquent à la syntaxe des onglets :

- La syntaxe des onglets doit être correcte.
- Les onglets dépendants doivent avoir été définis dans un groupe d’onglets précédent.
- Un seul niveau de dépendance est autorisé.
- Le nombre minimum d’onglets autorisés est de deux.
- Le nombre maximum d’onglets autorisés est de quatre.
- Les onglets doivent être approuvés.
- Les paires onglet/ID doivent être valides.
- Un groupe d’onglets ne peut pas contenir plusieurs ID d’onglet identiques.

## <a name="approved-tabs"></a>Onglets approuvés

Les paires nom d’onglet/ID d’onglet suivantes sont approuvées. Les ID d’onglets dépendants ne sont pas associés, mais ils doivent être valides conformément à la colonne ID de l’onglet. Les valeurs respectent la casse.

|Nom de l’onglet              |ID de l’onglet            |
|----------------------|------------------|
|`[.NET]`              |`(#tab/dotnet)`   |
|`[.NET Core 1.x]`     |`(#tab/netcore1x)`|
|`[.NET Core 2.x]`     |`(#tab/netcore2x)`|
|`[.NET Core 2.0]`     |`(#tab/netcore20)`|
|`[.NET Core 2.1]`     |`(#tab/netcore21)`|
|`[.NET Core 2.2]`     |`(#tab/netcore22)`|
|`[.NET Core 3.x]`     |`(#tab/netcore3x)`|
|`[.NET Core 3.0]`     |`(#tab/netcore30)`|
|`[.NET Core CLI]`     |`(#tab/netcore-cli)`|
|`[Azure CLI]`         |`(#tab/azure-cli)`|
|`[Android]`           |`(#tab/android)`  |
|`[Browser]`           |`(#tab/browser)`  |
|`[C#]`                |`(#tab/csharp)`   |
|`[C# Script]`         |`(#tab/csharp-script)`|
|`[CentOS]`            |`(#tab/centos)`|
|`[Command Line]`      |`(#tab/command-line)`|
|`[Debian]`            |`(#tab/debian)`|
|`[Docker Hub]`        |`(#tab/docker-hub)`|
|`[F#]`                |`(#tab/fsharp)`|
|`[Fedora]`            |`(#tab/fedora)`|
|`[iOS]`               |`(#tab/ios)`      |
|`[Java]`              |`(#tab/java)`|
|`[JavaScript]`        |`(#tab/javascript)`|
|`[Linux]`             |`(#tab/linux)`    |
|`[macOS]`             |`(#tab/macos)`    |
|`[Managed Kubernetes]`|`(#tab/kubernetes-managed)`|
|`[Maven]`             |`(#tab/maven)`|
|`[Mint]`              |`(#tab/mint)`|
|`[Node.js]`           |`(#tab/nodejs)`|
|`[npm]`               |`(#tab/npm)` |
|`[NuGet]`             |`(#tab/nuget)`|
|`[openSUSE]`          |`(#tab/opensuse)`|
|`[Other]`             |`(#tab/other)` |
|`[Oracle Linux]`      |`(#tab/oracle-linux)`|
|`[Package Manager]`   |`(#tab/package-manager)` |
|`[PEAR]`              |`(#tab/pear)`|
|`[pip]`               |`(#tab/pip)`|
|`[Portal]`            |`(#tab/azure-portal)`    |
|`[PowerShell]`        |`(#tab/azure-powershell)`|
|`[Private Registry]`  |`(#tab/private-registry)`|
|`[Python]`            |`(#tab/python)`|
|`[Resource Manager Template]`|`(#tab/azure-resource-manager)`|
|`[RHEL]`              |`(#tab/rhel)`|
|`[RubyGems]`          |`(#tab/rubygems)`|
|`[SQL Server]`        |`(#tab/sql-server)`|
|`[SQLite]`            |`(#tab/sqlite)`|
|`[TypeScript]`        |`(#tab/typescript)`|
|`[Visual Basic]`      |`(#tab/vb)` |
|`[Visual Studio]`     |`(#tab/visual-studio)`|
|`[Visual Studio 15.6 and earlier]`|`(#tab/vs156)`|
|`[Visual Studio 15.7 and later]`  |`(#tab/vs157)`|
|`[Visual Studio Code]`            |`(#tab/visual-studio-code)`|
|`[Visual Studio for Mac]`         |`(#tab/visual-studio-mac)`|
|`[Ubuntu]`                        |`(#tab/ubuntu)`|
|`[Unmanaged Kubernetes]`          |`(#tab/kubernetes-unmanaged)`|
|`[Windows]`   |`(#tab/windows)`   |