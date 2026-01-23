# 📁 Rapport Technique - SAÉ S1.03

![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple?style=for-the-badge&logo=bootstrap)
![Arch Linux](https://img.shields.io/badge/EndeavourOS-Arch_Linux-blue?style=for-the-badge&logo=arch-linux)
![Apache](https://img.shields.io/badge/Server-Apache_HTTP-red?style=for-the-badge&logo=apache)

> **Installation et Configuration d'un Poste de Travail Linux (Virtualisé)**
>
> 
 ### **Groupe 108 - Binôme 05**
 * Mattéo DE CARVALHO
 * Louis TCHOUANGOU
 * Mathieu FREY

Ce dépôt héberge le site web statique servant de rapport technique pour la SAÉ S1.03. Il documente l'intégralité du processus d'installation, de configuration et de mise en réseau d'un serveur Web sous Linux.

## 🌐 Accès au Site
Le rapport est consultable directement en ligne via GitHub Pages :
👉 **[Voir le Rapport en Ligne](https://Matdecar.github.io/RapportWeb-SAE-S103/)**

---

## 💻 Environnement Technique

Le projet a été réalisé en exploitant la puissance d'un hôte physique performant pour simuler des conditions de production confortables.

| Composant | Détails |
| :--- | :--- |
| **Machine Hôte** | Asus Zephyrus G14 (Ryzen 9 / 32 Go RAM) |
| **Hyperviseur** | VirtualBox 7.x |
| **OS Invité (VM)** | **EndeavourOS** (Base Arch Linux) |
| **Allocation VM** | 8 Go RAM / 4 vCPUs / 50 Go Stockage |
| **Serveur Web** | Apache HTTP Server (httpd) |
| **Outils Dev** | PhpStorm (JetBrains), Git |

## 🚀 Fonctionnalités du Projet

### 1. Infrastructure Système
* Installation d'un système Linux basé sur Arch (EndeavourOS).
* Configuration du chargeur d'amorçage **EFI** (indispensable pour les partitions GPT).
* Optimisation graphique : Utilisation du contrôleur **VMSVGA** + 128 Mo VRAM pour corriger les bugs d'affichage (écran noir) liés au GPU hybride de l'Asus G14.
* Gestion des utilisateurs et des groupes (`admin_gr108_binome05`, groupe `binome05`).

### 2. Configuration Réseau
* Mise en place initiale en **NAT** avec redirection de port (Host 8080 -> Guest 80).
* Migration vers un mode **Pont (Bridged Adapter)** pour rendre la VM accessible publiquement sur le réseau local (Wi-Fi).

### 3. Le Site (Rapport)
* **Interface :** Développée en HTML5 / CSS3 avec le framework **Bootstrap 5**.
* **Design :** Thème sombre ("Dark Mode") avec code couleur personnalisé.
* **Interactivité :**
    * Animations CSS fluides au survol.
    * Système de **Zoom** sur les captures d'écran (sans JavaScript lourd).
    * Navigation multi-pages détaillée.

## 📂 Structure du Dépôt

```text
├── assets/
│   ├── css/       # Styles personnalisés et animations
│   └── img/       # Preuves techniques (Captures d'écran VM)
├── index.html     # Page d'accueil (Résumé matériel)
├── system.html    # Détails de l'installation OS
├── reseau.html    # Configuration Apache et Bridged
├── administration.html # Gestion utilisateurs et Bash
├── journal.html   # Historique des problèmes résolus
├── zoom_user.html      # Vue détaillée : Création des comptes
├── zoom_reseau.html    # Vue détaillée : Configuration IP
├── zoom_web.html       # Vue détaillée : Test Apache
├── zoom_disque.html    # Vue détaillée : Partitionnement
└── README.md      # Documentation (ce fichier)
