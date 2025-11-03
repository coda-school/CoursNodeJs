waitFor : 
    
```typescript
export async function waitFor(ms: number): Promise<void> {
    return new Promise((resolve) => setTimeout(resolve, ms));
}

async function run() {
    console.log("toto");
    await waitFor(1000);
    console.log("bis");
}
run();
```

## Les questions

- Lorsque je lance ts-node toto.ts, cela m'affiche l'erreur suivante :

```shell
λ ts-node toto.ts
TypeError: Unknown file extension ".ts" for C:\Projets\coda\toto.ts
    at Object.getFileProtocolModuleFormat [as file:] (node:internal/modules/esm/get_format:219:9)
    at defaultGetFormat (node:internal/modules/esm/get_format:245:36)
    at defaultLoad (node:internal/modules/esm/load:120:22)
    at async ModuleLoader.loadAndTranslate (node:internal/modules/esm/loader:580:32)
    at async ModuleJob._link (node:internal/modules/esm/module_job:116:19) {
  code: 'ERR_UNKNOWN_FILE_EXTENSION'
}
```
Solution, il manque un fichier tsconfig.json

```shell
npx tsc --init
```

--------

#33#

Il était une fois le Javascript fullstack
https://www.commitstrip.com/fr/2016/05/06/a-story-about-full-stack-javascript/?

Vu par chat gpt : https://chatgpt.com/share/69087329-40f8-8005-a833-4244733e8b05

Qu'est-ce que Node.js ?
C'est un environnement d'exécution en JavaScript open-source, multiplateforme et gratuit et oui les rats c'est gratuit effectivement jamie vous avez pas besoin de débourser 1 euro !!!!!!!!!!!!!!!!!!!! (ouais mais il faut l'héberger)

Concrètement, Node.js est un environnement bas niveau permettant l'exécution de JavaScript côté serveur. 

    NodeJS a pour package manager principal, npm qui se base sur le registre de paquets npmjs.org, créé et maintenu par Github (Microsoft)


    Node.js est créé par Ryan Dahl en 2009. Il à était imaginer suite à l’observation d’un chargement de fichier sur le site Flickr : Le navigateur ne savait pas quel pourcentage du fichier était chargé et devait adresser une requête au serveur web. Dahl à donc voulu développer une méthode plus simple. Le serveur web Mongrel de Ruby fût l’autre source d’inspiration du créateur, après que Dahl ai échoué dans plusieurs projets en différents langages, il commença à s’intéresser à JavaScript à la suite de la diffusion du moteur V8 (Moteur open-souce javascript développé par Web Google Chrome et Chromium, et non le moteur de voiture)


    Node.js intègre nativement le module http qui facilite la création de serveurs HTTP et HTTPS. Grâce à cette fonctionnalité, il est possible de mettre en ligne des sites et applications web directement, sans avoir besoin d'installer de serveur web externe comme Nginx ou Apache.


    Node.js 

     Crée par Ryan Dahl le 27 mai 2009, Node.js est une plateforme logicielle libre en Javascript. Il est écrit en Javascript, C++ et Python.Node.js est un environnement permettant l'exécution de JavaScript côté serveur.  Node.js est asynchrone, cela permet de traiter plusieurs informations à la fois.

    Node.js est utilisé notamment comme plateforme de serveur Web, elle est utilisée par Netflix, PayPal, LinkedIn, Microsoft.


    Dépot Git : https://github.com/nodejs/node



## Système asynchrone
Node js n'utilise qu'un seul thread, cela signifie qu'il ne peut traiter qu'une seul opération à la fois. Pour palier à cela et fonctionner efficacement, il delegue les tâches qu'il ne peut pas executer instantanement à d'autres thread puis vient récuperer le résultat une fois qu'ils ont finis l'execution.
Le systeme d'execution de Node js repose sur plusieurs composants : 
    le thread principal, celui qui execute le code de maniere general
    le client, celui qui fait les requetes
    le thread pool, qui permet d'executer les requetes plus complexe (asynchrone)
    l'event loop, qui orcherstre le fonctionnement de l'ensemble
