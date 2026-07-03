# 🌱 MyGarden

Projet d'Interaction Homme-Machine (IHM) réalisé dans le cadre d'un mini-projet universitaire.
MyGarden est une application mobile de jardinage qui aide les jardiniers amateurs à organiser, suivre et se souvenir de l'état de leur jardin, à partir de leurs propres données uniquement.

---

## 🧠 Principe du projet

- Aider un public de jardiniers **amateurs** (95% des sondés ne jardinent pas professionnellement) à s'organiser
- Répondre à deux besoins principaux identifiés par questionnaires et interview : **l'organisation** (notes, rappels) et **la représentation du jardin**
- Fonctionner uniquement à partir des données saisies par l'utilisateur, sans source externe ni dimension collaborative
- Cibler le smartphone comme médium principal, car 95% des personnes interrogées l'ont sur elles en jardinant

---

## 🕹️ Fonctionnalités retenues

- 📓 **Blog personnel** : entrées datées avec texte et photos, pour consigner observations et évolution du jardin, comme un journal de bord
- 🗺️ **Représentation du jardin en grille** : chaque case peut être personnalisée avec un type de plante ; permet de se souvenir de l'emplacement des plantations (30% des sondés en avaient du mal) et de leur nature (25%)
- ⏰ **Rappels personnalisés** : création de rappels datés et horodatés (arrosage, taille, achat d'engrais…) avec notifications, pour éviter les oublis (40% arrosent trop peu, 15% trop souvent)
- 🌸 **Fiches plantes personnalisées** : type de plante, besoins en eau, périodes de taille, saisis manuellement par l'utilisateur

---

## ❌ Fonctionnalités écartées (et pourquoi)

- **Notifications météo** : jugée trop dispersive par rapport à l'objectif principal
- **Amis / échanges entre utilisateurs**, **recherche de posts**, **revues de matériel certifié** : contredisent la contrainte de n'utiliser que des données fournies par l'utilisateur, et introduisent une dimension communautaire hors périmètre
- **Arrosage automatique connecté (Smart Home)** : éloignerait l'application de son objectif principal
- **Partage du jardin entre comptes** : complexité technique (synchronisation) jugée disproportionnée pour un outil centré sur un seul utilisateur

---

## 🎨 Prototypage

- **Wireframes basse fidélité** dessinés à la main pour chaque fonctionnalité (blog, grille du jardin, rappels, fiches plantes), puis assemblés en parcours complet
- **Prototype haute fidélité** réalisé sur Figma :
  - Fichier : [Figma – Projet IHM MyGarden](https://www.figma.com/design/GrZjU1G0qP3nHHvAgjgSib/Projet-IHM---MyGarden)
    
    <img width="721" height="693" alt="Capture d’écran 2026-07-03 à 12 41 03" src="https://github.com/user-attachments/assets/ecd87a8c-0cf9-43d8-8f4b-a30bcf9aea8b" />
    <img width="649" height="626" alt="Capture d’écran 2026-07-03 à 12 38 21" src="https://github.com/user-attachments/assets/24e23cbf-d5e5-41ce-b11e-5ea50f43aaf4" />

  - Prototype interactif : [lien du prototype Figma](https://www.figma.com/proto/GrZjU1G0qP3nHHvAgjgSib/Projet-IHM---MyGarden)

---

## 🔵 Choix de conception (IHM)

- **Architecture de l'information** : structure "liste + détail" — vue globale du jardin en accueil, liste des plantes, puis fiche détaillée par plante
- **Hiérarchie visuelle** : actions fréquentes (consulter une plante, marquer une tâche finie) immédiatement visibles ; actions secondaires accessibles via icônes
- **Navigation** : pensée selon un compromis espace-temps, peu profonde, pour minimiser les allers-retours
- **Ergonomie** : nombre d'actions limité par écran, boutons larges adaptés à un usage extérieur (mains sales, mobilité)
- **Couleurs et accessibilité** : palette naturelle (verts, tons neutres), information jamais portée uniquement par la couleur (icônes + texte), contrastes suffisants pour une lisibilité en extérieur
- **Principes de Gestalt** : séparation fond/forme pour distinguer clairement les éléments interactifs
- **Cohérence esthétique** : mêmes styles de boutons, couleurs et typographies sur tous les écrans


https://github.com/user-attachments/assets/e2338ed1-56f8-4a3c-b3be-bda7cc30bef1


---

## 🔴 Évaluation et limites identifiées

**Walkthrough fonctionnel** (ajout de plantes) :
- Lacune : la grille par défaut ne permet pas de représenter la forme réelle d'un jardin (en L, en cercle…)
- Amélioration proposée : outil de tracé géométrique pour dessiner les contours du jardin à l'initialisation

**Walkthrough d'interaction** :
- Marquer plusieurs actions d'une même plante comme terminées, ou créer un rappel pour plusieurs plantes, nécessitait de répéter la même boucle N fois (interaction linéaire et lente)
- Amélioration proposée : bouton "Tout marquer comme fini" et sélection multiple de plantes lors de la création d'un rappel (interaction factorisée)

**Évaluation GOMS** (opérateurs tactiles Tap/Prep) :
- Solution initiale (N=3 actions) : 4T + 3E = **2.3 s**
- Solution améliorée : 2T + E = **0.9 s**
- Gain de 1,4 s pour N=3, l'écart augmentant avec le nombre d'actions — validant le choix de factoriser l'interaction

---

## Remarques

Projet réalisé dans un objectif pédagogique, avec un accent sur :
- une démarche de conception centrée utilisateur (questionnaires, interview, idéation, prototypage, évaluation)
- l'architecture de l'information et la hiérarchie visuelle
- l'évaluation formelle de l'interaction (walkthrough, GOMS)

*Réalisé par NDIAYE Adama Fahbine, ORABI Zahra et YILDIRIM Defne Su — Groupe de TD 1*
