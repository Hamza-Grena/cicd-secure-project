# Construction d'une Chaîne CI/CD Sécurisée

## 1. Présentation du projet

Ce projet consiste à mettre en place une chaîne CI/CD sécurisée basée sur Jenkins, SonarQube et Nexus.

L’objectif est d’automatiser les étapes suivantes :

1. Récupération du code source depuis GitHub
2. Compilation de l’application avec Maven
3. Analyse de la qualité du code avec SonarQube
4. Publication de l’artéfact généré dans Nexus Repository

Ce travail s’inscrit dans le cadre du module CI/CD du Mastère CCDAD M1.

## 2. Architecture globale

La solution repose sur trois outils principaux :

- Jenkins : outil d’intégration continue permettant d’automatiser le pipeline
- SonarQube : outil d’analyse statique de code
- Nexus Repository : dépôt privé pour stocker les artéfacts générés

## 3. Technologies utilisées

- Ubuntu
- Docker
- Docker Compose
- Jenkins
- SonarQube
- Nexus Repository Manager
- Maven
- GitHub
- Java

## 4. Structure du projet

```text
cicd-secure-project/
├── docker-compose.yml
├── app/
│   ├── pom.xml
│   ├── Jenkinsfile
│   └── src/
├── docs/
│   ├── screenshots/
│   └── ai-prompts/
├── README.md
├── LAB_SONARQUBE.md
└── LAB_NEXUS.md