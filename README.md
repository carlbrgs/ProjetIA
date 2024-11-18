# Projet : Déterminer si une personne est sportive

Ce projet vise à développer un modèle capable de déterminer si une personne est sportive. Le projet est divisé en deux parties principales :

1. Analyse à partir de **données numériques** telles que BodyFat, Age, Weight, etc.
2. Analyse à partir de **données imagées**.

## 🎯 Objectifs

- **Première étape** : Construire un modèle basé sur des données numériques pour prédire si une personne est sportive.
- **Deuxième étape** : Construire un modèle basé sur des données imagées pour effectuer la même prédiction.

Les données imagées ont été récupérées depuis les sources suivantes :
- [Images2000 sur Kaggle](https://www.kaggle.com/datasets/ahmadahmadzada/images2000?resource=download)
- [LSP Dataset sur Activeloop](https://app.activeloop.ai/activeloop/lsp-train/firstdbf9474d461a19e9333c2fd19b46115348f)

---

## ⚙️ Étapes du projet

### 1. Préparation des données

#### Données numériques
- Les données numériques ont été préparées et formatées dans un dataframe.
- Elles représentent des informations statistiques ou physiques sur les individus.

#### Données imagées
- Les images ont été récupérées depuis les URL mentionnées ci-dessus.
- Les bibliothèques utilisées :
  - **Deeplake** : pour manipuler les données imagées.
  - **Kaggle** : pour importer le dataset Kaggle.
- Les images ont été transformées pour respecter le format requis par le modèle (redimensionnement, normalisation, etc.).

#### Fusion des données
- Les données numériques et imagées ont été harmonisées au même format.
- Cela a permis de concaténer les deux sources dans un unique dataframe pour un entraînement plus fluide.

---

### 2. Entraînement des modèles

#### Modèle basé sur des données numériques
- Un premier modèle a été développé en utilisant des techniques classiques de machine learning :
  - Exemples : **SVM**, **MLPClassifier**.
- Résultats satisfaisants avec un bon taux de prédiction sur les données de test.

#### Modèle basé sur des données imagées
- Un réseau de neurones convolutif (**CNN**) a été entraîné sur les images.
- Résultats :
  - Les performances du modèle n'ont pas atteint les attentes.
  - Possibles causes :
    - Taille réduite du dataset.
    - Manque d'expérience avec les modèles d'images.
    - Problèmes de surajustement ou qualité des données.

#### Test des modèles
- Les deux modèles ont été testés sur un jeu de données construit manuellement pour évaluer leur efficacité dans des cas concrets.

---

## 🚧 Difficultés rencontrées

- **Préparation des données** : 
  - Fusionner et mettre au même format les données imagées et numériques a nécessité beaucoup de travail.
- **Entraînement des modèles** :
  - Le modèle basé sur les images était instable, avec des résultats imprévisibles.
- **Performances limitées** :
  - Les résultats étaient inférieurs aux attentes, surtout pour le modèle d'images.

---

## 🛠️ Technologies utilisées

- **Langage** : Python
- **Bibliothèques principales** :
  - Pandas
  - NumPy
  - Scikit-learn
  - TensorFlow/Keras (pour le modèle d'images)
  - Deeplake
  - Kaggle

---

## 📊 Résultats et conclusions

- **Modèle basé sur les données numériques** :
  - Obtenu des résultats satisfaisants, avec une bonne capacité de prédiction.
- **Modèle basé sur les données imagées** :
  - Résultats non-conformes à mes attentes.
  - Malgré tout, cette étape a permis de mieux comprendre les défis liés aux modèles basés sur des images.

---
