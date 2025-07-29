# Spotify Music Trends &amp; Intelligence: Recommendation, Classification, and Emerging Artist Discovery
A data science project designed to uncover emerging artists, analyze popularity drivers across music genres, and build an audio-based recommendation system using a real-world Spotify tracks dataset.

This project simulates the responsibilities of a Content Analytics - Music Partnerships Data Scientist at Spotify, focusing on:

- Data-driven music discovery

- Predictive insights into artist and genre performance

- Strategic intelligence for partnerships and promotion
# Dataset Overview
The dataset includes Spotify tracks with audio features, genre labels, and popularity scores. [Data Source]

Columns include:

- track_name, main_artist, track_genre, popularity

- Audio features: danceability, energy, loudness, speechiness, acousticness, instrumentalness, liveness, valence, tempo，explicit, duration_ms, mode, etc.

<img width="1257" height="385" alt="image" src="https://github.com/user-attachments/assets/30e204b1-51fa-4964-8157-31b691ba7db9" />


**A. Popularity Distribution**

<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/fcf02767-24a8-4d54-8dad-c6d57e7d0b15" />

**B. Genre Distribution**

<img width="606" height="436" alt="image" src="https://github.com/user-attachments/assets/cc0f59ab-069d-4b11-ac67-0892d8760b26" />

**C. Correlation Heatmap**

<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/e8c62b33-602d-41c5-b51d-2164840c6b4d" />


# Project Highlights
## 1. Audio-Based Recommendation System
Build a **content-based recommender** that suggests songs based on user-preferred audio traits (e.g. high energy, fast tempo, happy mood).

- Input: User-defined feature preferences

- Output: Top 5 most similar tracks using KNN + cosine similarity

- Example: Recommend high energy, medium speechiness, low acousticness
<img width="896" height="218" alt="image" src="https://github.com/user-attachments/assets/64f68699-020a-4543-8f1d-63e44236738f" />

## 2. Genre Classification Using Audio Features
Use a **Random Forest Classifier** to predict a song’s genre based on its audio signature.

- Trained on 114 genres

- Evaluated with precision, recall, F1-score

- Identified well-performing classes (e.g., comedy, sleep, rock) and poorly performing ones (e.g., brazil, electronic) due to feature overlap
<img width="500" height="250" alt="image" src="https://github.com/user-attachments/assets/9c8b8104-6392-4506-815b-469d66b0eed1" />
<img width="500" height="250" alt="image" src="https://github.com/user-attachments/assets/f5c22bae-638f-4035-99b6-93c59bb7d493" />


## 3. Emerging Track & Artist Discovery
Identify tracks and artists that are **not yet mainstream** but exhibit **high potential** based on audio characteristics.

- Focus on tracks with mid-range popularity (40–70)

- Construct an emerging score:
`emerging_score = danceability + energy + valence + tempo_norm - loudness_penalty

- Rank top tracks and artists to uncover future hits`

**A. Top 10 tracks**

<img width="1471" height="488" alt="image" src="https://github.com/user-attachments/assets/0ebc9d49-732b-49b8-80e2-2fc18e3c2c8b" />

**B. Top 10 artist**

<img width="739" height="435" alt="image" src="https://github.com/user-attachments/assets/898716eb-062c-4851-9b45-e6464ea9597b" />

## 4. Popularity Drivers by Genre
Answer: What drives track popularity within each genre?

- Trained separate linear regression models per genre

- Quantified how features like valence, tempo, or acousticness influence popularity in each genre

- Insight:

  - valence strongly boosts popularity in pop and dance pop
    
    <img width="472" height="331" alt="image" src="https://github.com/user-attachments/assets/fa38e0d5-fde8-47a7-bffd-990369b02383" />
    
  - energy strongly boosts popularity in pop and classic
    
    <img width="472" height="331" alt="image" src="https://github.com/user-attachments/assets/3b70082c-d7eb-4731-93ea-7e50d95f3cc7" />

  - danceability strongly boosts popularity in house and funk

    <img width="472" height="331" alt="image" src="https://github.com/user-attachments/assets/5e4e7758-59dc-4014-a7e1-5f713ccff762" />

 # Strategic Takeaways
- Different genres have unique success drivers; promotional strategies should be tailored accordingly

- Emerging artist scoring can guide early-stage partnerships

- Audio-based recommendation helps enhance discovery and curation experience

# Tech Stack
- Python: pandas, sklearn, seaborn, matplotlib

- Models: KNN, Random Forest, Linear Regression

- Visualization: Seaborn, Matplotlib

# 🙋‍♀️ About Me
I’m a data analyst passionate about turning content signals into strategic music insights. This project was developed to simulate real-world challenges at Spotify’s Music Partnerships team and demonstrate my skills in data storytelling, modeling, and actionable insight generation.
