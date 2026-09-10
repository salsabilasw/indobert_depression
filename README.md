# Text Mining for Classifying Potentially Depressive Tweets on X Using IndoBERT
Model IndoBERT ini digunakan untuk riset tugas akhir (skripsi) klasifikasi teks berpotensi depresi dan normal/non-depresi, published in
Text Mining for Classifying Potentially Depressive Tweets on X Using IndoBERT. (2025). J Statistika: Jurnal Ilmiah Teori Dan Aplikasi Statistika, 18(2), 1073-1085. https://doi.org/10.36456/jstat.vol18.no2.a10873

### Code 
- crawling: crawl_Xkomen_depresi.ipynb
- preprocessing: prepoX_depresi.ipynb
- main: rill_skripsi_nt.ipynb

### Methods
- Crawling: 5,000 tweets from X users between October 1st, 2024, and January 31st, 2025 using Tweet Harvest
- Labelling: manually by 1 annotator assisted by a psychiatrist
- Preprocessing:
  - Case folding/ lowercasing
  - Cleaning
  - Normalization using https://github.com/nasalsabila/kamus-alay
  - Stop word removal
- Splitting: 80% train 20% test
- IndoBERT Tokenization
- Pre-Fine-Tuning Model using https://github.com/azizp128/prediksi-emosi-indobert
- Fine-Tuning Model using learning rate of 2e-05, batch size 8, and 2 epochs
- Evaluation
- Implementation to Streamlit + Confidence Score

### Results
- 4,987 clean data with 2 attributes (label and full_text), 3,281 normal and 1,706 potentially depressed.
- 3,989 data points for training and 998 for testing.
- The model works well for text mining in classifying potentially depressive and normal tweets, with an accuracy of 87%, precision of 87%, recall of 87%, and an f1 score of 87%.
- The model’s performance affected by class imbalance, so it tended to be better at predicting the majority label (normal) than the minority label (depression).

