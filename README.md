# Automated License Validator

Automatisation de la validation des licences pour sécuriser la chaîne de production logicielle (Supply Chain Security). Cet outil audite les dépendances Python et vérifie leur conformité légale avant le déploiement.

## 🎯 Objectifs du projet
- **Audit automatique** : Analyse récursive des dépendances installées.
- **Filtrage des licences** : Application de règles strictes (Whitelisting/Blacklisting) pour les licences (MIT, Apache vs GPL).
- **Intégration CI/CD** : Blocage automatique des builds en cas de non-conformité.

## 🛠 Architecture & Choix Techniques
L'outil repose sur une adaptation de la logique de vérification de paquets standards (type `liccheck`), configurée pour un environnement de production strict.

- **Langage** : Python 3.10+
- **Configuration** : Fichier `liccheck.ini` pour définir les stratégies de licences.
- **Parsing** : Analyse des dépendances via `pkg_resources`.
- **CI/CD** : GitHub Actions pour exécuter automatiquement l'audit à chaque push.

