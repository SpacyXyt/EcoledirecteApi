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
Les requêtes prennent soit des query string dans l'URL (ex: ``https://api.exoldirecte.com/example.awp?requete=marequete``) soit du JSON dans le corp de la requête
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

## Login
