# Projet : Vote en Classe (P2P)

Application web de vote en direct pour la classe, fonctionnant de bout en bout et sans serveur de base de données, basée sur la technologie réseau pair-à-pair (PeerJS).

## 🚀 Fonctionnalités Principales

### 👨‍🏫 Mode Professeur
- **Création de session instantanée** : Génération d'un code alphanumérique unique à 6 caractères (ex: `A1B2C3`).
- **Accessibilité multi-supports** : Affichage d'un QR code pour les smartphones, et d'un code texte pour les ordinateurs.
- **Suivi en direct** : Affichage en temps réel du nombre de participants connectés et du nombre de votes exprimés.
- **Suspense** : Les résultats sont masqués par le message *"En attente de tous les votes"* tant que tout le monde n'a pas voté. L'affichage se fait automatiquement à 100% de participation, avec possibilité de forcer l'affichage.
- **Cartes de résultats** : Affichage visuel très clair sous forme de grandes cartes colorées.
- **Remise à zéro** : Relance un vote instantanément pour tous les élèves en un seul clic, via un système d'identifiant de session invisible.

### 🎓 Mode Élève
- **Rejoindre facilement** : Soit en scannant le QR code (le lien contient déjà la salle), soit en tapant le code depuis l'accueil (passage automatique en majuscules).
- **Interface simple** : 3 gros boutons arrondis (Oui, Non, Abstention).
- **Anti-triche intégré** : 
  - Une fois qu'un élève a voté, ses boutons se grisent instantanément.
  - S'il rafraîchit la page, la mémoire locale du navigateur (`sessionStorage`) couplée à l'identifiant caché de la question l'empêche de revoter.

## 🛠 Technique & Design
- **Réseau** : `PeerJS` (réseau WebRTC Pair-à-Pair)
- **Interface** : Framework `Bootstrap 5` avec le thème **Bootswatch Brite** (style "néobrutaliste").
- **CSS** : Séparé proprement dans un fichier `style.css`.
- **Zéro base de données** : Tout se passe directement dans le navigateur du professeur, assurant une confidentialité totale des votes !
