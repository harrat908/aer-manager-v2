# AER Manager • Aesthetic Equipment Repair

> **Application Android native de gestion de maintenance, SAV et diagnostic biomédical pour équipements esthétiques et médicaux.**  
> Développée avec **Kotlin & Jetpack Compose (Material 3)**, intégrée à **Google Gemini IA** et conçue pour les ingénieurs et techniciens biomédicaux en Algérie (devises DZD, fiches cliniques, rapports PDF).

---

## 🚀 Fonctionnalités Clés

### 1. 🏥 Gestion de Parc Machines & Cliniques
- **Clients & Cliniques** : Répertoire complet des médecins, dermatologues, chirurgiens et cliniques esthétiques (téléphone, adresse, géolocalisation, notes).
- **Parc Équipements Médicaux** : Fiches techniques détaillées par technologie :
  - **Lasers CO₂** fractionnés et chirurgicaux
  - **Diode Laser 808nm / 755nm / 1064nm**
  - **Nd:YAG Q-Switched & Pico**
  - **HIFU, IPL / DPL, Radiofréquence, Cryolipolyse, Hydrafacial**
- Suivi des dates d'achat, de mise en service, garanties constructeur et historique complet des interventions.

### 2. 🛠️ Gestion des Interventions & Rapports PDF
- Planification et suivi en temps réel des pannes et maintenances préventives.
- Niveaux de priorité (Urgent, Haute, Normale, Faible) et statuts (En cours, En attente pièce, Terminé).
- **Génération automatique de rapports d'intervention PDF professionnels** :
  - Mise en page vectorielle haute résolution.
  - Découpage et retour à la ligne automatique des diagnostics et observations.
  - Espace visa, cachet et signature technicien / praticien.
  - Génération de **devis commerciaux et factures proforma**.

### 3. 🤖 Assistant IA Biomédical (Google Gemini)
- Support technique et aide au diagnostic de pannes :
  - Défaillance tubes RF / optiques / miroirs galvanométriques.
  - Problèmes de refroidissement Peltier / circuits d'eau déminéralisée.
  - Perte de puissance et étalonnage joulemétrique.
- **Actions autonomes intégrées** : L'IA peut enregistrer directement des clients, machines et interventions dans la base locale à partir d'un ordre vocal ou textuel.
- **Google Maps Grounding** : Recherche et géolocalisation en direct des cliniques, cabinets et fournisseurs d'électronique en Algérie avec import en 1 clic.

### 4. 📊 Tableau de Bord Financier & Métriques SAV (DZD)
- Calcul automatique du chiffre d'affaires facturé, des dépenses réelles déboursées (pièces détachées, déplacements) et du **bénéfice net SAV**.
- Suivi de la marge commerciale sur pièces détachées et de la facturation de main-d'œuvre.
- Analyse visuelle des pannes récurrentes et catégories de défaillances.

### 5. ☁️ Synchronisation Cloud Firestore & Mode Hors-Ligne
- Base de données locale ultra-rapide **Room (SQLite)** : fonctionne parfaitement sans connexion Internet dans les blocs opératoires.
- Synchronisation bidirectionnelle automatique avec **Cloud Firestore** dès le retour du réseau.

---

## 🏗️ Architecture & Technologies

- **Langage** : Kotlin 2.2.10
- **UI Toolkit** : Jetpack Compose & Material 3
- **Base de données locale** : Room 2.7.0 (SQLite v3)
- **Asynchronisme** : Kotlin Coroutines & Flow
- **Intelligence Artificielle** : API Google Gemini (via OkHttp & JSON streaming)
- **Cloud** : Firebase Firestore & Firebase Auth
- **Génération de documents** : Android Native `PdfDocument` & Canvas API

---

## 💻 Installation & Lancement

### Prérequis
- [Android Studio Ladybug ou supérieur](https://developer.android.com/studio)
- JDK 17 ou supérieur
- Un appareil Android (API 24 minimum) ou un émulateur Android

### 1. Cloner le dépôt
```bash
git clone https://github.com/VOTRE_NOM/aer-manager.git
cd aer-manager
```

### 2. Configurer la Clé API Gemini
Créez un fichier `.env` à la racine du projet (ou configurez votre clé dans `local.properties`) :
```env
GEMINI_API_KEY=votre_cle_api_gemini_ici
```
> Vous pouvez obtenir une clé d'API gratuitement sur [Google AI Studio](https://aistudio.google.com).

### 3. Ouvrir dans Android Studio
1. Ouvrez Android Studio et cliquez sur **Open**.
2. Sélectionnez le dossier du projet.
3. Laissez Gradle synchroniser les dépendances.
4. Lancez l'application en cliquant sur **Run ▶**.

---

## 🔒 Sécurité & Bonnes Pratiques
- Le fichier `.gitignore` protège vos secrets (`.env`, `local.properties`, fichiers de keystore et caches de build).
- Ne commitez jamais votre clé d'API personnelle directement dans le code source.

---

## 📄 Licence
Projet sous licence propriétaire — Développé pour la maintenance biomédicale esthétique AER.
