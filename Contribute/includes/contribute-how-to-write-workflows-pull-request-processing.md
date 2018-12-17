## <a name="pull-request-processing"></a>Traitement des demandes de tirage (pull request)

La section précédente a décrit le processus d’envoi des modifications proposées, en les regroupant dans une nouvelle demande de tirage qui est ajoutée à la file d’attente des demandes de tirage du dépôt cible. Une demande de tirage active le modèle de collaboration de GitHub en demandant que les modifications de votre branche de travail soient tirées (pull) et fusionnées dans une autre branche. Dans la plupart des cas, cette autre branche est la branche par défaut/master du dépôt principal.

### <a name="validation"></a>Validation

Avant de pouvoir fusionner votre demande de tirage dans sa branche de destination, vous devrez probablement effectuer une ou plusieurs procédures de validation. Les procédures de validation peuvent varier en fonction de l’étendue des modifications proposées et des règles du dépôt cible. Après l’envoi de votre demande de tirage, un ou plusieurs des événements suivants peuvent se produire :

- **Fusionnabilité** : Un test de fusionnabilité GitHub de base de référence est d’abord effectué pour vérifier si les changements proposés dans votre branche ne sont pas en conflit avec la branche de destination. Si la demande de tirage indique que ce test a échoué, vous devez réconcilier le contenu qui provoque le conflit de fusion pour que le traitement puisse continuer.
- **Contrat de licence de contribution (CLA)**  : Si vous contribuez à un dépôt public et que vous n’êtes pas un employé Microsoft, en fonction de l’importance des changements proposés, il vous sera probablement demandé de remplir un contrat de licence de contribution la première fois que vous envoyez une demande de tirage à ce dépôt. Une fois le contrat SLA rempli, votre demande de tirage est traitée.
- **Étiquetage** : Des étiquettes sont appliquées automatiquement à votre demande de tirage pour indiquer l’état de celle-ci au fur et à mesure qu’elle progresse dans le workflow de validation. Par exemple, les nouvelles demandes de tirage peuvent recevoir automatiquement l’étiquette « ne pas fusionner », indiquant que la demande de tirage n’a pas encore subi les étapes de validation, de revue et d’accord final.
- **Validation et génération** : Des contrôles automatisés vérifient si vos modifications passent les tests de validation. Les tests de validation peuvent générer des avertissements ou des erreurs, qui vous obligent à apporter des modifications à un ou plusieurs fichiers de votre demande de tirage pour permettre à celle-ci d’être fusionnée. Les résultats des tests de validation sont ajoutés sous forme de commentaires à votre demande de tirage pour être utilisés lors de votre revue et peuvent vous être envoyés dans un e-mail.
- **Préproduction** : Les pages de l’article affectées par vos modifications sont déployées automatiquement sur un environnement de préproduction pour revue, en attendant que la validation et la génération réussissent. Des URL de préversion apparaissent dans un commentaire de demande de tirage.
- **Fusion automatique** : La demande de tirage peut être fusionnée automatiquement si elle passe les tests de validation et répond à certains critères. Dans ce cas, vous n’avez aucune autre action à effectuer.

### <a name="review-and-sign-off"></a>Revue et accord final

Une fois le traitement de la demande de tirage terminé, vous devez examiner les résultats (commentaires de la demande de tirage, URL des préversions, etc.) pour déterminer si des modifications supplémentaires de ses fichiers sont nécessaires avant de marquer votre accord final pour la fusion. Si un réviseur de demande de tirage a revu votre demande de tirage, il peut avoir indiqué via des commentaires si des problèmes ou des questions en suspens doivent être résolus avant la fusion.

[!INCLUDE[contribute-how-to-pull-requests-apex-automation.md](contribute-how-to-pull-requests-apex-automation.md)]

Si la demande de tirage n’a plus de problème et a reçu un accord final, vos modifications sont fusionnées dans la branche parent et la demande de tirage est clôturée.

### <a name="publishing"></a>Publication

Rappelez-vous que votre demande de tirage doit être fusionnée par un réviseur de demande de tirage pour que les modifications puissent être incluses dans la publication planifiée suivante. Les demandes de tirage sont normalement revues/fusionnées dans leur ordre d’envoi. Si votre demande de tirage doit être fusionnée pour une publication spécifique, vous devez travailler avec votre réviseur de demande de tirage suffisamment à l’avance pour que la fusion soit effectuée avant la publication.

Une fois vos contributions approuvées et fusionnées, elles sont collectées par le processus de publication de docs.microsoft.com. En fonction de l’équipe qui gère le dépôt auquel vous contribuez, le délai de publication peut varier. Les articles publiés dans les chemins suivants sont normalement déployés aux environs de 10h30 et 15h30 (heure du Pacifique, GMT-8), du lundi au vendredi :

- https://docs.microsoft.com/azure/
- https://docs.microsoft.com/aspnet/
- https://docs.microsoft.com/dotnet/
- https://docs.microsoft.com/enterprise-mobility-security

Jusqu’à 45 minutes peuvent être nécessaires pour que les articles apparaissent en ligne après la publication. Une fois votre article publié, vous pouvez vérifier vos modifications à l’URL appropriée : `https://docs.microsoft.com/<path-to-your-article-without-the-md-extension>`.
