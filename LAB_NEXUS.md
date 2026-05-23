# LAB Nexus Repository

## 1. Besoin

Dans une chaîne CI/CD, il est nécessaire de stocker les fichiers générés par le build dans un dépôt centralisé.

Nexus Repository permet de stocker les artéfacts générés par Jenkins, comme les fichiers `.jar`.

Dans ce projet, Nexus est utilisé comme dépôt privé Maven.

## 2. Concepts clés

### Artéfact

Un artéfact est un fichier généré après la compilation d’un projet.

Exemple :

```text
secure-cicd-app-1.0.0.jar