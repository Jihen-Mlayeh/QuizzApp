# 🎯 Quiz France - Application Flutter

## 🎯 Aperçu

Quiz France est une application mobile développée en Flutter permettant de tester ses connaissances sur la France à travers 15 questions de type Vrai/Faux. L'application propose **deux modes de gestion d'état** : Provider et BLoC.

### ✨ Caractéristiques Principales

- 📚 **15 Questions** réparties en 5 catégories
- 🎨 **Interface Moderne** avec animations fluides
- 🔄 **Deux Modes** : Provider et BLoC
- 📊 **Feedback Visuel** instantané
- 🏆 **Page de Résultats** détaillée
- 🌈 **Thème Personnalisé** avec dégradés

---

## ⚡ Fonctionnalités

### Questions & Catégories

| Catégorie | Nombre de Questions |
|-----------|---------------------|
| Histoire | 4 |
| Géographie | 5 |
| Culture | 5 |
| Sport | 1 |


## 📦 Prérequis

Avant de commencer, assurez-vous d'avoir installé :

- **Flutter SDK** : `>= 3.0.0`
- **Dart SDK** : `>= 3.0.0`
- **Android Studio** / **VS Code** avec extensions Flutter
- **Git**

### Vérification de l'Installation

```bash
flutter doctor
```

Assurez-vous que tous les éléments affichent ✓.

---

## 🚀 Installation

### 1. Cloner le Projet

```bash
git https://github.com/Jihen-Mlayeh/QuizzApp
cd QuizzApp
```

### 2. Installer les Dépendances

```bash
flutter pub get
```

### 3. Vérifier les Dépendances

```bash
flutter pub outdated
```

### 4. Lancer l'Application

#### Sur Émulateur Android
```bash
flutter run
```

#### Sur Émulateur iOS (macOS uniquement)
```bash
flutter run -d ios
```

#### Sur Navigateur Web
```bash
flutter run -d chrome
```

#### Sur Windows
```bash
flutter run -d windows
```

---

## 📁 Structure du Projet

```
lib/
├── main.dart                           # Point d'entrée
│
├── business_logic/                     # Logique métier
│   ├── blocs/
│   │   ├── quiz_bloc.dart             # BLoC principal
│   │   └── quiz_state.dart            # États BLoC
│   └── events/
│       └── quiz_event.dart            # Événements BLoC
│
├── data/                               # Données
│   ├── models/
│   │   ├── question_model.dart        # Modèle Question
│   │   └── answer_model.dart          # Modèle Réponse
│   ├── providers/
│   │   └── quiz_provider.dart         # Provider Pattern
│   └── repositories/
│       └── quiz_repository.dart       # Source de données
│
└── presentation/                       # Interface
    ├── pages/
    │   ├── menu_page.dart             # Menu principal
    │   ├── home_page.dart             # Quiz BLoC
    │   ├── home_page_provider.dart    # Quiz Provider
    │   ├── result_page.dart           # Résultats BLoC
    │   └── result_page_provider.dart  # Résultats Provider
    ├── widgets/
    │   ├── question_card.dart         # Carte question
    │   ├── answer_button.dart         # Bouton réponse
    │   └── progress_bar.dart          # Barre progression
    ├── animations/
    │   └── animated_background.dart   # Fond animé
    └── themes/
        └── app_theme.dart             # Thème app
```

---

## ⚙️ Configuration

### Fichier `pubspec.yaml`

```yaml
name: quiz_france
description: Application de quiz sur la France

environment:
  sdk: ">=3.0.0 <4.0.0"

dependencies:
  flutter:
    sdk: flutter
  
  # Gestion d'état
  provider: ^6.1.1
  flutter_bloc: ^8.1.3
  
  # UI
  cupertino_icons: ^1.0.6

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.1
```

### Installation des Packages

```bash
# Provider
flutter pub add provider

# BLoC
flutter pub add flutter_bloc
flutter pub add bloc
```

---

## 🎮 Utilisation

### Démarrage Rapide

1. **Lancez l'application**
2. **Choisissez un mode** : Provider ou BLoC
3. **Répondez aux questions** (Vrai/Faux)
4. **Visualisez votre score** à la fin

### Navigation

```
Menu Principal
    ├── Mode Provider → Quiz (15 questions) → Résultats
    └── Mode BLoC     → Quiz (15 questions) → Résultats
```

### Raccourcis Clavier (Desktop)

- `R` : Hot reload
- `Shift + R` : Hot restart
- `Q` : Quitter

---

## 🏗️ Architecture

### Diagramme de l'Architecture

```
┌─────────────────────────────────────────┐
│          PRESENTATION LAYER             │
│  (Pages, Widgets, Themes, Animations)   │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│       BUSINESS LOGIC LAYER              │
│    (Provider / BLoC / Events / States)  │
└──────────────┬──────────────────────────┘
               │
┌──────────────▼──────────────────────────┐
│            DATA LAYER                   │
│   (Models, Repository, Data Source)     │
└─────────────────────────────────────────┘
```

---

## 📚 Dépendances

### Principales

| Package | Version | Usage |
|---------|---------|-------|
| `flutter` | SDK | Framework |
| `provider` | ^6.1.1 | Gestion d'état simple |
| `flutter_bloc` | ^8.1.3 | Gestion d'état avancée |
| `bloc` | ^8.1.2 | Core BLoC |

### Dev Dependencies

| Package | Version | Usage |
|---------|---------|-------|
| `flutter_test` | SDK | Tests unitaires |
| `flutter_lints` | ^3.0.1 | Linter Dart |

---


