# 🐳 Guide complet sur la conteneurisation

Support de cours et de révision pour comprendre **comment fonctionne un conteneur**, des primitives Linux jusqu'à l'utilisation de **Podman**, avec des TPs pratiques et une simulation d'examen.

> 💡 **Idée clé** : un conteneur n'est pas une machine virtuelle. C'est un processus Linux isolé par des **namespaces**, limité par des **cgroups**, et qui s'exécute dans un **rootfs** dédié.

---

## 📚 Contenu

### Chapitres (cours)

| # | Chapitre | Sujets abordés | Formats |
|---|----------|----------------|---------|
| 01 | Fondations Linux | Kernel, processus, filesystem, namespaces, cgroups | PDF |
| 02 | Container Runtime & OCI | Runtimes, containerd, runc, architecture Docker vs Podman, standard OCI | PDF · MD |
| 03 | Podman | Containerfile, ports, volumes, variables d'environnement, ARG vs ENV, réseaux | PDF · MD |

Chaque chapitre contient : schémas explicatifs, glossaire, points clés à retenir et questions de compréhension avec corrigés.

### Travaux pratiques

| TP | Titre | Objectif |
|----|-------|----------|
| [TP-01](TPs/TP-01.md) | Fondations de conteneurisation | Construire un conteneur **à la main** (rootfs Alpine, chroot, namespaces, cgroups) sans Docker ni Podman |
| [TP-02](TPs/TP-02.md) | Gérer les conteneurs avec Podman | Préparation à la certification **Red Hat EX188** avec une simulation d'examen |

---

## 🗂️ Structure du dépôt

```text
conteneurisation/
├── 01-Fondations-Linux.pdf
├── 02-Container-Runtime-OCI.md / .pdf
├── 03-Podman.md / .pdf
├── images/            # Schémas utilisés dans les cours et les TPs
└── TPs/
    ├── TP-01.md       # Lab guidé : conteneur manuel
    ├── TP-02.md       # Lab Podman + simulation d'examen
    ├── prep.sh        # Prépare l'environnement de l'examen
    └── grading.sh     # Corrige et calcule le score
```

---

## 🚀 Démarrage rapide

### 1. Cloner le dépôt

```bash
git clone https://github.com/AjmiOns/guide-complet-conteneurisation.git
cd guide-complet-conteneurisation
```

### 2. Lire les cours

Ouvrir les PDF, ou les fichiers `.md` directement sur GitHub. Ordre conseillé : **01 → 02 → 03**.

### 3. Faire les TPs

- **TP-01** : à réaliser sur une machine Linux avec les droits root.
- **TP-02** : à réaliser sur une VM **Red Hat** (ou compatible) avec Podman installé.

---

## 🧪 Simulation d'examen (TP-02)

Le TP-02 propose une simulation d'examen Podman notée sur **300 points** (réussite à **210**).

| Tâche | Points |
|-------|:------:|
| 1. Lancer des conteneurs simples | 30 |
| 2. Interagir avec les conteneurs | 45 |
| 3. Injecter des variables | 45 |
| 4. Construire des images personnalisées | 65 |
| 5. Déploiement multi-conteneurs | 75 |
| 6. Dépannage multi-conteneurs | 40 |

**Utilisation :**

```bash
cd TPs
bash prep.sh       # 1. prépare l'environnement
# 2. réaliser les tâches de l'énoncé
bash grading.sh    # 3. affiche le score
```

Énoncé de la simulation : <https://ex188-validation-test.lovable.app/>

---

## 🎯 Prérequis

- Bases de la ligne de commande Linux
- Une VM ou machine Linux (Red Hat / Fedora / CentOS recommandé pour Podman)
- `git`, `podman`

---

## 🧭 Ce que vous saurez faire à la fin

- Expliquer ce qu'est réellement un conteneur (namespaces, cgroups, rootfs)
- Différencier **container runtime**, **containerd**, **runc** et le standard **OCI**
- Comparer l'architecture de **Docker** et de **Podman**
- Construire des images, lancer et gérer des conteneurs avec Podman
- Configurer ports, volumes, variables d'environnement et réseaux

---

## 👤 Auteur

**Ons Ajmi**: Cloud Infrastructure Management Engineering student, TEK-UP University, Tunisia

[![GitHub](https://img.shields.io/badge/GitHub-AjmiOns-181717?style=flat-square&logo=github)](https://github.com/AjmiOns)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ons%20Ajmi-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/ons-ajmi--/)

---

## 📄 Licence

Projet à but pédagogique. Libre de consultation et de réutilisation .
---

<p align="center">
  <em>Un conteneur n'est pas de la magie : c'est un processus qu'on a bien isolé.</em>
</p>
