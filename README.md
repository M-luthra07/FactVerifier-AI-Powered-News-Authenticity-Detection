FactVerifier-AI-Powered-News-Authenticity-Detection
🌟 Overview
This project implements a hybrid deep learning model combining:

🤖 BERT embeddings

🔄 Bidirectional LSTM

🎯 SVM classifier

to detect fake news headlines with 91.5% accuracy!

🚀 Quick Start
⚙️ Prerequisites
Python 3.6+

TensorFlow 2.x

Transformers library

Scikit-learn

Pandas, NumPy
📊 Performance Metrics
🥇 Model Comparison
Model	Accuracy	Precision	Recall	F1-Score
LSTM	89.80%	73.93%	90.95%	81.56%
SVM	91.51%	83.45%	82.02%	82.73%
Hybrid	91.48%	83.57%	81.72%	82.64%
📈 Key Insights
🏆 SVM wins on overall accuracy (91.51%)

🔍 LSTM best at catching fakes (90.95% recall)

🤝 Hybrid balances precision & recall

🎯 All models beat random (50%) by wide margin

🧠 How It Works
🔧 Pipeline
📝 Text Cleaning:

Lowercase, remove URLs/special chars

Handle short texts specially

🤖 BERT Embeddings:

bert-base-uncased model

128 max tokens

🧠 LSTM Network:

Bidirectional (128 units)

Dropout (0.3)

64 ReLU units

🎯 SVM Classifier:

RBF kernel

Probability estimates

🤝 Hybrid Rules:

Short texts (<3 words) get special handling

Political names trigger "fake" classification

Others use SVM prediction

💾 About the Data
FakeNewsNet dataset:

23,196 news records

Balanced with augmented short texts

Sources: Politifact & GossipCop

🎭 Example Classifications
text
✅ Real: "Congress passes new education bill"
✅ Real: "NASA announces Mars mission details"
❌ Fake: "Celebrity spotted with alien" 
❌ Fake: "The Lion King" (too short + low confidence)
🛠️ Technical Highlights
⏱️ Trained for 10 epochs (early stopping at 7)

⚖️ Class weights for imbalance

🔄 Bidirectional LSTM captures context

🧩 Hybrid system handles edge cases

🚀 Future Roadmap
📰 Incorporate full article text

🏷️ Add metadata features

🌐 Multilingual support


📜 License
MIT License - see LICENSE for details.



☁️ Deploy as web service

🧑‍⚖️ Explainability features
