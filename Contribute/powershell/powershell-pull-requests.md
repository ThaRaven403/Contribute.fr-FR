---
title: Envoi d’une demande de tirage (pull request)
description: Cet article décrit le processus de demande de tirage et les bonnes pratiques pour garantir que votre contribution peut être fusionnée.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: sdwheeler
ms.author: sewhee
ms.date: 10/09/2019
ms.openlocfilehash: 09b9fd1057a32c8d2755e07cac564eca417bd357
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72290078"
---
# <a name="best-practices-for-pull-requests"></a><span data-ttu-id="5daca-103">Bonnes pratiques pour les demandes de tirage</span><span class="sxs-lookup"><span data-stu-id="5daca-103">Best Practices for Pull requests</span></span>

<span data-ttu-id="5daca-104">Pour publier des modifications au contenu, vous devez envoyer une requête de tirage pour votre embranchement.</span><span class="sxs-lookup"><span data-stu-id="5daca-104">To publish changes to content, you submit a pull request from your fork.</span></span> <span data-ttu-id="5daca-105">Chaque demande de tirage doit être révisée avant de pouvoir être fusionnée.</span><span class="sxs-lookup"><span data-stu-id="5daca-105">Every pull request has to be reviewed before it can merged.</span></span>

## <a name="target-the-correct-branch"></a><span data-ttu-id="5daca-106">Cibler la branche correcte</span><span class="sxs-lookup"><span data-stu-id="5daca-106">Target the correct branch</span></span>

<span data-ttu-id="5daca-107">Tous les changements doivent être apportés à la branche `staging`.</span><span class="sxs-lookup"><span data-stu-id="5daca-107">All changes should be made to the `staging` branch.</span></span> <span data-ttu-id="5daca-108">Les changements ne doivent jamais être ciblés sur la branche `live`.</span><span class="sxs-lookup"><span data-stu-id="5daca-108">Changes should never be targeted at the `live` branch.</span></span> <span data-ttu-id="5daca-109">Les changements apportés à la branche `staging` sont fusionnés dans `live`, de sorte que tous les changements apportés à `live` sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="5daca-109">Changes made in the `staging` branch get merged into `live` so any changes made to `live` are overwritten.</span></span>

<span data-ttu-id="5daca-110">Si vous envoyez un changement à la documentation qui s’applique seulement à une version non publiée de PowerShell, vérifiez s’il existe une branche de publication (release) pour cette version.</span><span class="sxs-lookup"><span data-stu-id="5daca-110">If you are submitting a change to documentation that only applies to an unreleased version of PowerShell, check to see if there is a release branch for that version.</span></span> <span data-ttu-id="5daca-111">Tous les changements qui s’appliquent à une version ultérieure spécifique doivent être ciblés sur la branche de la publication (release).</span><span class="sxs-lookup"><span data-stu-id="5daca-111">All changes that apply to a specific, future version should be targeted at the release branch.</span></span> <span data-ttu-id="5daca-112">Les branches de publication (release) ont le modèle de nom suivant : `release-<version>`.</span><span class="sxs-lookup"><span data-stu-id="5daca-112">Release branches have the following name pattern: `release-<version>`.</span></span>

## <a name="make-the-pull-request-queue-work-better-for-everyone"></a><span data-ttu-id="5daca-113">Aidez la file d'attente de requêtes à mieux fonctionner pour tout le monde</span><span class="sxs-lookup"><span data-stu-id="5daca-113">Make the pull request queue work better for everyone</span></span>

<span data-ttu-id="5daca-114">Il existe deux réalités fondamentales dans la file d’attente de PR :</span><span class="sxs-lookup"><span data-stu-id="5daca-114">There are two basic realities in the PR queue:</span></span>

- <span data-ttu-id="5daca-115">Les demandes de tirage de petite étendue et avec des changements très similaires sont plus rapides à réviser.</span><span class="sxs-lookup"><span data-stu-id="5daca-115">Pull requests that are small in scope and relate changes take less time to review.</span></span>
- <span data-ttu-id="5daca-116">La révision des demandes de tirage de grande étendue ou contenant des changements sans liens entre eux prend plus de temps.</span><span class="sxs-lookup"><span data-stu-id="5daca-116">Pull requests that are large in scope or that contain unrelated changes take more time to review.</span></span>