Par exemple si on souhaite lire un fichier, il faut recuperer le fichier c'est un processus lent donc l'event loop va deleguer cette tache au thread pool pour ne pas bloquer le thread principal, un fois que le thread pool à  terminer de récuperer le fichier, il l'indique en l'ajoutant dans la file d'execution du thread principal qui est ainsi informer qu'il peut passer à l'execution du code lié à la récuperation du fichier

## TypeScript

    Typescript (donc javascript typé) est une surcouche (et un langage de programmation) permettant de corriger l'un des plus gros problème de Javascript qui est le manque de typage. Typescript utilise un compiler qui est un package nodeJS (tsc) pour compiler le code écrit en typescript en javascript avec plusieurs garde-fou pour éviter les plantages relatifs au manque de typage de javascript. Ca permet également de se rendre compte d'erreur avant l'execution du code.


## Javascript

La première version de Javascript a été publiée en mai 1996 et créée par Brendan Eich (ancien PDG de Mozilla, aujourd'hui à la tête de l'entreprise Brave). Ce langage a été créé en seulement 10 jours à l'époque où Mr Eich travaillait pour Netscape Navigator (ancêtre de Mozilla). Ce laps de temps très réduit est l'origine des nombreux raccourcis/problèmes de Javascript comme le typage ou le manque de Garbage collector.

## Outils

nvm : https://github.com/nvm-sh/nvm
npm: https://npmjs.org
pnpm > npm : https://pnpm.io/fr/

##Asynchrone

Il est non-bloquant et asynchrone, ce qui signifie que les opérations de lecture/écriture, comme la lecture de fichiers ou les requêtes réseau, ne bloquent pas le programme. Cela le rend particulièrement efficace pour des applications en temps réel, comme des chats ou des APIs.

## Les promesses

Promesses : Les promesses représentent une valeur qui sera disponible à l'avenir (résultat ou erreur). Elles améliorent la lisibilité du code en offrant des méthodes comme .then() et .catch() pour gérer le succès ou l'échec d’une opération asynchrone.

Node js: https://nodejs.org/fr/about

    est un  moteur d'exécution JavaScript orienté évènement. conçu pour faire des applications réseaux évolutives il a été influencée par des systèmes tels que Ruby Event Machine et Twisted de python. Un serveur est démarrer par un appel bloquant tel que EventMachine::run()

    repo officiel de node.js https://github.com/nodejs , https://github.com/pkgjs






##Avantages et inconvénients

###Avantages:
    

    Évolutivité facile

    Facile à apprendre

    Langage de programmation unique

    Avantages de Fullstack JS

    Offre de hautes performances

    Soutien d’une communauté importante et active

    Offre la liberté de développer des applications


###Inconvénients:
    

    Interface de programmation d’applications (API) instable

    Non efficace pour les applications à grande échelle

    Manque de soutien de la part des bibliothèques

    Modèle de programmation asynchrone

    Indisponibilité de développeurs Node.js expérimentés

