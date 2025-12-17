# Projet Library Management
Système de gestion de bibliothèque développé en Python avec une interface graphique PyQt5 et une base de données SQLite.

## 📋 Description
Ce projet consiste en la gestion complète d'une bibliothèque permettant la gestion des livres, des emprunts et des retours, avec un système d'authentification utilisateur.

## ✨ Fonctionnalités prévues
- Ajouter, modifier et supprimer des livres
- Emprunter et retourner des livres
- Authentification utilisateur avec rôles (Administrateur et Membre)
- Gestion des utilisateurs
- Suivi des emprunts en cours

## 🏗️ Architecture du projet

Le projet suit une architecture en couches (layered architecture) pour une meilleure séparation des responsabilités :

```
Library_management/
│
├── conception/                          # Diagrammes de conception
│   ├── Diagramme de classes_Library_management.png
│   ├── Diagramme_UML_library_management.png
│   ├── Diagramme_de_sequence_Library_management.drawio.png
│   ├── MCD_library_management_v2.png
│   ├── Use_Case_Utilisateur_library_management.png
│   └── Use_case_Administrateur_library_management.png
│
├── app/
│   ├── __init__.py
│   │
│   ├── repositories/                    # Couche d'accès aux données
│   │   ├── __init__.py
│   │   ├── database.py                 # Gestion de la connexion à la base de données
│   │   └── book_repository.py          # Repository pour les opérations CRUD sur les livres
│   │
│   ├── services/                        # Couche logique métier
│   │   ├── __init__.py
│   │   └── book_service.py             # Logique métier pour la gestion des livres
│   │
│   └── ui/                              # Couche interface utilisateur
│       ├── __init__.py
│       ├── main_window.py              # Fenêtre principale de l'application
│       ├── book_table.py               # Tableau d'affichage des livres
│       ├── book_form.py                # Formulaire d'ajout/édition de livres
│       └── dialogs.py                  # Boîtes de dialogue (confirmation, erreurs, etc.)
│
├── main.py                              # Point d'entrée de l'application
├── requirements.txt                     # Dépendances Python
└── README.md                            # Documentation du projet
```

## 🎨 Conception

Le projet a été entièrement conçu avec les diagrammes suivants :

### Diagrammes UML
- **Diagramme de classes** : Modélisation des entités (Livre, Utilisateur, Emprunt) et leurs relations
- **Diagramme de séquence** : Flux d'interactions pour les opérations principales
- **Use Cases** : Scénarios d'utilisation pour l'administrateur et les utilisateurs

### Modèle de données
- **MCD (Modèle Conceptuel de Données)** : Structure de la base de données SQLite

Tous les diagrammes sont disponibles dans le dossier `/conception/`.

## 🛠️ Technologies utilisées

- **Python 3.x** : Langage de programmation principal
- **PyQt5** : Framework pour l'interface graphique
- **SQLite** : Base de données relationnelle légère

## 📦 Installation

1. Cloner le repository 
2. Installer python 3.12
3. Installer l'extension Draw.io pour lire les fichiers de conception
4. Importer PyQT5
