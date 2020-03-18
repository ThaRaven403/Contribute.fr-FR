---
title: Complétion des langages de développement - Docs Authoring Pack
description: Découvrez comment la complétion des langages de développement aide les contributeurs de l’extension Visual Studio Code Docs Authoring Pack.
author: scottaddie
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.date: 03/03/2020
ms.author: scaddie
ms.openlocfilehash: f81dc2315dc09256639c98ed72484517ff2c6ff3
ms.sourcegitcommit: dbc2c48194e29bfa0c88d33f50f94b9ee26be2da
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "78336793"
---
# <a name="dev-lang-completion"></a><span data-ttu-id="0d0e5-103">Complétion des langages de développement</span><span class="sxs-lookup"><span data-stu-id="0d0e5-103">Dev lang completion</span></span>

[!INCLUDE [markdown-extension](includes/markdown-extension.md)]

## <a name="summary"></a><span data-ttu-id="0d0e5-104">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="0d0e5-104">Summary</span></span>

<span data-ttu-id="0d0e5-105">Les contributeurs ont besoin d’aide pour déterminer les identificateurs de langage valide (langages de développement) qui peuvent suivre les trois accents graves (ouvertures de délimitation de code) dans un fichier Markdown.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-105">Contributors need assistance determining the valid language identifiers (dev langs) that can follow triple-backticks (code fence openings) in a Markdown file.</span></span> <span data-ttu-id="0d0e5-106">Malheureusement, il n’existe pas de validation des langages de développement au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-106">Unfortunately, build-time validation of dev langs doesn't exist.</span></span> <span data-ttu-id="0d0e5-107">Il en résulte des représentations disparates d’un même langage au sein du même docset conceptuel.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-107">The result is disparate representations of a single language within the same conceptual docset.</span></span>

<span data-ttu-id="0d0e5-108">Prenons C# à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-108">Consider C# as an example.</span></span> <span data-ttu-id="0d0e5-109">Les contributeurs ont utilisé `c#`, `C#`, `cs`, `csharp`, entre autres, comme représentations du langage de développement.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-109">Contributors have used `c#`, `C#`, `cs`, `csharp`, and others as dev lang representations of the language.</span></span> <span data-ttu-id="0d0e5-110">Laquelle des représentations précédentes est correcte ?</span><span class="sxs-lookup"><span data-stu-id="0d0e5-110">Which of the preceding representations is correct?</span></span>

<span data-ttu-id="0d0e5-111">La fonctionnalité *Dev lang completion* (Complétion des langages de développement) dissipe la confusion en affichant une liste des langages de développement connus.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-111">The *Dev lang completion* feature dispels the confusion by displaying a list of known dev langs.</span></span> <span data-ttu-id="0d0e5-112">Lors de la sélection d’un nom de langage de développement dans IntelliSense :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-112">Upon selecting a dev lang name from IntelliSense:</span></span>

* <span data-ttu-id="0d0e5-113">La délimitation de code est fermée.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-113">The code fence is closed.</span></span>
* <span data-ttu-id="0d0e5-114">Le signe insertion est positionné dans la délimitation de code.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-114">The caret is positioned in the code fence.</span></span>

## <a name="preferences"></a><span data-ttu-id="0d0e5-115">Préférences</span><span class="sxs-lookup"><span data-stu-id="0d0e5-115">Preferences</span></span>

<span data-ttu-id="0d0e5-116">Il n’est pas possible de désactiver cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-116">It's not possible to disable this feature.</span></span> <span data-ttu-id="0d0e5-117">Les paramètres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-117">The following settings are available:</span></span>

