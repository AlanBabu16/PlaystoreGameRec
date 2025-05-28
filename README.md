# PlaystoreGameRec

**Comparison of Sentiment-Driven Deep Learning Models for Play-Store Game Recommendations**
---

## 📖 Overview  
A hybrid recommender that leverages both star‐ratings and VADER sentiment scores from Google Play Store game reviews.  
We implement and compare four deep‐learning architectures—  
1. **GloVe+LSTM+Attention**  
2. **DistilBERT**  
3. **Hybrid GRU–CNN**  
4. **DistilGPT2**  
…in terms of  
- **Prediction error:** MSE, MAE  
- **Ranking quality:** Recall@K, NDCG@K

Data Source: Kaggle “Play-Store Game Reviews” dataset

Raw format: nested JSON

Sampling: we extract a random 100 000‐row subset 

Preprocessing steps:

lowercase, punctuation & stop‐word removal

emoji & URL/mention stripping

VADER sentiment → compound score mapped to [1–5]

Best prediction (MSE/MAE): Hybrid GRU–CNN (0.0391 / 0.1239)

Best ranking (Recall@10, NDCG@10): LSTM+Attention (0.8440, 0.8440)
