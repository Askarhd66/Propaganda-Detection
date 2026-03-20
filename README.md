<h1>🧠 Propaganda Detection Using Classical ML, LSTMs & BERT</h1>

<h2>🎯 Project Overview</h2>
This project focuses on detecting propaganda in political text using both classical and modern NLP methods.  
It covers two tasks:
<ul>
  <li><b>Task 1:</b> Given a known propaganda span → classify the propaganda technique.</li>
  <li><b>Task 2:</b> From raw text → detect the span + classify the technique.</li>
</ul>

The project compares:
<ul>
  <li>TF‑IDF + Logistic Regression</li>
  <li>BiLSTM with trainable embeddings</li>
  <li>Fine‑tuned BERT (sequence classification)</li>
  <li>BERT BIO‑tagging (token classification)</li>
  <li>Heuristic span detection + Logistic Regression</li>
  <li>QA‑style BERT span prediction + BERT classifier</li>
</ul>

<h2>🛠 Tools & Libraries</h2>

- Python  
- scikit‑learn  
- TensorFlow / Keras  
- PyTorch  
- HuggingFace Transformers  
- Pandas, NumPy  

<h2>📊 Dataset</h2>

Propaganda Techniques Corpus (PTC):  
- 2,560 training sentences  
- 640 validation sentences  
- 9 propaganda techniques + “not propaganda”  
- <code>&lt;BOS&gt;</code> and <code>&lt;EOS&gt;</code> tags mark the gold span  

<h2>🏆 Key Results</h2>
<b>Task 1 - Technique Classification</b>
<ul>
  
  <li><b>Logistic Regression:</b> 57% accuracy, macro F1 = 0.41</li>
  <li><b>BiLSTM:</b> 55% accuracy, macro F1 = 0.35</li>
  <li><b>BERT:</b> <b>72% accuracy</b>, macro F1 = <b>0.59</b> (best)</li>
</ul>

<b>Task 2 - Span + Technique Detection</b>
<ul>
  <li><b>BIO‑tagging BERT:</b> 63% token accuracy, macro F1 = 0.18</li>
  <li><b>Heuristic + Logistic Regression:</b> fast baseline, moderate span overlap</li>
  <li><b>QA‑style BERT:</b> good span extraction, weaker full‑match accuracy</li>
</ul>

<h2>📌 Summary</h2>

- BERT significantly outperforms classical and LSTM models.  
- Span detection is harder than technique classification.  
- QA‑style BERT is promising but sensitive to alignment errors.  
- Logistic Regression remains a strong, interpretable baseline.  
