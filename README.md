<<<<<<< HEAD

# Fraud-detection

# 💳 Détection de Fraude par Carte Bancaire

## 📖 Description

Projet de machine learning appliqué à la **détection de fraudes bancaires**.  
Dataset déséquilibré (~0.2% de fraudes).  

Objectif : développer des modèles capables d’identifier efficacement les transactions frauduleuses.

---

## 📂 Structure

- `creditcard.csv` → Dataset des transactions normales et des fraudes
- `Data_Processed.csv` → Dataset `creditcard.csv`nettoyé et amélioré
- `project.ipynb` → Exploration & visualisation  
- `predict.ipynb` → Régression logistique, Random Forest, XGBoost, SMOTE, seuils  
- `Rapport final.pdf` → Rapport rédigé du projet 
- `README.md` → Rapport du projet 
- `requirements.txt` → Principales bibliothèques utilisées
- `outputs/` → Graphiques & matrices de confusion  

---

## 📊 Résultats principaux
| Modèle                | Précision (fraude) | Recall (fraude) | F1   | AUC   |
|------------------------|-------------------|----------------|------|-------|
| Logistic Regression    | 0.06              | 0.87           | 0.10 | 0.97  |
| Random Forest          | 0.88              | 0.76           | 0.82 | 0.94  |
| XGBoost                | 0.75              | 0.80           | 0.77 | 0.94  |
| RF + SMOTE (thr=0.4)   | 0.88              | 0.76           | 0.82 | 0.94  |
| XGB + SMOTE (thr=0.3)  | 0.70              | 0.82           | 0.75 | 0.94  |

---


📌 Problèmes rencontrés & solutions

Dataset déséquilibré → SMOTE, class_weight, seuils.

Mauvais recall de la baseline → RandomForest + tuning.

Faux positifs nombreux → ajustement des seuils.

Plots illisibles (matrices de confusion) → heatmaps annotées.

Données volumineuses → scaling + PCA déjà appliqué dans le dataset.


## 🛠️ Installation

1) Cloner le dépôt

```
git clone https://github.com/HDonzo/Fraud-detection.git
cd fraud-detection
```

2) Créer un environnement virtuel

```
python -m venv venv
source venv/bin/activate # Linux/Mac
venv\Scripts\activate # Windows
```

3) Installer les dépendances

```
pip install -r requirements.txt
```

4) Lancer Jupyter

```
jupyter notebook
```

🚀 Utilisation

```
# Exemple d'entraînement d’un modèle
from sklearn.ensemble import RandomForestClassifier
rf = RandomForestClassifier(class_weight="balanced", random_state=42)
rf.fit(X_train, y_train)
```



## 📌 Auteurs

👤 **Donovan H.**  
Projet personnel d’exploration et de prédiction sur des données bancaires, réalisé avec Python (pandas, sklearn, matplotlib, seaborn, xgboost, imbalanced-learn).



📜 Licence

MIT License
>>>>>>> b80e9ca (Ajout des notebooks EDA et Predict ainsi que requirements et README)
