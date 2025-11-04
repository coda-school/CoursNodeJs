# Comment tester notre API

Support de cours commun interactif : https://semestriel.framapad.org/p/codenodejs-gly0zj1ya6-ahok?lang=fr
Support de cours archivé : https://github.com/coda-school/CoursNodeJs/blob/main/support_commun.md

Vous pouvez noter dans ce support de cours commun les liens de référence, les exemples de code ou les prompts que vous utilisez. Vous pouvez aussi noter vos questions, vos observations, etc...

## Connexion
Renseignez-vous sur les méthodes de tests d'une API et indiquez dans le support de cours commun un concept qui attire votre attention. 

## 1. L'outil de base : curl
Vous êtes capables d'ajouter, supprimer, lire les données de votre serveur via des commandes curl.
### Livrable
 Vous devrez fournir un ou plusieurs exemples de chaque commande.
### Références
- https://curl.se/
- https://terminalcheatsheet.com/fr/guides/curl-rest-api
- https://blog.stephane-robert.info/docs/admin-serveurs/linux/curl/
## 2. L'outil de référence : postman
Comme avec curl, vous devez utiliser postman pour tester votre serveur
### Livrable
Vous avez une collection de requête permettant de manipuler votre serveur

### Références
- https://www.postman.com/
- https://welovedevs.com/articles/postman/
## 3. Directement dans l'IDE - http request file
Comme précédement, vous devez être capable d'utiliser les http request file pour exécuter des requêtes http.
### Livrable
Vous avez un fichier http qui permet de lancer chaque requête
### Références
- https://codewithandrea.com/tips/rest-client-vscode/
- https://kenslearningcurve.com/tutorials/test-an-api-by-using-http-files-in-vscode/

## 4. Les tests automatiques - vitest, tout simplement
Vous allez maintenant installer et utiliser vitest pour faire le même travail.
### Livrable
Vous avez une suite de tests qui permet de tester votre serveur. 
Vitest doit être installé sur votre poste et être en mesure de lancer cette suite de test.
### Références
- https://vitest.fr/guide/
- https://betterstack.com/community/guides/testing/vitest-explained/
- demander à l'ia d'expliquer comment tester le serveur actuel.

## 5.Les tests automatiques - vitest et supertest
Supertest permet d'enrichir vitest et de simplifier le test de vos API.
### Livrable
Une seconde suite de test basée sur supertest permettant de tester votre serveur.

### Références
- https://www.npmjs.com/package/supertest (attention, c'est du javascript)

## 6. Final : Terminer votre mini-serveur
Vous allez maintenant terminer votre mini-serveur en ajoutant les tests qui manquent (un par un). Dès qu'un test est en place, vous allez procéder à son implémentation.
### Livrable
Finir le mini-serveur avec toutes les routes attendues.

## Conclusion
Faire un schéma via exalidraw permettant de retracer le cours.