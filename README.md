# Poly4 — Machine de Polymérisation

## Prérequis
- .NET 8 SDK (Windows) : https://dotnet.microsoft.com/download/dotnet/8.0
- Visual Studio 2022 ou VS Code avec extension C#

## Structure du projet
```
Poly4/
├── App.xaml              → Application + styles globaux
├── App.xaml.cs
├── Menu.xaml             → Page principale (paramètres + lancement)
├── Menu.xaml.cs
├── Progression.xaml      → Page de suivi de progression
├── Progression.xaml.cs
├── Parametres.xaml       → Page des paramètres
├── Parametres.xaml.cs
├── Poly4.csproj
└── Properties/
    └── AssemblyInfo.cs
```

## Lancer le projet
```bash
cd Poly4
dotnet run
```

## Ouvrir dans Visual Studio
1. Double-cliquer sur `Poly4.csproj`
2. Appuyer sur F5 pour démarrer

## Fonctionnalités
### Page Menu
- **Barre de tâches** : Logo, titre "Machine de Polymérisation", bouton Paramètres (⚙)
- **Nombre de cycles** : Slider de 1 à 10
- **Taille** : Slider de 5 à 30 (pas de 5)
- **Options** :
  - ☐ Nettoyage en fin de cycle
  - ☐ Nettoyage seul
- **Temps estimé** : Calcul automatique en bas à gauche
- **Bouton LANCER** : Ouvre la page de progression

### Page Progression
- **Barre de progression globale** avec pourcentage
- **Barre de progression du cycle actuel**
- **Informations en temps réel** : cycle actuel, temps restant, temps écoulé
- **Bouton ARRÊT** : Demande confirmation, puis retour au menu

### Page Paramètres
- Durée de base par cycle (1–60 min)
- Durée de nettoyage (1–30 min)

## Notes
- La progression est simulée en accéléré (x20) pour faciliter les tests.
- Pour un cycle réel, ajustez `_timer.Interval` dans `Progression.xaml.cs`.
