# 03 - Introduction DevSecOps

## Atelier 1 : test SAST

### Introduction

Cet atelier met en pratique l'usage d'une solution SAST. Pour se faire, nous allons utiliser GitHub Actions comme base pour concevoir notre CI/CD et y implanter le test SAST.

### Exercice 

Contrairement aux autres ateliers, celui-ci est libre d'être réalisé seul ou en binôme (aux moyens de branches git et *pull request* vu sur [02-Manipuler_git](https://github.com/rxinui-teaching/02-manipuler-git)).

Aussi, cet atelier demande beaucoup d'autonomie dans les démarches à effectuer. Il est moins guidé que les précédents.

Les principales ressources à voir sont :
- [01-Introduction_CI/CD](https://github.com/rxinui-teaching/01-introduction-ci-cd) pour la manipulation de la CI/CD
- [SAST de 42Crunch](https://github.com/42Crunch/api-security-audit-action) à utiliser pour implémenter la partie sécurité
- [Docs officielle de Swagger / OpenAPI](https://swagger.io/docs/specification/about/)

L'utilisation de l'action 42Crunch requiert l'usage de Swagger/OpenAPI. OpenAPI est un standard qui permet de spécifier une API en `json` ou `yaml`. L'intérêt est de concevoir l'API de manière fonctionnelle sans utiliser un quelconque langage de programmation. Il est même possible de tester une API spécifier en `json` sans aucune ligne de code. Grâce à ce standard, l'API est compréhensible par tous et non que par les développeurs (ie. manager, business owner, ...) et permets de concrétiser une application sans se fixer un langage de programmation.

C'est sur ce standard que se base l'inspection de code de 42Crunch. Il va évaluer la spécification de votre API plutot que votre code d'implémentation. En effet, la spéfication sert de guide / modèle à l'implémentation. Si votre implémentation diffère de votre spécification, alors votre implémation est incorrecte. C'est le b.a-ba du développement logiciel.

Cela dit, pour cet atelier, nous allons créer notre spécification à partir de notre implémentation (*on brise le tabou*). La spécification de notre api est `atelier/openapi.yml` et est écrit au format YAML.

1. **TODO**: Modifier la chaine CI/CD pour inclure l'action 42Crunch afin qu'il analyse la spécification de l'API à chaque évènement de type `push` sur la branche `atl1_actif`. S'aider de [SAST de 42Crunch](https://github.com/42Crunch/api-security-audit-action). Mettre le seuil de validation des contraintes de sécurité à `80`.

Un audit sera réalisé par 42Crunch et sera mis à disposition dans la CI/CD. Parcourir les logs de la CI/CD pour trouver le lien qui vous redirigera vers l'analyse sécuritée fait par 42Crunch.

2. **TODO**: Après avoir lu l'audit, modifier la spécification de sorte à ce que le score atteigne `>=95`. Pour recalculer le score, il suffit de créer un nouveau commit et de déposer les changements sur le serveur GitHub.

*NB: Celui qui a le meilleur API score gagne :)*

**ATTENTION: Il ne vous est pas demandé de modifier l'implémentation du code, uniquement la spécification `atelier/openapi.yml`.**

3. **TODO**: Arranger la CI/CD afin d'établir le job `build-test` uniquement si le job SAST est validé.

*That's all folks*