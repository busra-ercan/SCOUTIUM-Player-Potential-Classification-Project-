# ⭐ Scoutium Player Potential Classification Project
### Predicting Football Player Potential Using Machine Learning

---

## 📌 Project Purpose

This project aims to predict whether a football player will be classified as **"average"** or **"highlighted"** based on real match evaluations performed by professional scouts on the Scoutium platform.

Using Machine Learning models, we transform subjective scouting evaluations into objective and reproducible predictions.

---

## 🎯 Why Machine Learning?

Traditional approaches are insufficient to capture:

- Non-linear relationships between player attributes  
- Interactions across dozens of features  
- Complex scoring patterns used by different scouts  

Machine Learning provides:

- Higher predictive accuracy  
- Automatic feature extraction  
- Ranking of the most important attributes  
- A more consistent and unbiased scouting support tool  

This project demonstrates how ML can support **talent identification**, **player development**, and **recruitment decisions** in modern football.

---

## 📊 Dataset Description

The dataset consists of two files provided by Scoutium:

1. **scoutium_attributes.csv**  
   - Player attribute evaluations per match  
   - Attributes include physical, technical, tactical and mental metrics

2. **scoutium_potential_labels.csv**  
   - Final potential classification assigned by scouts  
   - Target variable: `potential_label`  
     - `average`  
     - `highlighted`

After merging both datasets, the following preprocessing steps were applied:

- Removal of goalkeepers (`position_id = 1`)  
- Removal of minority class (`below_average`)  
- Pivot table creation (one row = one player)  
- Label encoding  
- Standard scaling  

---

## 🧠 Machine Learning Workflow

### ✔ Data Preprocessing
- Merge datasets (4 keys)
- Remove specific positions and rare labels
- Pivot table transformation
- Encode target variable
- Scale numerical features

### ✔ Models Applied
- KNN  
- Decision Tree  
- Random Forest  
- XGBoost  
- CatBoost  
- Logistic Regression  
- SVC  
- AdaBoost  
- Gradient Boosting  
- LightGBM  

### ✔ Hyperparameter Optimization
Performed using **GridSearchCV**, tuning:

- KNN  
- CART  
- Random Forest  
- XGBoost  
- CatBoost  

### ✔ Best Model
**Random Forest Classifier**


---

## 📈 Results

All Model Results (ROC-AUC):
KNN:      0.5088
CART:     0.8155
RF:       0.9084
XGBoost:  0.8838
CatBoost: 0.8879

Final Best Model: RF


Cross-validation confirmed high generalization performance.

---

## 🔍 Feature Importance

The model revealed the attributes most responsible for predicting player potential.  
Feature importance plots were generated to visualize this ranking.

---

## 🛠 Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- LightGBM  
- CatBoost  
- Matplotlib  
- Kaggle Notebook  

---

# ⭐ Scoutium Oyuncu Potansiyeli Sınıflandırma Projesi
### Makine Öğrenmesi ile Futbolcu Potansiyel Tahmini

---

## 📌 Projenin Amacı

Bu projenin temel amacı, profesyonel scout’lar tarafından maç sırasında verilen oyuncu özellik puanlarını kullanarak bir futbolcunun **“average (ortalama)”** mı yoksa **“highlighted (öne çıkan)”** mı olduğunu tahmin etmektir.

Scoutium platformundan elde edilen gerçek maç değerlendirmeleri kullanılarak, subjektif scout gözlemleri makine öğrenmesi modelleri yardımıyla **daha objektif ve yeniden üretilebilir** hale getirilmektedir.

---

## 🎯 Neden Makine Öğrenmesi?

Geleneksel yöntemler, futbolcu değerlendirmelerindeki:

- Çok boyutlu ilişkileri  
- Non-lineer yapıları  
- Scout’a özgü değerlendirme farklılıklarını  
- Yakalanması zor istatistiksel örüntüleri  

yakalamakta yetersiz kalmaktadır.

Bu nedenle makine öğrenmesi kullanmak:

✔ Daha yüksek tahmin performansı sağlar  
✔ Özellikler arasındaki karmaşık ilişkileri öğrenir  
✔ Önemli nitelikleri otomatik olarak ortaya çıkarır  
✔ Scout karar verme süreçlerine destek olur  
✔ Yetenek keşfi ve oyuncu geliştirme için güçlü bir araçtır

---

## 📊 Veri Seti Açıklaması

Çalışmada iki adet Scoutium veri seti kullanılmıştır:

### 1. **scoutium_attributes.csv**
- Oyuncuların maç sırasında aldığı attribute (özellik) puanları  
- Fiziksel, teknik, mental ve oyun görüşü gibi çeşitli özellikleri içerir

### 2. **scoutium_potential_labels.csv**
- Scout’un maç sonundaki oyuncu potansiyel etiketi  
  - `average`  
  - `highlighted`

### Yapılan Veri Hazırlama Adımları

- Kalecilerin çıkarılması (`position_id = 1`)  
- Nadir görülen `below_average` etiketinin kaldırılması  
- Oyuncu bazlı pivot-tablosu oluşturulması  
- Hedef değişkenin etiketlenmesi (Label Encoding)  
- Sayısal değişkenlerin ölçeklenmesi (StandardScaler)

---

## 🧠 Makine Öğrenmesi Süreci

### ✔ Veri Ön İşleme
- Veri setlerinin 4 kolon üzerinden birleştirilmesi  
- Kaleci ve nadir sınıfların temizlenmesi  
- Pivot table dönüşümü  
- Label Encoding  
- StandardScaler ile ölçeklendirme  

### ✔ Kullanılan Modeller
- Lojistik Regresyon  
- KNN  
- SVC  
- Karar Ağacı (CART)  
- Random Forest  
- AdaBoost  
- Gradient Boosting  
- XGBoost  
- LightGBM  
- CatBoost  

### ✔ Hiperparametre Optimizasyonu (GridSearchCV)
Aşağıdaki modellerde hiperparametre taraması yapılmıştır:

- KNN  
- CART  
- Random Forest  
- XGBoost  
- CatBoost  

### ✔ En İyi Model

🏆 **Random Forest Classifier**


---

## 📈 Sonuçlar

All Model Results (ROC-AUC):
KNN:      0.5088
CART:     0.8155
RF:       0.9084
XGBoost:  0.8838
CatBoost: 0.8879

Final Best Model: RF

Çapraz doğrulama (Cross-Validation) sonuçları da modelin tutarlı olduğunu göstermiştir.

---

## 🔍 Özellik Önem Düzeyleri

Random Forest modeli, oyuncu potansiyelini belirlemede en etkili attribute’ları ortaya çıkarmıştır.  
Bu sıralama grafikler ve CSV çıktılarıyla görselleştirilmiştir.

---

## 🛠 Kullanılan Teknolojiler

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- LightGBM  
- CatBoost  
- Matplotlib / Seaborn  
- Jupyter / Kaggle Notebook  





