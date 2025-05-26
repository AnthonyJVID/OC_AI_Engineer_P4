# 💳 OC - Projet 4 : Construisez un modèle de scoring

Ce projet est réalisé dans le cadre du parcours *AI Engineer* d’OpenClassrooms.  
Il simule une mission en tant que **Data Scientist** au sein de l’entreprise **Prêt à dépenser**, spécialisée dans l’octroi de crédits à la consommation à des clients avec peu ou pas d’historique.

---

## 🎯 Objectif

> Développer un modèle de **scoring crédit** permettant de prédire la probabilité de défaut d’un client, tout en assurant une bonne **interprétabilité** pour les équipes métier.

---

## 📁 Étapes réalisées

Le projet est structuré en deux notebooks :

### 1. Analyse exploratoire et feature engineering (`1_notebook_analyse_exploratoire_feature_enginering_092024.ipynb`)
- Analyse du déséquilibre des classes (clients solvables vs non solvables)
- Création de nouvelles variables pertinentes (features métiers)
- Nettoyage des données (valeurs manquantes, aberrantes)
- Visualisations descriptives pour identifier les patterns

### 2. Modélisation et interprétabilité (`2_notebook_modelisation_092024.ipynb`)
- Entraînement de plusieurs modèles de classification (logistique, RandomForest, XGBoost…)
- Prise en compte du **déséquilibre des classes** (undersampling, SMOTE, etc.)
- Optimisation des **hyperparamètres** via **GridSearchCV**
- Analyse **globale** de l’importance des variables (feature importance)
- Analyse **locale** via des outils d’interprétation (ex : SHAP)
- Évaluation métier via un **score personnalisé** prenant en compte :
  - Coût d’un faux négatif (FN) = 10
  - Coût d’un faux positif (FP) = 1
  - Optimisation du **seuil de prédiction** pour minimiser le coût total
- Évaluation classique via **AUC**, **accuracy**, **matrice de confusion**

---

## 📊 Métriques utilisées

- `AUC` (Area Under Curve)
- `accuracy`
- `precision`, `recall`, `f1-score`
- **Score métier personnalisé** basé sur le coût des erreurs

---

## 📈 Visualisations

- Distribution des variables cibles
- Matrice de confusion
- Importance des variables (globale et locale)
- Analyse du seuil optimal pour la classification

---

## 📁 Structure du projet

```
├── 1_notebook_analyse_exploratoire_feature_enginering_092024.ipynb  → Exploration + Feature Engineering
├── 2_notebook_modelisation_092024.ipynb                             → Modélisation + Évaluation
├── data/                                                            → Données client/finance (non fournies)
├── README.md                                                        → Présentation du projet
└── requirements.txt                                                 → Dépendances Python
```

---

## 🧠 Auteur

Projet réalisé par **AnthonyJVID** dans le cadre du parcours *AI Engineer* chez OpenClassrooms.

---

## 📄 Licence

Projet pédagogique à visée démonstrative, avec des données fictives.
