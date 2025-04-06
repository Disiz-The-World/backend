# backend

## Paramétrage du backend

Clonez le repository avec la commande :

```sh
git clone https://github.com/Disiz-The-World/backend.git
```

Installez les dépendances avec la commande (nécessite d'avoir Node installé et dans le PATH) :

```sh
npm i
```

Lancez le backend en utilisant la commande suivante :

```sh
npx json-server db.json --static public
```

## Architecture du backend

### Balades

Une balade est représentée de la manière suivante :

```jsonc
{
  "id": 1,
  "name": "Moudon par la petite porte",
  "catchPhrase": "...",
  "duration": 75,
  "location": 1510,
  "previewPath": "/1/preview.png",
  "map": "/1/map.png",
  "infos": [
    {
      "icon": "f816",
      "name": "Départ",
      "description": "Gare de Moudon",
    },
    {
      "icon": "f81b",
      "name": "Arrivée",
      "description": "Gare de Bressonaz",
    },
    {
      "icon": "f6ea",
      "name": "Distance",
      "description": "~5km",
    },
    {
      "icon": "f873",
      "name": "Dénivelé",
      "description": "+180m -180m",
    },
  ],
  "favoriteIds": [1, 2],
  "ratings": [1, 2, 3],
  "content": {
    "details": "...",
    "sections": [
      {
        "id": 1,
        "title": "Moudon par la petite porte",
        "content": [
          {
            "type": "text",
            "text": "...",
          },
          {
            "type": "image/normal",
            "path": "/1/2.jpg",
            "legend": "...",
          },
          {
            "type": "image/side",
            "path": "/1/1.png",
            "legend": "Carte: Hélène Becquelin.",
          },
        ],
      },
      {
        "id": 2,
        "title": "En route pour Moudon",
        "content": [
          {
            "type": "text",
            "text": "...",
          },
          {
            "type": "text",
            "text": "...",
          },
          {
            "type": "image/normal",
            "path": "/1/3.png",
            "legend": "Le long de la Broye sur le chemin du retour.",
          },
          {
            "type": "image/side",
            "path": "/1/4.png",
            "legend": "...",
          },
        ],
      },
      {
        "id": 3,
        "title": "La ville haute",
        "content": [
          {
            "type": "text",
            "text": "...",
          },
          {
            "type": "image/normal",
            "path": "/1/5.png",
            "legend": "...",
          },
          {
            "type": "image/side",
            "path": "/1/6.png",
            "legend": "",
          },
        ],
      },
    ],
  },
  "attributions": {
    "Illustrations": "Hélène Becquelin",
    "Textes": "Monique Fontannaz",
    "Images": "Jean-Claude Péclet",
  },
  "seeMore": ["...", "...", "..."],
  "tagIds": [1, 2],
}
```

### Tags

Un tag est représenté de la manière suivante :

```jsonc
    {
      "id": 1, // ID du tag dans la base de données
      "name": "Transports publics", // Nom du tag
      "icon": "e530" // Icône du tag (https://fonts.google.com/icons)
    },
```

### Users

Un user est représenté de la manière suivante :

```jsonc
    {
      "id": 1, // ID dans la base de données
      "username": "admin", // Username
      "password": "admin" // Mot de passe utilisateur
    },
```
