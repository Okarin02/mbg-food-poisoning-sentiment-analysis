# Sentiment Analysis of Public Opinion on MBG Food Poisoning Cases Using IndoBERTweet and SVM

## Research Workflow

### Step 1 – Data Collection

Notebook:

* `CODE_1_tweet__keracunan_MBG_.ipynb`
* `CODE_1_2_tweet__keracunan_makan_bergizi_gratis_.ipynb`

Activities:

* Collect tweets related to MBG food poisoning cases using Tweet Harvest.
* Store tweet metadata and text content.

Output:

* `Keracunan_mbg.csv`
* `Keracunan_mbg_2.csv`

---

### Step 2 – Tweet Selection Based on Reply Count

Activities:

* Filter tweets with at least 50 replies to obtain discussions with higher public engagement.

Output:

* `Keracunan_mbg_min_reply_50.csv`
* `Keracunan_mbg_min_reply_50_2.csv`

---

### Step 3 – Reply Collection

Activities:

* Collect replies and comments from selected tweets.

Output:

* `hasil_komentar_keracunan_mbg.csv`
* `hasil_komentar_keracunan_mbg_2.csv`

---

### Step 4 – Merge Tweets and Replies

Notebook:

* `CODE_3_gabung_tweet_dan_komentar.ipynb`

Activities:

* Merge tweet texts and reply texts into a single dataset.
* Remove duplicate records.

Output:

* `gabungan_tweet_komentar_text_bersih.csv`

---

### Step 5 – Initial Preprocessing and Sentiment Labeling

Notebook:

* `CODE_4_preprocessing_awal_dan_labeling_indobertweet.ipynb`

Activities:

* Initial text preprocessing.
* Sentiment labeling using IndoBERTweet.
* Generate sentiment labels: positive, negative, and neutral.

Output:

* `01_preprocessing_awal_indobertweet.csv`
* `02_hasil_labeling_indobertweet.csv`

---

### Step 6 – Advanced Preprocessing

Notebook:

* `CODE_5_Preprocessing_lanjtan_word_cloud.ipynb`

Activities:

* Cleaning
* Case Folding
* Text Normalization using Indonesian slang lexicon
* Tokenization
* Stopword Removal using Sastrawi
* Stemming using Sastrawi

Output:

* `03_hasil_preprocessing_lanjutan.csv`

---

### Step 7 – Feature Extraction and Data Splitting

Notebook:

* `CODE_5_Preprocessing_lanjtan_word_cloud.ipynb`

Activities:

* Split dataset into training data (70%) and testing data (30%).
* Extract textual features using TF-IDF.

---

### Step 8 – Sentiment Classification

Notebook:

* `CODE_5_Preprocessing_lanjtan_word_cloud.ipynb`

Activities:

* Train Support Vector Machine (SVM) classifier using TF-IDF features.
* Predict sentiment classes on testing data.

Output:

* `hasil_prediksi_svm.csv`

---

### Step 9 – Model Evaluation

Notebook:

* `CODE_5_Preprocessing_lanjtan_word_cloud.ipynb`

Activities:

* Classification Report
* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Output:

* Evaluation metrics and visualizations.

---

### Step 10 – Text Analysis and Visualization

Notebook:

* `CODE_5_Preprocessing_lanjtan_word_cloud.ipynb`

Activities:

* Top TF-IDF word analysis.
* Word frequency analysis.
* Word Cloud generation for each sentiment class.

Output:

* TF-IDF ranking tables.
* Word Cloud visualizations.
* Top 10 words per sentiment category.
