## Objectifs
Créer une API permettant de gérer le ressenti météo dans les villes qui nous entourent

## Ressources 

 Lister toutes les villes
```
GET /cities
response : [
	{
		zipCode: string,
		name: string
	}
]
```

Détail d'une ville
```
GET /cities/{zip-code}
response : {
	zipCode: string,
	name: string
}
```

Suppression d'une ville
```
DELETE /cities/{zip-code}
response : {}
```

Modification d'une ville
```
PUT /cities/{zip-code}
body: {
	name: string
}
response : {
	zipCode: string,
	name: string
}
```

Météo d'une ville (on indique la tendance la plus représentée)
```
GET /cities/{zip-code}/weather
response : {
	zipCode: string,
	name: string
	weather: "pluie"|"beau"|"neige"
}
```

Ajout d'un bulletin météo (en réponse, on récupère l'id du bulletin météo)
```
POST /cities/{zip-code}/weather
body : {
	zipCode: string,
	weather: "pluie"|"beau"|"neige"
}
response: {id: number}
```

Suppression d'un bulletin météo 
```
DELETE /weather/{id}
response: {}
```

Détail d'un bulletin météo (2 routes)
```
GET /cities/{zip-code}/weather/{id}
GET /weather/{id}
response : {
	id: number, 
	zipCode: string,
	townName: string,
	weather: "pluie"|"beau"|"neige"
}
```

Bulletin météo de toutes les villes
```
GET /weather
response : [
	{
		zipCode: string,
		townName: string,
		weather: "pluie"|"beau"|"neige"
	}
]
```

## Notation

- commit propre et séparée par fonctionnalité / route : 1
- tests fonctionnels : 1
- gestion des différents code d'erreur : 1
- présence de log cohérents : 1
- script curl ou http file : 1
- point par route effectuée et fonctionnelle : 5 (0.5 point par route pour un total de 10 routes)
- note arbitraire sur l'état général du code, le fonctionnement global, les bugs, la clareté : 10

Dans la note arbitraire, je vérifierai en particulier ces points : 
- l'application doit pouvoir être lancée en production 
- les code http renvoyés sont cohérents
- les données restent cohérentes après l'utilisation des routes
- les noms de variables et de fonctions sont explicites

Vous avez le droit :
- de travailler en groupe de 2 ou 3. La note sera identique pour chaque membre du groupe
- d'utiliser internet
- de poser des questions
- de demander à un autre binôme de faire une revue de code
- vous avez le droit d'utiliser l'IA, mais vous devez éviter le copier-coller et vous devez toujours être en contrôle de votre code. Je passerai régulièrement faire des revues de code. En cas de doute, je vous poserai des questions qui auront un impact sur la note arbitraire. 
