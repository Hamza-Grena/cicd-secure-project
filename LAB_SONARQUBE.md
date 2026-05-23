# LAB SonarQube

## 1. Besoin

Dans une chaîne CI/CD professionnelle, il est important de vérifier la qualité du code avant de livrer une application.

SonarQube permet d’analyser automatiquement le code source afin de détecter :

- les bugs
- les vulnérabilités
- les mauvaises pratiques
- la dette technique
- les problèmes de maintenabilité

Dans ce projet, SonarQube est intégré avec Jenkins afin que chaque exécution du pipeline déclenche une analyse automatique du code.

## 2. Concepts clés

### Quality Gate

Le Quality Gate est un ensemble de conditions permettant de décider si le code est acceptable ou non.

Exemples de critères :

- absence de vulnérabilités critiques
- taux de duplication acceptable
- dette technique limitée
- couverture de tests suffisante

### Bugs

Les bugs représentent des erreurs potentielles dans le code qui peuvent provoquer un mauvais fonctionnement de l’application.

### Vulnerabilities

Les vulnérabilités représentent des faiblesses de sécurité pouvant être exploitées par un attaquant.

### Code Smells

Les Code Smells sont des mauvaises pratiques qui rendent le code difficile à maintenir.

### Clean as You Code

Le principe Clean as You Code consiste à garder propre le nouveau code ajouté au projet.

## 3. Installation de SonarQube

SonarQube a été installé avec Docker dans le fichier `docker-compose.yml`.

Extrait :

```yaml
sonarqube:
  image: sonarqube:lts-community
  container_name: sonarqube
  ports:
    - "9000:9000"
  networks:
    - cicd-network