# Ajouter un nouveau bot (available-bots.json)

Pour ajouter un bot, ajoute un nouvel objet dans le tableau du fichier **available-bots.json** en respectant ce format :

## Format d’un bot
- **name** : nom du bot (unique)
- **description** : petite description (optionnel)
- **git** : lien du dépôt Git
- **node** : version majeure de Node.js requise (ex : 18, 20)
- **runCommand** : comment lancer le bot
  - **type** : "npm" ou "node"
  - **arg** : ex. "start" ou "index.js"
- **env** : liste des variables d’environnement nécessaires (laisser vide après le "=" si besoin)

## Exemple
```json
{
  "name": "MyBot",
  "git": "https://github.com/user/mybot.git",
  "node": 20,
  "runCommand": { "type": "npm", "arg": "start" },
  "env": ["SESSION_ID=", "PREFIX=."]
}
```

## Rappels
- Le fichier doit être un JSON valide.
- Pas de virgule en trop.
- Utilise toujours des guillemets doubles.
