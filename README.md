# Prédiction de la Réadmission Non Planifiée en Réanimation (ICU) à J7

## 📌 Description du projet

Ce projet a été réalisé dans le cadre de l'Unité d'Enseignement "Machine Learning in Healthcare". 

**Contexte clinique :** Les réadmissions non planifiées en Unité de Soins Intensifs (ICU) sont associées à une surmortalité importante, à des séjours hospitaliers prolongés et à un fardeau financier majeur pour les systèmes de santé. 

**Objectif :** L'objectif de ce projet est de développer et de valider un modèle d'apprentissage automatique (Machine Learning) capable de prédire le risque de réadmission non planifiée en ICU dans les 7 jours suivant la sortie d'un patient. 

Le rapport scientifique détaillé de cette étude est disponible dans le dossier `Rapport/` : [rapport.pdf](Rapport/rapport.pdf).

---

## 🗄️ Accès aux données (MIMIC-IV)

Ce projet utilise la base de données clinique publique **MIMIC-IV v3.1** (Medical Information Mart for Intensive Care).

⚠️ **Conditions d'accès et confidentialité :**
Conformément à la convention d'utilisation des données (Data Use Agreement) de PhysioNet, **aucune donnée brute de patient n'est hébergée sur ce dépôt GitHub**. 

Pour reproduire les résultats de ce projet, vous devez obtenir l'accès à MIMIC-IV :
1. Créer un compte sur [PhysioNet](https://physionet.org/).
2. Valider la formation requise sur l'éthique de la recherche humaine (CITI Program).
3. Signer l'accord d'utilisation des données pour MIMIC-IV.
4. Télécharger le dataset depuis la page officielle : [MIMIC-IV v3.1 sur PhysioNet](https://physionet.org/content/mimiciv/3.1/).

Une fois l'accès obtenu, placez les fichiers CSV nécessaires extraits (ou issus de vos requêtes BigQuery) dans le dossier `data/` à la racine de ce projet.

---

## ⚙️ Installation de l'environnement

Le projet a été développé en Python 3.x. Pour garantir la reproductibilité, il est fortement recommandé d'utiliser un environnement virtuel.

# Création de l'environnement
python -m venv .venv

# Activation sur Windows
.venv\Scripts\activate

# Activation sur macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt



## 📁 Structure du dépôt

```text
mlh-icu-readmission/
│
├
│
├── data/               # Dossier (vide sur GitHub) destiné à recevoir les données MIMIC-IV brutes
│
├── figures/            # Graphiques générés par les modèles et utilisés dans le rapport
│
├── notebooks/          # Notebooks Jupyter (EDA, Feature Engineering, Modélisation)
│   ├── 01_cohort.ipynb
│   ├── 02_features.ipynb
│   └── 03_modeling.ipynb
│   └── 04_smote.ipynb  # Compare les perfs de la modélisation de base avec SMOTE
│
├
│── rapport.qmd     # Code source du rapport en Markdown/Quarto
│── rapport.pdf     # RAPPORT SCIENTIFIQUE FINAL (Livrable)
│
├── .gitignore          # Fichiers et dossiers ignorés par Git (ex: /data)
├── README.md           # Ce fichier
└── requirements.txt    # Liste exacte des dépendances Python
