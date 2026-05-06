# 🔐 DevSecOps Lab

Projet de démonstration DevSecOps intégrant la sécurité à chaque étape du cycle de développement.

## 🎯 Objectif

Démontrer comment intégrer la sécurité automatiquement dans un pipeline CI/CD grâce aux outils DevSecOps.

## 🛠️ Stack technique

| Outil | Rôle |
|---|---|
| **Flask** | Application web Python |
| **Docker** | Conteneurisation |
| **GitHub Actions** | Pipeline CI/CD |
| **Bandit** | SAST - Analyse statique du code |
| **pip-audit** | SCA - Scan des dépendances |
| **Trivy** | Scan de l'image Docker (CVE) |
| **Prometheus** | Collecte des métriques |
| **Grafana** | Dashboard de monitoring |

## 🏗️ ArchitectureDeveloper
↓ git push
GitHub Actions Pipeline
├── SAST (Bandit)
├── SCA (pip-audit)
└── Scan Docker (Trivy)
↓
Docker Compose
├── App Flask    → port 5000
├── Prometheus   → port 9090
└── Grafana      → port 3000
 ## 🔐 Failles volontaires détectées

- ⚠️ Mot de passe codé en dur
- ⚠️ Mode debug activé en production
- ⚠️ Comparaison de mot de passe non sécurisée

## 🚀 Lancer le projet

### Prérequis
- Docker
- Docker Compose
- Git

### Installation

```bash
# Cloner le projet
git clone https://github.com/saralagrace/devsecops-lab.git
cd devsecops-lab

# Lancer tous les services
docker compose -f docker/docker-compose.yml up -d
```

### Accès aux services

| Service | URL |
|---|---|
| Application Flask | http://localhost:5000 |
| Prometheus | http://localhost:9090 |
| Grafana | http://localhost:3000 |

## 📊 Pipeline CI/CD

À chaque `git push` sur `main` :

1. **Bandit** → analyse statique du code Python
2. **pip-audit** → vérifie les dépendances
3. **Trivy** → scanne l'image Docker

## 🎓 Concepts DevSecOps couverts

- ✅ **Shift Left Security** → sécurité intégrée dès le développement
- ✅ **SAST** → Static Application Security Testing
- ✅ **SCA** → Software Composition Analysis
- ✅ **CVE** → détection de failles connues
- ✅ **IaC** → Infrastructure as Code
- ✅ **Monitoring** → surveillance en temps réel

## 👩‍💻 Auteur

**Saralagrace** — Alternance DevSecOps
