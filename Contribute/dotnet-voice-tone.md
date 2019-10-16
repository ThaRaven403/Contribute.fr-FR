---
title: Guide de style pour les contributions à la documentation .NET
description: Découvrez notre guide de style en comparant des exemples qui le suivent à des exemples qui le ne suivent pas.
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
ms.date: 11/07/2018
ms.openlocfilehash: 4108019ac50d703c6dd509eca7a6394cc1c9dc18
ms.sourcegitcommit: ca84e542b081e145052f38967e826f6ef25da1b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2019
ms.locfileid: "72288485"
---
# <a name="voice-and-tone-guidelines"></a>Guide de style

Des utilisateurs très divers, notamment des professionnels de l’informatique et des développeurs, lisent vos documents en vue d’apprendre à utiliser .NET dans leurs tâches quotidiennes. Votre objectif est de créer une documentation qui accompagne les lecteurs. Notre guide de style a pour but de vous y aider. Il contient les recommandations suivantes :

Vous trouverez des exemples tout au long de ce guide de style. Nous avons rédigé ce guide pour vous fournir des exemples à suivre quand vous créerez votre documentation pour .NET. À des fins de comparaison, il contient également des exemples d’articles qui ne respectent pas nos recommandations.

## <a name="use-a-conversational-tone"></a>Utilisez un style oral

### <a name="appropriate-style"></a>Style approprié

Nous souhaitons que notre documentation emploie un style oral. Le lecteur devrait avoir l’impression d’avoir une conversation avec l’auteur lors de la lecture d’un tutoriel ou d’explications. L’expérience doit être informelle, conversationnelle et informative. Le lecteur doit avoir l’impression qu’il écoute l’auteur lui expliquer les concepts.

### <a name="inappropriate-style"></a>Style inapproprié

Il existe un contraste entre le style oral et le style des rubriques techniques au traitement plus académique. Ces ressources sont très utiles, mais leurs auteurs ont écrit ces articles dans un style très différent de celui de notre documentation. Une revue académique emploie un ton et un style rédactionnels totalement différents. On a généralement la sensation de lire une rubrique avec un ton très sec.  

Le premier paragraphe ci-dessus respecte nos recommandations en matière de style oral. Le second emploie un style plus académique. On voit immédiatement la différence. 

## <a name="write-in-second-person"></a>Écriture à la deuxième personne

### <a name="appropriate-style"></a>Style approprié

Vous devez écrire vos articles comme si vous vous adressiez directement au lecteur. Vous devez souvent employer la deuxième personne (comme je l’ai fait dans ces deux phrases). Mais le terme « deuxième personne » ne veut pas toujours dire utiliser le mot « vous ». Écrivez directement au lecteur. Écrivez des phrases à l’impératif. Dites au lecteur ce que vous voulez qu’il apprenne.

### <a name="inappropriate-style"></a>Style inapproprié

Un auteur pourrait également choisir d’écrire à la troisième personne. Dans ce modèle, il doit trouver un nom ou un pronom à employer pour faire référence au lecteur. Le lecteur trouvera souvent ce style moins agréable à lire.

Le premier paragraphe respecte nos recommandations de style. Le deuxième utilise la troisième personne. Veuillez écrire à la deuxième personne. Vous avez sans doute trouvé cela beaucoup plus plaisant à lire.

## <a name="use-active-voice"></a>Utilisez la voix active

Rédigez vos articles à la voix active. Le terme « voix active » signifie que le sujet de la phrase effectue l’action (verbe) de cette phrase. Par contraste, une phrase à la voix passive est organisée de telle sorte que le sujet de la phrase subit l’action. Comparez ces deux exemples :

>Le compilateur a transformé le code source en exécutable.

>Le code source a été transformé en exécutable par le compilateur.

La première phrase utilise la voix active. La deuxième phrase a été rédigé à la voix passive. (Ces deux phrase fournissent un autre exemple de chaque style.)

Nous recommandons l’utilisation de la voix active car elle est plus agréable à lire. La voix passive peut être plus difficile à lire.

## <a name="target-a-fifth-grade-reading-level"></a>Ciblez un niveau de lecture correspondant à une première année de collège

Nous fournissons cette dernière recommandation car une grande partie de nos lecteurs ne sont pas des anglophones natifs. Vos articles sont destinés à une audience internationale. N’oubliez pas que vos lecteurs n’auront peut-être pas le même niveau de vocabulaire anglais que vous.

Mais d’un autre côté, vous écrivez tout de même pour des techniciens. Vous pouvez partir du principe que vos lecteurs ont des connaissances en programmation et du vocabulaire propre aux termes de programmation. Des termes tels que programmation orientée objet, classe, objet, fonction et méthode leur seront familiers. En revanche, tous vos lecteurs ne seront pas titulaires d’une licence en informatique. Vous devrez probablement définir des termes tels que « idempotent » si vous les utilisez :

>La méthode `Close()` est idempotente, ce qui signifie que vous pouvez l’appeler plusieurs fois et l’effet sera le même que si vous l’aviez appelée une seule fois.

## <a name="avoid-future-tense"></a>Évitez d’employer le futur

Dans certaines langues, le concept du futur comme temps verbal n’est pas le même qu’en anglais. L’emploi du futur peut accroître la difficulté de lecture de vos documents. De plus, quand on emploie le futur, la question évidente est « quand ? ». Ainsi, si vous écrivez « L’apprentissage PowerShell vous sera bénéfique », le lecteur se posera la question évidente « Quand cela sera-t-il bénéfique ? ». Au lieu de cela, dites simplement : « L’apprentissage PowerShell est très utile ».

## <a name="what-is-it---so-what"></a>Qu’est-ce que c’est ?

Chaque fois que vous introduisez un nouveau concept, définissez-le d’abord. Ensuite, expliquez pourquoi il est utile. Le lecteur doit d’abord comprendre de quoi il s’agit avant de pouvoir en comprendre les avantages (ou inconvénients).
