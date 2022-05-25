# 03 - Introduction DevSecOps

## Introduction

À travers cet atelier, nous allons revoir le concept de CI/CD où l'on incorporera la notion de sécurité.

Comme vu en cours, le *DevSecOps* peut intervenir dans la CI/CD à l'aide des solutions de testions que sont les **SAST** et les **DAST**. Ces solutions sont développées par de grande entreprise et constituent un business (donc solutions payantes). Par chance, sur GitHub Actions, on peut trouver des solutions *ready-to-go* gratuite.

## Atelier


Pour éviter de perdre du temps sur le développement, on va reprendre l'atelier 1 de [01-Introduction_CI/CD](https://github.com/rxinui-teaching/01-introduction-ci-cd/tree/atl1).

*Normalement, vous êtes censé l'avoir fini lors de notre dernière séance :)*

Mais dans le doute, la solution est disponible sur ce repository. 

### Choix d'atelier

Il est nécessaire de forker le projet. Cliquer sur Fork (en haut à droite) et choisissez votre compte. Cela permet de cloner mon repo GitHub sur votre compte personnel.

Cloner le votre repository forké sur votre compte GitHub sur votre machine locale en cliquant sur Code. Copier-coller l'URL qui est apparue et lancer sur votre machine la commande suivante :

```
git clone <url-copiée>
```

Pour séléctionner et débuter un atelier, veuillez lancer une des commandes indiquées ci-dessous.

1. Sécurité: Test SAST

```
git checkout -b atl1_actif origin/atl1
```

2. Sécurité: Test DAST

**Indisponible pour le moment**

```
git checkout -b atl2_actif origin/atl2
```