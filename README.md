# Analyse Logistique & Satisfaction Client – Dataset E-commerce (Olist) 

**Dataset :** [Brazilian E-Commerce – Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?resource=download)


Ce projet est basé sur le dataset **Brazilian E-Commerce – Olist**, issu de Kaggle.  
Le jeu de données regroupe l’activité d’une grande plateforme d’e-commerce : commandes, paiements, expéditions, produits, vendeurs et avis clients.

L’objectif de cette analyse est de :
- **évaluer la performance logistique**,  
- **identifier les facteurs qui influencent la satisfaction client**,  
- et **préparer des données propres et exploitables** pour guider des décisions opérationnelles (précision des estimations de livraison, catégories problématiques, géographies critiques).

Le travail s’articule autour d’un processus complet de **Data Wrangling**, suivi d’une **analyse exploratoire orientée business**.

---

## 🧹 Nettoyage des données

- Chargement des fichiers depuis Kaggle  
- Exploration initiale : `.head()`, `.info()`, `.describe()`  
- Conversion des types selon la sémantique :
  - dates, numériques, catégorielles  
- Normalisation des colonnes textuelles (ex. noms de ville) :
  - suppression des accents  
  - uniformisation des formats  
- Suppression :
  - des doublons  
  - des lignes invalides  
- Analyse et traitement des valeurs manquantes :
  - imputation, suppression, ou marquage contextuel

---

## 🔁 Transformation

- Création de nouvelles colonnes issues des données logistiques :
  - `durée_livraison` = date_livraison_réelle - date_achat  
  - `écart_livraison` = date_estimée - date_livraison_réelle  
  - `livraison_à_temps` (booléen)  
  - `montant_commande` (produits + frais)  
  - `montant_frais_commande`  
- Normalisation et nettoyage des attributs produits / clients

---

## 🧠 Enrichissement

- Sélection de variables pertinentes (feature engineering)  
- Jointures multi-tables :
  - informations géographiques des clients  
  - score de satisfaction (`review_score`)  

---

## 📊 Analyse exploratoire

- Distribution du score de satisfaction  
- Impact du **retard de livraison** sur les avis clients  
- Relations entre **montant de commande** et satisfaction  
- Villes et régions les plus touchées par les retards  
- Catégories de produits avec retards récurrents  
- Durée moyenne de livraison par catégorie

---

> Projet réalisé en Python dans le cadre d’un TD orienté Data Wrangling.  
> L’analyse met en lumière les leviers d’amélioration logistique pour optimiser l’expérience client.
