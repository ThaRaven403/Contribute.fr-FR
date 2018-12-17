# <a name="tabbed-conceptual"></a><span data-ttu-id="6b905-101">Conception à onglets</span><span class="sxs-lookup"><span data-stu-id="6b905-101">Tabbed conceptual</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b905-102">La syntaxe conceptuelle à onglets ayant été dépréciée, n’ajoutez pas de nouveaux onglets.</span><span class="sxs-lookup"><span data-stu-id="6b905-102">The tabbed conceptual syntax has been deprecated and new tabs should not be added.</span></span> <span data-ttu-id="6b905-103">Les validations décrites dans cet article s’appliquent aux ensembles de contenus autorisés à utiliser une conception à onglets jusqu’à ce qu’une fonctionnalité de remplacement soit disponible.</span><span class="sxs-lookup"><span data-stu-id="6b905-103">The validations described in this article apply to content sets that have been approved to use tabbed conceptual until replacement functionality is available.</span></span>

## <a name="tab-syntax"></a><span data-ttu-id="6b905-104">Syntaxe des onglets</span><span class="sxs-lookup"><span data-stu-id="6b905-104">Tab syntax</span></span>

<span data-ttu-id="6b905-105">La syntaxe des onglets est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6b905-105">The syntax for tabs is as follows:</span></span>

<span data-ttu-id="6b905-106">Onglet à un niveau :</span><span class="sxs-lookup"><span data-stu-id="6b905-106">Single level tab:</span></span>

`# [Tab Display Name](#tab/tab-id)`

<span data-ttu-id="6b905-107">Onglet dépendant facultatif :</span><span class="sxs-lookup"><span data-stu-id="6b905-107">Optional dependent tab:</span></span>

`# [Tab Display Name](#tab/tab-id/tab-condition)`

<span data-ttu-id="6b905-108">Exemple d’une section d’onglets à un niveau avec deux onglets et le terminateur de groupe d’onglets (---) :</span><span class="sxs-lookup"><span data-stu-id="6b905-108">Example of a single-level tab section with two tabs and the tab group terminator (---):</span></span>

```
# [Linux](#tab/linux)

Content for Linux...

# [Windows](#tab/windows)

Content for Windows...

---
```

<span data-ttu-id="6b905-109">Les onglets peuvent éventuellement contenir des onglets secondaires (ou onglets de dépendance).</span><span class="sxs-lookup"><span data-stu-id="6b905-109">Tabs can optionally contain secondary tabs, or dependency tabs.</span></span> <span data-ttu-id="6b905-110">Les onglets dépendent alors de la sélection dans un autre ensemble d’onglets.</span><span class="sxs-lookup"><span data-stu-id="6b905-110">This makes tabs dependent on the selection in another set of tabs.</span></span> <span data-ttu-id="6b905-111">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="6b905-111">Here's an example:</span></span>

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

<span data-ttu-id="6b905-112">Les validations suivantes s’appliquent à la syntaxe des onglets :</span><span class="sxs-lookup"><span data-stu-id="6b905-112">The following validations apply to tab syntax:</span></span>

- <span data-ttu-id="6b905-113">La syntaxe des onglets doit être correcte.</span><span class="sxs-lookup"><span data-stu-id="6b905-113">Tab syntax must be correct.</span></span>
- <span data-ttu-id="6b905-114">Les onglets dépendants doivent avoir été définis dans un groupe d’onglets précédent.</span><span class="sxs-lookup"><span data-stu-id="6b905-114">Dependent tabs must have been defined in a previous tab group.</span></span>
- <span data-ttu-id="6b905-115">Un seul niveau de dépendance est autorisé.</span><span class="sxs-lookup"><span data-stu-id="6b905-115">Only one level of dependency is allowed.</span></span>
- <span data-ttu-id="6b905-116">Le nombre minimum d’onglets autorisés est de deux.</span><span class="sxs-lookup"><span data-stu-id="6b905-116">No fewer than two tabs are allowed.</span></span>
- <span data-ttu-id="6b905-117">Le nombre maximum d’onglets autorisés est de quatre.</span><span class="sxs-lookup"><span data-stu-id="6b905-117">No more than four tabs are allowed.</span></span>
- <span data-ttu-id="6b905-118">Les onglets doivent être sur liste verte.</span><span class="sxs-lookup"><span data-stu-id="6b905-118">Tabs must be whitelisted.</span></span>
- <span data-ttu-id="6b905-119">Les paires onglet/ID doivent être valides.</span><span class="sxs-lookup"><span data-stu-id="6b905-119">Tab/ID pairs must be valid.</span></span>
- <span data-ttu-id="6b905-120">Un groupe d’onglets ne peut pas contenir plusieurs ID d’onglet identiques.</span><span class="sxs-lookup"><span data-stu-id="6b905-120">Cannot have the same tab ID multiple times in one tab group.</span></span>

## <a name="tab-whitelist"></a><span data-ttu-id="6b905-121">Liste verte d’onglets</span><span class="sxs-lookup"><span data-stu-id="6b905-121">Tab whitelist</span></span>

<span data-ttu-id="6b905-122">Les paires nom d’onglet/ID d’onglet suivantes sont sur liste verte.</span><span class="sxs-lookup"><span data-stu-id="6b905-122">The following tab name/tab ID pairs are whitelisted.</span></span> <span data-ttu-id="6b905-123">Les ID d’onglets dépendants ne sont pas associés, mais ils doivent être valides conformément à la colonne ID de l’onglet.</span><span class="sxs-lookup"><span data-stu-id="6b905-123">Dependent tab IDs are not paired but must be valid per the Tab ID column.</span></span> <span data-ttu-id="6b905-124">Les valeurs respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6b905-124">The values are case-sensitive</span></span>

|<span data-ttu-id="6b905-125">Nom de l’onglet</span><span class="sxs-lookup"><span data-stu-id="6b905-125">Tab name</span></span>              |<span data-ttu-id="6b905-126">ID de l’onglet</span><span class="sxs-lookup"><span data-stu-id="6b905-126">Tab ID</span></span>            |
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