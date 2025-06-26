# TD Python – Data Wrangling avec le dataset Olist

**Dataset :** [Brazilian E-Commerce – Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?resource=download)

---

## Approche de préparation des données – Projet Olist

### 🧹 Nettoyage

- Chargement des fichiers directement depuis le site Kaggle
- Familiarisation avec la structure des données :
  - `.head()`, `.info()`, `.describe()`
- Conversion des types de données selon leur nature sémantique :
  - Dates, numériques, catégorielles, etc.
- Normalisation des colonnes textuelles (ex. : noms de ville) :
  - Suppression des accents
  - Harmonisation des formats
- Suppression :
  - Des doublons
  - Des lignes vides
- Analyse des valeurs manquantes :
  - Traitement contextuel : imputation, exclusion ou étiquetage

---

### 🔁 Transformation

- Création de nouvelles colonnes :
  - `durée_livraison` = `date_livraison_réelle` - `date_achat`
  - `écart_livraison` = `date_estimée` - `date_livraison_réelle`
  - `livraison_à_temps` (booléenne)
  - `montant_commande` = produits + frais de livraison
  - `montant_frais_commande` (frais isolés)

---

### 🧠 Enrichissement

- Sélection de variables pertinentes (feature engineering)
- Jointure avec la table des clients :
  - Informations géographiques
  - Score de satisfaction

---

### 📊 Analyse exploratoire

- Répartition du score de satisfaction (`review_score`)
- Impact du **retard de livraison** sur la satisfaction
- Influence du **montant de la commande** sur la satisfaction
- Villes avec le plus de **commandes en retard**
- Produits et catégories associés à des **retards fréquents**
- Durée moyenne de livraison par **catégorie de produit** (`groupby + mean`)

---

> Projet réalisé en Python dans le cadre d’un TD orienté Data Wrangling.
