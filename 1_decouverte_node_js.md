# Découverte de NodeJS.

Support de cours commun : https://semestriel.framapad.org/p/codenodejs-gly0zj1ya6-ahok?lang=fr

Vous pouvez noter dans ce support de cours commun les liens de référence, les exemples de code ou les prompts que vous utilisez. Vous pouvez aussi noter vos questions, vos observations, etc...

## Connexion
Renseignez-vous sur NodeJS et écrivez dans le support de cours commun un concept qui attire votre attention. 

## 1. Installer NodeJS
Vous devez installer NodeJS sur votre poste de travail. 

### Livrable
Vous êtes capable d'afficher la version de NodeJS installée sur votre machine avec la commande 

```shell
node -v
```

### Références
- https://nodejs.org/fr
- https://nodejs.org/fr/download

## 2. Installer Typescript
Vous devez installer typescript sur votre poste de travail

### Livrable
Vous êtes capable d'afficher la version de Typescript installée sur votre machaine avec la commande 

```shell
tsc --version
```

### Références
- https://www.typescriptlang.org/download/


## 3. Découvrir les modules standards
Vous allez découvrir certains modules standards de NodeJS : 
- fs
- path
- os
- process
- http
- https
- url

Attention : ignorez pour le moment la notion d'asynchronisme.

### Livrable
Un code mettant en oeuvre chaque module

## 4. Comprendre le fonctionnement de package.json
Vous allez maintenant comprendre comment fonctionne le fichier `package.json`

### Livrable
Un fichier `package.json` renseigné, avec à minima une dépendance et un script.

### Références
- https://docs.npmjs.com/cli/v11/configuring-npm/package-json
- https://talks.freelancerepublik.com/fichier-configuration-package-json-bien-utiliser/?utm_source=chatgpt.com

## 5.L'asynchronisme
Vous devez comprendre la notion d'asynchronisme et ces effets. Pour cela, vous devez découvrir les notions suivantes : 
- callback
- promises
- await / async

### Livrable
Un code mettant explicitement en évidence l'asynchronisme sous les 3 formes différentes (callback, promises et await / async)

## 6. Final : Créer un mini serveur http
Vous devez créer un mini serveur http en appliquant tous les concepts vus précédemment. Vous n'avez pas le droit d'utiliser un framework existant

### Livrable
Un code permettant de lancer un mini serveur http proposant au moins une route GET.

