# Ecoledirecte Api Documentation
Une doc permettant de comprendre l'api de ecoledirecte.

## Introduction
Bienvenue sur la documentation non officielle de l'api d'ecoledirecte.
Cette documentation est inspirée d'un autre projet github ('[ecoledirecte-api-docs](https://github.com/EduWireApps/ecoledirecte-api-docs)')
Si jamais cette documentation vient a être défaillante, merci de faire une issue avec les problèmes rencontrés
(Si jamais vous avez des idées de formatage, hésitez pas à me le faire savoir SpacyXyt)

## Sommaire
Un simple sommaire afin de naviguer facilement entre les différentes catégories.

- [Introduction](#introduction)
- [Login](#login)

## Format de la documentation
Les requêtes prennent soit des query string dans l'URL (ex: ``https://api.exoldirecte.com/example.awp?requete=marequete``) soit du JSON dans le corp de la requête, example:
```
fetch('https://reqbin.com/echo/post/json', {
    method: 'POST',
    headers: {
        'Accept': 'application/json',
        'Content-Type': 'application/json'
    },
    body: JSON.stringify({ "requete": "marequete" })
})
```

**Important**: Toutes demande à l'api sont effectuer en ``POST`` (``method: 'POST'``). Il faut aussi envoyer un paramètre ``verbe`` (``/example.awp?verbe=POSTE``) utilisé pour spécifier le verbe HTTP. Ici nous n'utiliseront pas ce paramètre, en vue du fait que même sans celui-ci la requête est fonctionel.

Les réponses de l'api ressemble à cela:
```{
  "host": "HTTP<n° serveur>",
  "code": 200, // Ou autre en cas d'erreur
  "token": "<token>",
  "message": "", // Rarement présent hors erreur, sinon en cas d'erreur
  "data": {...},
}```

Mais dans l'api il n'y aura que les données dans ``data`` qui vont seront vraiment utiles, c'est dans cette partie de la réponse que vous trouverez ce que vous avez demander à l'api.

## Login