### <a name="avoid-branches-that-update-large-numbers-of-files"></a><span data-ttu-id="5daca-117">Éviter les branches qui mettent à jour un grand nombre de fichiers</span><span class="sxs-lookup"><span data-stu-id="5daca-117">Avoid branches that update large numbers of files</span></span>

<span data-ttu-id="5daca-118">Séparez les mises à jour mineures à des articles existants des nouveaux articles ou révisions majeures.</span><span class="sxs-lookup"><span data-stu-id="5daca-118">Separate minor updates to existing articles from new articles or major rewrites.</span></span> <span data-ttu-id="5daca-119">Travaillez sur ces changements dans des branches de travail distinctes.</span><span class="sxs-lookup"><span data-stu-id="5daca-119">Work on these changes in separate working branches.</span></span>

<span data-ttu-id="5daca-120">Les changements en bloc entraînent des demandes de tirage avec un grand nombre de fichiers à changer.</span><span class="sxs-lookup"><span data-stu-id="5daca-120">Bulk changes drive PRs with large numbers of changed files.</span></span> <span data-ttu-id="5daca-121">Limitez vos demandes de tirage à un maximum de 50 fichiers à changer.</span><span class="sxs-lookup"><span data-stu-id="5daca-121">Limit your PRs to a maximum of 50 changed files.</span></span> <span data-ttu-id="5daca-122">Les grandes demandes de tirage sont difficiles à réviser et sont plus susceptibles de contenir des erreurs.</span><span class="sxs-lookup"><span data-stu-id="5daca-122">Large PRs are difficult to review and are more prone to contain errors.</span></span>

### <a name="renaming-or-deleting-files"></a><span data-ttu-id="5daca-123">Renommage ou suppression de fichiers</span><span class="sxs-lookup"><span data-stu-id="5daca-123">Renaming or deleting files</span></span>

<span data-ttu-id="5daca-124">Quand vous renommez ou supprimez des fichiers, évitez de mélanger ces changements avec des ajouts ou des mises à jour du contenu.</span><span class="sxs-lookup"><span data-stu-id="5daca-124">When you rename or delete files, avoid mixing these changes with content additions or updates.</span></span>
<span data-ttu-id="5daca-125">Gérez ces changements dans une demande de tirage distincte qui sera fusionnée après la demande de tirage pour les mises à jour associées.</span><span class="sxs-lookup"><span data-stu-id="5daca-125">Handle these changes in a separate PR that gets merged after the PR for related updates.</span></span> <span data-ttu-id="5daca-126">Par exemple, mettez à jour le fichier des redirections et vérifiez que la redirection fonctionne avant de supprimer un article.</span><span class="sxs-lookup"><span data-stu-id="5daca-126">For example, update the redirects file and verify the redirect is working before deleting an article.</span></span>

<span data-ttu-id="5daca-127">Vous devez mettre à jour tous les fichiers qui sont liés au fichier renommé.</span><span class="sxs-lookup"><span data-stu-id="5daca-127">You must update all files that link to the renamed file.</span></span> <span data-ttu-id="5daca-128">Cela comprend tous les fichiers de table des matières.</span><span class="sxs-lookup"><span data-stu-id="5daca-128">This includes any TOC files.</span></span> <span data-ttu-id="5daca-129">Vous devez également ajouter des entrées de redirection dans le fichier de redirection maître (`.openpublishing.redirection.json`) à la racine du dépôt.</span><span class="sxs-lookup"><span data-stu-id="5daca-129">You must also add redirection entries in the master redirection file (`.openpublishing.redirection.json`) in the root of the repository.</span></span>

## <a name="docs-pr-validation-service"></a><span data-ttu-id="5daca-130">Service de validation de demande de tirage (pull request) Docs</span><span class="sxs-lookup"><span data-stu-id="5daca-130">Docs PR validation service</span></span>

<span data-ttu-id="5daca-131">Le service de validation de demande de tirage Docs est une application GitHub qui exécuter des règles de validation sur des fichiers dans une demande de tirage.</span><span class="sxs-lookup"><span data-stu-id="5daca-131">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="5daca-132">Vous pouvez observer le comportement suivant :</span><span class="sxs-lookup"><span data-stu-id="5daca-132">You'll see the following behavior:</span></span>

