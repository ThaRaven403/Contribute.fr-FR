# <a name="locale-specific-links"></a>Liens spécifiques aux paramètres régionaux

Les codes de paramètres régionaux, comme `en-us`, ne doivent pas être inclus dans les liens vers certains sites Microsoft. Si un code de paramètres régionaux est inclus dans un lien dans du contenu en anglais, il l’est également dans les liens traduits, ce qui entraîne une mauvaise expérience de contenu traduit. Par exemple, si un lien dans du contenu traduit en allemand inclut `en-us`, les clients allemands sont dirigés vers l’article en anglais, même si une version allemande est disponible.

Supprimez les codes de paramètres régionaux des liens vers des sites Microsoft. Voici un exemple.

Avant :

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

Après :

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

Les sites suivants sont dans la portée de cette validation :

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com