source:tkt (https://www.yuhiro-global.com/fr/avantages-et-inconvenients-de-node-js/)

## Modules
Node.js utilise un système de modules afin d'organiser le code, tous les fichiers sont des modules isolés qui peuvent importer et exporter des fonctionnalités.

    L'écosystème de Node.js repose sur un principe de "small modules", énormément de petits packages qui combinés, créent des applications complexes, une approche qui a pour but de favoriser la maintenabilité et la durabilité des apps.


## Péremption des versions
https://nodejs.org/en/about/eol
NodeJS est mis à jour régulièrement, vous pouvez trouver les différentes versions sur le lien, ainsi que leur niveau de vulnérabilité.
La version actuelle est V25 sortie le 15 octobre 2025.

Plus de 1000 annonce Indeed et plus de 900 sur hellowork contienne le tag NodeJS d'ou l'importance de ce language

L’affaire left-pad (2016) — “un dev supprime 11 lignes et casse la moitié du web” :
En mars 2016, Azer Koçulu retire de npm un minuscule package appelé left-pad (11 lignes qui ajoutent des espaces au début d’une chaîne). Problème : il était une dépendance transitive de milliers de projets (Babel, React, etc.). Résultat : des builds partout dans le monde se mettent à planter jusqu’à ce que npm restaure d’urgence le package et change ses règles de suppression. L’épisode a servi d’électrochoc sur la fragilité de la supply chain JS. 
https://en.wikipedia.org/wiki/Npm_left-pad_incident

1) Aux origines : Joyent et la naissance de Node.js

    2009 — Ryan Dahl présente Node.js, un runtime asynchrone basé sur V8 (le moteur JS de Chrome).

    2010–2014 — Node se développe chez Joyent, qui emploie Ryan Dahl et sponsorise le projet. Joyent fournit l’infrastructure, mais Node est open-source : le code, la roadmap et les contributions viennent d’une communauté grandissante.

2) 2016 : Samsung rachète Joyent… mais pas Node.js

    Juin 2016 — Samsung acquiert Joyent (principalement pour ses activités cloud et expertise infra).

    Ce rachat ne porte pas sur Node.js : le projet reste open-source et continue sous l’égide de la Node.js Foundation.

    Joyent devient une filiale de Samsung, mais Node ne « change pas de propriétaire » (il n’en a pas, au sens commercial).


Avantages :

    Rapide et léger ( grace au modèle non bloquant)

    Meme langage côté client et serveur (JS)

    Enorme communauté et écosystème (npm)

    Excellent pour les applications en temp réel

Limites :

    Le modèle asynchrone peut devenir complexe (callbacks hell)

    Moins adapté aux calculs lourds CPU

    Pas multithread nativement (mais “worker threads” existent)



Infos via ChatGPT :
Node.js est un environnement d’exécution JavaScript qui permet d’exécuter du code JavaScript en dehors du navigateur, notamment sur un serveur.
Le même langage peut maintenant :

    créer des serveurs web,

    manipuler des fichiers,

    se connecter à une base de données,

    gérer des API ou de la logique métier côté back-end.



WebSocket avec Node.js = Temps réel parfait
✅ Bidirectionnel et instantané
✅ Faible latence
✅ Efficace en bande passante
✅ Parfait pour chat, jeux, dashboards



    DOCUMENTATION


fs (fichiers)
Lire/écrire des fichiers.

const fs = require('fs/promises');
const txt = await fs.readFile('a.txt','utf8');
await fs.writeFile('b.txt', txt);

------------------------------------------------------------------------------------

path (chemins)
Assembler/extraire des chemins portables.

const path = require('path');
const p = path.join(__dirname, 'data', 'file.json');

------------------------------------------------------------------------------------

os (infos système)
Infos OS, CPU, RAM, home, tmp…

const os = require('os');
console.log(os.platform(), os.homedir());

------------------------------------------------------------------------------------

process (processus Node)
Env, arguments, CWD, sortie.

console.log(process.env.NODE_ENV);
const [, , name='world'] = process.argv;
console.log('Hi', name);

------------------------------------------------------------------------------------

http (serveur HTTP)
Serveur sans dépendances.

const http = require('http');
http.createServer((req,res)=>{res.end('OK');})
  .listen(3000);

------------------------------------------------------------------------------------

https (HTTP sécurisé)
Comme http mais avec TLS.

const https = require('https');
https.get('https://example.com', res => res.pipe(process.stdout));

------------------------------------------------------------------------------------

url (objets URL)
Parser/construire des URLs.

const { URL } = require('url');
const u = new URL('https://ex.com/path?a=1');
u.searchParams.set('b','2'); // -> https://ex.com/path?a=1&b=2

![images/01.png]