1. <span data-ttu-id="5daca-133">Vous envoyez une demande de tirage.</span><span class="sxs-lookup"><span data-stu-id="5daca-133">You submit a PR.</span></span>
1. <span data-ttu-id="5daca-134">Dans le commentaire GitHub qui indique l’état de votre demande de tirage, l’état des « contrôles » activés sur le dépôt s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5daca-134">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="5daca-135">Notez que dans cet exemple, deux contrôles sont activés : « Commit Validation » et « OpenPublishing.Build » :</span><span class="sxs-lookup"><span data-stu-id="5daca-135">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![certains contrôles ont échoué](media/powershell-pull-requests/validation-failed.png)

   <span data-ttu-id="5daca-137">La build peut réussir même si la validation de la confirmation échoue.</span><span class="sxs-lookup"><span data-stu-id="5daca-137">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="5daca-138">Pour plus d’informations, cliquez sur **Détails**.</span><span class="sxs-lookup"><span data-stu-id="5daca-138">Click **Details** for more information.</span></span>
1. <span data-ttu-id="5daca-139">Dans la page Details, vous voyez tous les contrôles de validation qui ont échoué, avec des informations sur la façon de corriger les problèmes.</span><span class="sxs-lookup"><span data-stu-id="5daca-139">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues.</span></span>
1. <span data-ttu-id="5daca-140">Quand la validation réussit, le commentaire suivant est ajouté à la demande de tirage :</span><span class="sxs-lookup"><span data-stu-id="5daca-140">When validation succeeds, the following comment is added to the PR:</span></span>

   ![Validation de build](media/powershell-pull-requests/build-validation.png)

<span data-ttu-id="5daca-142">Si vous êtes contributeur externe (non-Microsoft), vous n’avez pas accès aux rapports de génération détaillés ni aux liens d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="5daca-142">If you are an external (non-Microsoft) contributor you do not have access to the detailed build reports or preview links.</span></span>

### <a name="build-warnings"></a><span data-ttu-id="5daca-143">Avertissements de build</span><span class="sxs-lookup"><span data-stu-id="5daca-143">Build warnings</span></span>

<span data-ttu-id="5daca-144">Normalement, vous devez corriger toutes les erreurs, tous les avertissements et toutes les suggestions d’une build.</span><span class="sxs-lookup"><span data-stu-id="5daca-144">Normally you should fix all build errors, warnings, and suggestions.</span></span> <span data-ttu-id="5daca-145">Certains avertissements peuvent cependant être ignorés.</span><span class="sxs-lookup"><span data-stu-id="5daca-145">However, there are some warnings that can be ignored.</span></span>

<span data-ttu-id="5daca-146">Les avertissements suivants peuvent être ignorés :</span><span class="sxs-lookup"><span data-stu-id="5daca-146">The following warnings can be ignored:</span></span>

- > <span data-ttu-id="5daca-147">Impossible de trouver le nom du service pour `<version>/<modulepath>/About/About.md`</span><span class="sxs-lookup"><span data-stu-id="5daca-147">Can't find service name for `<version>/<modulepath>/About/About.md`</span></span>

- > <span data-ttu-id="5daca-148">Les métadonnées avec les noms suivants ne peuvent pas être définies dans l’en-tête YAML, ou sous forme de métadonnées au niveau du fichier dans docfx.json ou en tant que métadonnées globales dans docfx.json : `locale`.</span><span class="sxs-lookup"><span data-stu-id="5daca-148">Metadata with following name(s) are not allowed to be set in Yaml header, or as file level metadata in docfx.json, or as global metadata in docfx.json: `locale`.</span></span> <span data-ttu-id="5daca-149">Elles sont générées par la plateforme Docs : les valeurs définies à ces 3 emplacements sont donc ignorées.</span><span class="sxs-lookup"><span data-stu-id="5daca-149">They are generated by Docs platform, so the values set in these 3 places will be ignored.</span></span> <span data-ttu-id="5daca-150">Pour résoudre l’avertissement, supprimez-les des 3 emplacements.</span><span class="sxs-lookup"><span data-stu-id="5daca-150">Please remove them from all 3 places to resolve the warning.</span></span>
