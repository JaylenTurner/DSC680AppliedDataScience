# Readme for project one

## 📌 Project Overview

With thousands of games released every year, finding titles that match a player’s interests can be overwhelming. This project presents a **game recommendation system** that combines:

- **Content-Based Filtering** to suggest similar games based on game metadata.
- **K-Means Clustering** to categorize games into meaningful groups for discovery.

The hybrid system enhances both personalization and exploration, providing a scalable solution for digital gaming platforms like Steam or Xbox.

---

## 📂 Dataset

- **Source:** [RAWG Video Game Dataset – Kaggle](https://www.kaggle.com/datasets/jummyegg/rawg-game-dataset)
- **Size:** 474,000+ video games
- **Key Features:**
  - Game Title
  - Genre(s)
  - Developer
  - ESRB Rating
  - Average Playtime
  - User Rating
  - Release Year

---

## 🧹 Data Preprocessing

- Missing value handling
- One-hot encoding of top genres and developers (others grouped as "Other")
- Normalization of numeric features
- Multi-label fields simplified to avoid memory issues
- Dimensionality reduction using PCA for visualization

---

## 🔍 Techniques Used

### 1. Content-Based Filtering
- Uses **Nearest Neighbors** to find games similar to a selected title.
- Recommendations based on genre, developer, playtime, and rating.
- Example: Input = "The Witcher 3" → Output = Skyrim, GTA V, God of War, etc.

### 2. K-Means Clustering
- Optimal clusters determined using the **Elbow Method**.
- Identified 4 primary game clusters:
  - 🎨 Indies
  - 💥 Mainstream Action Core
  - 🧙 Hardcore Long-Play RPGs
  - 🕹️ Casual Midcore Mix
- **Classification model** trained to assign new games to clusters with near-perfect accuracy.

### 3. Hybrid System
- Allows combined queries like:
  - "Find me Witcher-like RPGs"
  - "Recommend games from the Casual Midcore Mix cluster"

---

## 🛠 Deployment & Integration

This system can be deployed into game platforms with:
- Real-time or batch processing
- UI for browsing clusters and recommendations
- API layer for integration with frontend applications

---

## 🔐 Ethical Considerations

- Avoid reinforcing bias toward only popular games
- Promote fair visibility of indie/niche titles
- Ensure transparency in how recommendations are made
- Address user privacy and compliance (GDPR/CCPA)

---

## 🚀 Future Improvements

- Add collaborative filtering using user interaction data
- Incorporate real-time feedback (clicks, ratings)
- Explore neural network models for deeper personalization
- Use cloud infrastructure for larger-scale processing

---

## 📚 References

- European Union. *General Data Protection Regulation (GDPR)* – [gdpr.eu](https://gdpr.eu/)  
- California Consumer Privacy Act (CCPA) – [oag.ca.gov/privacy/ccpa](https://oag.ca.gov/privacy/ccpa)  
- JummyEgg. *RAWG Game Dataset* – [Kaggle](https://www.kaggle.com/datasets/jummyegg/rawg-game-dataset)  
- Ricci, Rokach, Shapira. *Recommender Systems Handbook* – [Springer](https://doi.org/10.1007/978-1-4899-7637-6_1)

---

## ❓ Q&A Highlights

- ✅ *How many clusters?* → Chosen using Elbow Method (K=4)
- ✅ *Can it recommend unknown games?* → Yes, via clustering
- ✅ *Can it personalize to individuals?* → Future extension
- ✅ *What was hardest?* → Managing high-cardinality categorical features

---

## 🧠 Conclusion

This project successfully demonstrates the use of **machine learning and recommender systems** to build a smart, ethical, and scalable solution for helping players discover video games they'll enjoy. It forms a strong base for future work and real-world deployment.
