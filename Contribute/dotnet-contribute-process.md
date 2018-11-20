---
title: Processus de contribution pour les dépôts de documentation .NET
description: Cet article fournit une brève introduction à la contribution aux dépôts de documentation .NET. Vous découvrirez les dépôts utilisés, le processus d’organisation du contenu et les stratégies de gestion des exemples de code et autres ressources.
ms.date: 11/07/2018
ms.openlocfilehash: b83a3080f1abd4df8caaa9d10859760006216e86
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609759"
---
# <a name="process-for-contributing-to-net-docs"></a>Processus de contribution à la documentation .NET

Nous apprécions toute contribution de la communauté à la documentation. Vous trouverez ci-dessous quelques règles qu’il convient de garder à l’esprit quand vous contribuez à la documentation .NET :

- Ne nous surprenez **pas** avec de grandes demandes de tirage (pull requests). Ouvrez plutôt un problème et lancez une discussion pour que nous puissions nous entendre sur la marche à suivre, ceci afin de ne pas gaspiller votre temps inutilement.
- **Suivez** ces instructions et respectez le [guide de style](dotnet-voice-tone.md).
- **Utilisez** le fichier de [modèle](dotnet-style-guide.md) comme point de départ pour votre travail.
- **Créez** une branche distincte sur votre duplication (fork) avant de travailler sur les articles.
- **Suivez** le [workflow GitHub Flow](https://guides.github.com/introduction/flow/).
- **Rédigez** fréquemment des tweets et des billets de blog (ou autres) concernant vos contributions.

Le respect de ces instructions est garant d’une meilleure expérience à la fois pour vous et pour nous.

## <a name="make-a-contribution-to-net-docs"></a>Contribuer à la documentation .NET

**Étape 1 :** Ignorez cette étape pour les petits changements. Si vous souhaitez rédiger du nouveau contenu ou réviser du contenu existant en profondeur, ouvrez un [problème](https://github.com/dotnet/docs/issues) décrivant ce que vous voulez faire.

Le contenu du dossier **docs** est organisé en sections qui sont reflétées dans la Table des matières. Définissez l’emplacement de la rubrique dans la Table des matières. Obtenez des commentaires concernant votre proposition.

-ou-

Vous pouvez également choisir parmi les problèmes existants, pour lesquels les contributions de la communauté sont les bienvenues. La page [Projects for .NET Community contributors](https://github.com/dotnet/docs/projects/35) liste une grande partie des problèmes disponibles pour les contributeurs de la communauté. En fonction de vos intérêts et de votre niveau d’implication, vous pouvez choisir parmi les problèmes des catégories suivantes :

- **Maintenance**. Cette catégorie comprend des contributions assez simples, telles que la réparation de liens rompus ou incorrects, l’ajout d’exemples de code manquants ou la résolution de problèmes de contenu limités. Dans certains cas, ces problèmes peuvent concerner de grandes quantités de fichiers. Vous devez alors nous indiquer sur quoi vous souhaitez travailler avant de commencer. Ajoutez un commentaire au problème pour nous signaler que vous travaillez dessus.

- **Mises à jour de contenu**. Étant donné la taille gigantesque du jeu de documentation, le contenu devient facilement obsolète et nécessite une révision. De plus, pour diverses raisons une partie du contenu est dupliquée, voir tripliquée. La mise à jour du contenu implique de s’assurer que chacune des rubriques est à jour ou de réviser le contenu d’un domaine de fonctionnalités afin d’éliminer la duplication et de garantir que tout le contenu unique est préservé dans le jeu de documentation plus petit.

- **Création de nouveau contenu**. Si vous souhaitez créer votre propre rubrique, ces problèmes listent les rubriques que nous aimerions vouloir ajouter à notre jeu de documentation. Veillez tout de même à nous le signaler avant de commencer à travailler sur une rubrique. Si vous souhaitez créer une rubrique qui n’est pas mentionnée ici, ouvrez un problème.

Vous pouvez aussi consulter notre liste de [problèmes ouverts](https://github.com/dotnet/docs/issues) et vous porter volontaire pour travailler sur ceux qui vous intéressent. Nous utilisons l’étiquette [up-for-grabs](https://github.com/dotnet/docs/labels/up-for-grabs) pour signaler les problèmes identifiés pour la contribution par la communauté. Ils nécessitent généralement un contexte minimal et conviennent particulièrement aux premiers problèmes. Nous encourageons les contributeurs expérimentés au sein de notre communauté à examiner tous les problèmes qui les intéressent. Quand vous en identifiez un, ajoutez un commentaire pour demander s’il est ouvert.

Une fois que vous avez choisi une tâche sur laquelle travailler, suivez le guide [Bien démarrer](get-started-setup-github.md) pour créer un compte GitHub et configurer votre environnement.

**Étape 2 :** Dupliquez (fork) les dépôts `/dotnet/docs`, `dotnet/samples`, `dotnet/dotnet-api-docs`, `dotnet/roslyn-api-docs` ou `dotnet/ml-api-docs` selon les besoins, et créez une branche pour vos changements.

Pour les petits changements, consultez les instructions relatives aux modifications dans GitHub dans la [page d’accueil](index.md#quick-edits-to-existing-documents) du guide du contributeur.

**Étape 3 :** Apportez vos modifications sur cette nouvelle branche.

S’il s’agit d’une nouvelle rubrique, vous pouvez utiliser ce [fichier de modèle](dotnet-style-guide.md) comme point de départ. Il contient les instructions de rédaction et explique également quelles sont les métadonnées nécessaires pour chaque article, telles que les informations sur l’auteur.

Accédez au dossier qui correspond à l’emplacement dans la Table des matières déterminé pour votre article à l’étape 1. Ce dossier contient les fichiers Markdown pour tous les articles de cette section. Si nécessaire, créez un nouveau dossier où placer les fichiers pour votre contenu. L’article principal de cette section se nomme *index.md*. Pour les images et autres ressources statiques, créez (s’il n’existe pas) un sous-dossier nommé **media** dans le dossier qui contient votre article. Dans le dossier **media**, créez un sous-dossier avec le nom de l’article (sauf le fichier d’index). L’exemple de code doit figurer dans le dépôt `dotnet/samples`, comme décrit dans la section sur les [exemples](#contributing-to-samples).

Veillez à bien respecter la syntaxe Markdown. Pour obtenir des exemples, consultez l’[aide-mémoire sur les modèles et la syntaxe Markdown](dotnet-style-guide.md).

## <a name="example-structure"></a>Exemple  de structure

    docs
      /about
      /core
        /porting
          porting-overview.md
          /media
            /porting-overview
                portability_report.png

**Étape 4 :** Envoyez une demande de tirage de votre branche à la branche principale.

> [!IMPORTANT]
> La fonctionnalité d’[automation de commentaire](how-to-write-workflows-major.md#review-and-sign-off) n’est disponible sur aucun des dépôts de documentation .NET pour l’instant. Les membres de l’équipe de documentation .NET examineront et fusionneront votre demande de tirage.

Chaque demande de tirage doit généralement traiter un seul problème à la fois. La demande de tirage peut modifier un un plusieurs fichiers. Si vous traitez plusieurs correctifs sur plusieurs fichiers, il est préférable de soumettre plusieurs demandes de tirage. Si vous créez des exemples de code en plus de mettre à jour le Markdown, vous devez créer une demande de tirage distincte pour les exemples.

Si votre demande de tirage résout un problème existant, ajoutez le mot clé `Fixes #Issue_Number` au message de validation ou à la description de la demande de tirage. Ainsi, le problème sera fermé automatiquement lors de la fusion de la demande de tirage. Pour plus d’informations, consultez [Closing issues via commit messages](https://help.github.com/articles/closing-issues-via-commit-messages/).

L’équipe .NET examinera votre demande de tirage et vous indiquera si d’autres mises à jour/changements sont nécessaires pour son approbation.

**Étape 5 :** Apportez les mises à jour nécessaires à votre branche, comme discuté avec l’équipe.

Les personnes chargées de la maintenance fusionneront votre demande de tirage dans la branche principale une fois que les commentaires auront été appliqués et que vos changements auront été approuvés.

Nous envoyons (push) régulièrement toutes les validations de la branche master à la branche active ; vous pourrez alors voir votre contribution sur le site https://docs.microsoft.com/dotnet/. En règle générale, nous effectuons des publications chaque jour ouvré. Les activités de maintenance peuvent retarder la publication de quelques jours.

## <a name="contributing-to-samples"></a>Contribution aux exemples de code

Le dépôt [dotnet/samples](https://github.com/dotnet/samples) contient tous les exemples de code qui font partie d’une rubrique sous la documentation .NET. Il existe différents projets qui sont organisés dans des sous-dossiers. Ces sous-dossiers sont organisés de manière semblable à l’organisation de la documentation .NET.

Nous faisons la distinction suivante pour le code qui existe dans notre dépôt :

- Exemples de code : les lecteurs peuvent télécharger et exécuter les exemples. Tous les exemples de code doivent être des bibliothèques ou applications complètes. Là où l’exemple crée une bibliothèque, il doit inclure des tests unitaires ou une application qui permet aux lecteurs d’exécuter le code. Ils utilisent souvent plusieurs technologies, fonctionnalités ou boîtes à outils. Le fichier readme.md de chaque exemple de code fera référence à l’article afin que vous puissiez en savoir davantage sur les concepts traités dans chaque exemple.
- Extraits : ils illustrent un concept ou une tâche plus petit(e). Ils peuvent être compilés, mais ne sont pas censés être des applications complètes. Ils doivent s’exécuter correctement, mais ne constituent pas un exemple d’application pour un scénario type. Ils sont plutôt conçus pour être le plus petit possible, afin d’illustrer un seul concept ou une seule fonctionnalité. Ils ne doivent pas occuper plus d’un écran de code.

Tout le code réside dans le dépôt [dotnet/samples](https://github.com/dotnet/samples). Nous travaillons actuellement à l’élaboration d’un modèle dans lequel notre structure de dossiers d’exemples de code correspond à notre structure de dossiers de documentation. Nous respectons les règles suivantes :

- Le dossier de premier niveau *snippets* contient des extraits de code pour de petits exemples bien précis.
- Les exemples de référence d’API sont placés dans un dossier qui suit ce modèle : *snippets/\<langage>/api/\<espace_de_noms>/\<nom_api>*.
- Les autres dossiers de niveau supérieur correspondent aux dossiers de niveau supérieur du dépôt *docs*. Par exemple, le dépôt docs contient un dossier *machine-learning/tutorials*, et les exemples de code relatifs aux tutoriels d’apprentissage automatique se trouvent dans le dossier *samples/machine-learning/tutorials*.

De plus, tous les exemples de code sous les dossiers *core* et *standard* doivent pouvoir être générés et exécutés sur toutes les plateformes prises en charge par .NET Core. Notre système Build CI (intégration continue) appliquera cette règle. Le dossier *framework* de premier niveau contient des exemples de code qui sont générés et validés uniquement sur Windows.

Les exemples de projets doivent pouvoir être générés et exécutés sur la gamme de plateformes la plus large possible pour un exemple donné. En pratique, cela signifie que vous devez générer dans la mesure du possible des applications console .NET Core. Les exemples qui sont propres au web ou à un framework d’interface utilisateur (applications web, applications mobiles, applications WPF ou WinForms, entre autres) doivent ajouter ces outils si nécessaire.

Nous essayons actuellement de mettre en place un système d’intégration continue pour tout le code. Quand vous effectuez une mise à jour d’un exemple de code, veillez à ce qu’elle fasse partie d’un projet pouvant être généré. Dans l’idéal, ajoutez également des tests pour vérifier que les exemples de code sont corrects.

Chaque exemple de code complet que vous créez doit contenir un fichier *readme.md*. Ce fichier doit contenir une brève description de l’exemple (un ou deux paragraphes). Votre fichier *readme.md* doit indiquer aux lecteurs ce qu’ils apprendront en explorant cet exemple. Il doit également contenir un lien vers le document actif sur le [site de documentation .NET](https://docs.microsoft.com/dotnet/welcome). Pour déterminer l’emplacement sur ce site où est mappé un fichier stocké dans le dépôt, remplacez `/docs` dans le chemin du dépôt par `http://docs.microsoft.com/dotnet`.

Votre rubrique contiendra aussi des liens vers l’exemple de code. Établissez un lien direct vers le dossier de l’exemple de code sur GitHub.

### <a name="writing-a-new-snippet-or-sample"></a>Rédaction d’un nouvel extrait ou exemple de code

1. Votre exemple **doit faire partie d’un projet pouvant être généré**. Dans la mesure du possible, les projets doivent pouvoir être générés sur toutes les plateformes prises en charge par .NET Core. Les exceptions à cette règle sont les exemples de code qui illustrent une fonctionnalité ou un outil propre à une plateforme.

2. Pour des raisons de cohérence, votre exemple de code doit être conforme au [style de codage corefx](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md).

    - De plus, nous préférons que vous utilisiez des méthodes `static` plutôt que des instances de méthodes quand vous illustrez quelque chose qui ne nécessite pas l’instanciation d’un nouvel objet.

3. Votre exemple de code doit inclure une **gestion des exceptions appropriée**. Il doit gérer toutes les exceptions susceptibles d’être levées dans le contexte de l’exemple. Par exemple, un exemple de code qui appelle la méthode [Console.ReadLine](https://docs.microsoft.com/dotnet/api/system.console.readline) pour récupérer l’entrée d’utilisateur doit utiliser une gestion des exceptions appropriée quand la chaîne d’entrée est passée en tant qu’argument à une méthode. De même, si votre exemple de code s’attend à ce qu’un appel de méthode échoue, l’exception résultante doit être gérée. Vous devez toujours gérer les exceptions spécifiques levées par la méthode, plutôt que les exceptions de classe de base telles que [Exception](https://docs.microsoft.com/dotnet/api/system.exception) ou [SystemException](https://docs.microsoft.com/dotnet/api/system.systemexception).

4. Si votre exemple de code génère un package autonome, vous devez inclure les runtimes utilisés par notre système CI Build, en plus de ceux utilisés par votre exemple :
    - `win7-x64`
    - `win8-x64`
    - `win81-x64`
    - `ubuntu.16.04-x64`

Nous mettrons bientôt en place un système d’intégration continue pour générer ces projets.

Pour créer un exemple de code :

1. Soumettez un [problème](https://github.com/dotnet/docs/issues) ou ajoutez un commentaire à un problème existant sur lequel vous travaillez.
2. Rédigez une rubrique qui explique les concepts illustrés par votre exemple de code (exemple : `docs/standard/linq/where-clause.md`).
3. Rédigez votre exemple de code (exemple : `WhereClause-Sample1.cs`).
4. Créez un fichier Program.cs avec un point d’entrée Main qui appelle votre exemple de code. S’il y en a déjà un, ajoutez l’appel à votre exemple :
    ```csharp
    public class Program
    {
        public void Main(string[] args)
        {
            WhereClause1.QuerySyntaxExample();

            // Add the method syntax as an example.
            WhereClause1.MethodSyntaxExample();
        }
    }
    ```
Vous devez générer tout exemple ou extrait de code .NET Core à l’aide de l’interface de ligne de commande .NET Core, que vous pouvez installer avec le [SDK .NET Core](https://www.microsoft.com/net/download). Pour générer et exécuter votre exemple de code :

1. Accédez au dossier de l’exemple et générez-le afin de vérifier s’il existe des erreurs :

    ```console
    dotnet build
    ```
2. Exécutez votre exemple de code :

    ```console
    dotnet run
    ```

3. Ajoutez un fichier readme.md au répertoire racine de votre exemple. 

   Il doit inclure une brève description du code et renvoyer le lecteur à l’article qui référence l’exemple.

Sauf indication contraire, tous les exemples de code doivent pouvoir être générés à partir de la ligne de commande sur n’importe quelle plateforme prise en charge par .NET Core. Il existe quelques exemples de code qui sont propres à Visual Studio et nécessitent Visual Studio 2017 ou version ultérieure. De plus, certains exemples illustrent des fonctionnalités propres à une plateforme, et nécessiteront une plateforme spécifique. D’autres exemples et extraits de code nécessitent le .NET Framework, et s’exécuteront sur des plateformes Windows et  nécessiteront le Pack du développeur pour la version cible de .Net Framework.

## <a name="the-c-interactive-experience"></a>Expérience interactive C#

Tous les exemples de code inclus dans un article utilisent une [balise de langage](how-to-write-use-markdown.md#code-snippets) pour indiquer le langage source. Les exemples de code courts en C# peuvent utiliser la balise de langage `csharp-interactive` pour spécifier un exemple C# qui s’exécute dans le navigateur. (Les exemples de code inline utilisent la balise `csharp-interactive` ; pour les extraits inclus à partir de la source, utilisez la balise `code-csharp-interactive`.) Ces exemples de code affichent une fenêtre de code et une fenêtre de sortie dans l’article. La fenêtre de sortie affiche toute sortie d’exécution du code interactif une fois que l’utilisateur a exécuté l’exemple de code.

L’expérience interactive C# change la façon dont nous travaillons avec nos exemples de code. Les visiteurs peuvent exécuter l’exemple pour voir les résultats. Plusieurs facteurs contribuent à déterminer si l’exemple ou le texte correspondant doit inclure des informations sur la sortie.

### <a name="when-to-display-the-expected-output-without-running-the-sample"></a>Quand faut-il afficher la sortie attendue sans exécuter l’exemple de code ?

- Les articles destinés aux débutants doivent fournir une sortie afin que le lecteur puisse comparer la sortie générée par leur travail à la réponse attendue.
- Les exemples de code pour lesquels la sortie est intégrée à la rubrique doivent afficher cette sortie. Par exemple, les articles relatifs au texte mis en forme doivent montrer le format du texte sans qu’il soit nécessaire d’exécuter l’exemple.
- Quand l’exemple de code et la sortie attendue sont tous les deux courts, vous pouvez afficher la sortie. Cela permet de gagner un peu de temps.
- Les articles expliquant de quelle manière la culture actuelle ou la culture invariante affectent la sortie doivent expliquer quelle est la sortie attendue. La boucle REPL (Read Evaluate Print Loop) s’exécute sur un hôte Linux. La culture par défaut et la culture invariante produisent différentes sorties sur différents systèmes d’exploitation et ordinateurs. L’article doit fournir des explications concernant la sortie sur les systèmes Windows, Linux et Mac.

### <a name="when-to-exclude-expected-output-from-the-sample"></a>Quand faut-il ne pas inclure la sortie attendue dans l’exemple de code ?

- Les articles dont l’exemple de code génère une longue sortie ne doivent pas l’inclure dans les commentaires. Cela obscurcit le code une fois que l’exemple a été exécuté.
- Dans les articles dont l’exemple illustre une rubrique, mais pour lesquels la sortie n’est pas essentielle à la compréhension. Par exemple, le code qui exécute une requête LINQ pour expliquer la syntaxe de requête et qui affiche ensuite chaque élément de la collection de sortie.

> [!NOTE]
> Vous remarquerez peut-être que certaines rubriques ne respectent pas toutes les instructions spécifiées ici. Nous nous efforçons actuellement d’appliquer une cohérence dans l’ensemble du site. Consultez la liste des [problèmes ouverts](https://github.com/dotnet/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22%3Abookmark_tabs%3A+Information+Architecture%22) que nous suivons actuellement en vue d’atteindre cet objectif spécifique.

## <a name="contributor-license-agreement"></a>Contrat de licence pour les contributeurs

Vous devez signer le [.NET Foundation Contribution License Agreement (CLA)](https://cla.dotnetfoundation.org) pour que votre demande de tirage soit fusionnée. Il s’agit d’une exigence ponctuelle pour les projets .NET Foundation. Pour en savoir plus, consultez la page [Contribution License Agreements (CLA)](http://en.wikipedia.org/wiki/Contributor_License_Agreement) sur Wikipedia.

Le contrat : [net-foundation-contribution-license-agreement.pdf](https://github.com/dotnet/home/blob/master/guidance/net-foundation-contribution-license-agreement.pdf)

Vous n’êtes pas obligé de signer le contrat tout de suite. Vous pouvez cloner, dupliquer (fork) et soumettre votre demande de tirage comme d’habitude. Une fois votre demande de tirage créée, elle est classifiée par un bot CLA. Si le changement est mineur (par exemple, vous avez corrigé une faute de frappe), la demande de tirage est libellée avec `cla-not-required`. Sinon, elle est classifiée en tant que `cla-required`. Une fois que vous avez signé le CLA, la demande de tirage actuelle et toutes les demandes ultérieures sont libellées en tant que `cla-signed`.