* [<span data-ttu-id="0d0e5-118">Afficher les langages de développement couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="0d0e5-118">Display commonly used dev langs</span></span>](#display-commonly-used-dev-langs)
* [<span data-ttu-id="0d0e5-119">Afficher tous les langages de développement connus</span><span class="sxs-lookup"><span data-stu-id="0d0e5-119">Display all known dev langs</span></span>](#display-all-known-dev-langs)

### <a name="display-commonly-used-dev-langs"></a><span data-ttu-id="0d0e5-120">Afficher les langages de développement couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="0d0e5-120">Display commonly used dev langs</span></span>

<span data-ttu-id="0d0e5-121">Seule une partie des langages de développement valides est utilisé dans un même docset.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-121">Only a subset of the valid dev langs will be used in a single docset.</span></span> <span data-ttu-id="0d0e5-122">Pour améliorer l’expérience utilisateur :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-122">To enhance the user experience:</span></span>

1. <span data-ttu-id="0d0e5-123">Dans Visual Studio Code, ouvrez le docset dans le répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-123">In Visual Studio Code, open the docset to the root directory.</span></span>
1. <span data-ttu-id="0d0e5-124">Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-124">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="0d0e5-125">Cliquez sur le lien **Edit in settings.json** (Modifier dans settings.json) dans la section **Markdown: Docset Languages** (Markdown : Langage du docset).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-125">Click the **Edit in settings.json** link in the **Markdown: Docset Languages** section.</span></span>
1. <span data-ttu-id="0d0e5-126">Ajoutez la propriété `markdown.docsetLanguages` suivante au fichier *settings.json* :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-126">Add the following `markdown.docsetLanguages` property to the *settings.json* file:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [

        ]
    }
    ```

1. <span data-ttu-id="0d0e5-127">Placez le signe insertion dans le tableau vide de la propriété, puis activez IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Espace</kbd>).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-127">Position your caret in the property's empty array, and activate IntelliSense (via <kbd>Ctrl</kbd> + <kbd>Space</kbd>).</span></span> <span data-ttu-id="0d0e5-128">Une liste de noms de langage de développement connus s’affiche.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-128">A list of known dev lang names appears.</span></span>
1. <span data-ttu-id="0d0e5-129">Ajoutez des noms de langage de développement au tableau jusqu’à ce que vous soyez satisfait de la liste.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-129">Add dev lang names to the array until you're satisfied with the list.</span></span> <span data-ttu-id="0d0e5-130">Par exemple, la liste suivante présente quatre noms de langage de développement à l’utilisateur après la saisie de trois accents graves :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-130">For example, the following list will display four dev lang names to the user after typing triple-ticks:</span></span>

    ```json
    {
        "markdown.docsetLanguages": [
            ".NET Core CLI",
            "C#",
            "Markdown",
            "YAML"
        ]
    }
    ```

1. <span data-ttu-id="0d0e5-131">Enregistrez les modifications apportées au fichier *settings.json*.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-131">Save your changes to the *settings.json* file.</span></span>

> [!WARNING]
> <span data-ttu-id="0d0e5-132">Un tableau `markdown.docsetLanguages` vide provoque l’affichage de tous les langages de développement connus.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-132">An empty `markdown.docsetLanguages` array causes all known dev langs to display.</span></span>

### <a name="display-all-known-dev-langs"></a><span data-ttu-id="0d0e5-133">Afficher tous les langages de développement connus</span><span class="sxs-lookup"><span data-stu-id="0d0e5-133">Display all known dev langs</span></span>

<span data-ttu-id="0d0e5-134">Par défaut, tous les noms de langage de développement connus sont affichés dans IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="0d0e5-134">By default, all known dev lang names are displayed in IntelliSense.</span></span> <span data-ttu-id="0d0e5-135">Ce paramètre remplace la propriété `markdown.docsetLanguages` décrite dans [Afficher les langages de développement couramment utilisés](#display-commonly-used-dev-langs).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-135">This setting overrides the `markdown.docsetLanguages` property described in [Display commonly used dev langs](#display-commonly-used-dev-langs).</span></span>

<span data-ttu-id="0d0e5-136">Pour changer ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-136">To change this setting:</span></span>

1. <span data-ttu-id="0d0e5-137">Sélectionnez **Fichier** > **Préférences** > **Paramètres** et filtrez par *Docs Markdown Extension* (Extension Docs Markdown).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-137">Select **File** > **Preferences** > **Settings** and filter by *Docs Markdown Extension*.</span></span>
1. <span data-ttu-id="0d0e5-138">Activez/désactivez le paramètre dans la section **Markdown : All Available Languages** (Markdown : Tous les langages disponibles).</span><span class="sxs-lookup"><span data-stu-id="0d0e5-138">Toggle the setting in the **Markdown: All Available Languages** section.</span></span>

## <a name="in-action"></a><span data-ttu-id="0d0e5-139">En action</span><span class="sxs-lookup"><span data-stu-id="0d0e5-139">In action</span></span>

<span data-ttu-id="0d0e5-140">Vous trouverez ci-dessous une brève démonstration de cette fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="0d0e5-140">Below is a brief demonstration of this feature:</span></span>

<span data-ttu-id="0d0e5-141">[![Complétion des langages de développement](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0d0e5-141">[![Dev lang completion](media/dev-lang-completion.gif)](media/dev-lang-completion.gif#lightbox)</span></span>
