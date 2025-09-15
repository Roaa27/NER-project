# 📝 Named Entity Recognition (NER) with spaCy

This project is part of my Elevvo Internship (NLP Track).  
The goal of this task is to perform Named Entity Recognition (NER) using the CoNLL-2003 dataset and spaCy’s pre-trained models.

---

## 📌 Project Steps

Step 1: Import Libraries  
I imported all the required libraries including spaCy for natural language processing, displacy for visualization, and seqeval for evaluation metrics.

Step 2: Upload Dataset  
I uploaded the CoNLL-2003 dataset files (train, test, validation) to Colab using files.upload(). These files contain tokenized sentences with their ground truth NER labels.

Step 3: Read and Prepare Data  
I defined a function to read the CoNLL data format.  
- It collects tokens and their corresponding labels for each sentence.  
- Finally, it returns a list of sentences (`train_sentences`) and their labels (`train_labels`).

Step 4: Load spaCy Model  
I loaded the spaCy English model en_core_web_sm, which comes with a pre-trained Named Entity Recognition component.

Step 5: Run NER on a Sample Sentence  
I tested the model on one example sentence from the training set.  
The model outputs named entities such as PERSON, ORG, and GPE, and I printed them out to verify the predictions.

Step 6: Visualization with displacy  
I used spaCy’s built-in displacy visualizer to highlight named entities in the text with different colors for better understanding.

Step 7: Evaluate the Model  
I compared spaCy’s predictions with the ground truth labels from the dataset using seqeval metrics.  
The evaluation provides Precision, Recall, and F1-score, along with a detailed classification report for each entity type.

---

## 📊 Results

- Entities Detected (example):
- Barack Obama - PERSON
United States - GPE
Hawaii - GPE
Harvard University - ORG
United Nations - ORG
Angela Merkel - PERSON
Berlin - GPE

- Evaluation Metrics (sample on subset):
- Precision: 0.75
Recall: 0.62
F1-score: 0.68

---

## 🛠️ Tools & Libraries Used

- Python  
- spaCy (`en_core_web_sm`)  
- displacy (NER visualization)  
- seqeval (NER evaluation metrics)  
- Google Colab  

---

pip install spacy seqeval
python -m spacy download en_core_web_sm
