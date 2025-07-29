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

# Project Highlights
1. 🎵 Audio-Based Recommendation System
Build a content-based recommender that suggests songs based on user-preferred audio traits (e.g. high energy, fast tempo, happy mood).

Input: User-defined feature preferences

Output: Top 5 most similar tracks using KNN + cosine similarity

Example: Recommend danceable and energetic pop songs with fast beats

2. 🧠 Genre Classification Using Audio Features
Use a Random Forest Classifier to predict a song’s genre based on its audio signature.

Trained on 30+ genres

Evaluated with precision, recall, F1-score

Identified well-performing classes (e.g., comedy, drum-and-bass) and poorly performing ones (e.g., anime, dub) due to feature overlap

3. 🚀 Emerging Track & Artist Discovery
Identify tracks and artists that are not yet mainstream but exhibit high potential based on audio characteristics.

Focus on tracks with mid-range popularity (40–70)

Construct an emerging score:

ini
Copy
emerging_score = danceability + energy + valence + tempo_norm - loudness_penalty
Rank top tracks and artists to uncover future hits

4. 📈 Popularity Drivers by Genre
Answer: What drives track popularity within each genre?

Trained separate linear regression models per genre

Quantified how features like valence, tempo, or acousticness influence popularity in each genre

Insight:

valence strongly boosts popularity in pop and dance pop

In metal, lower valence (darker tone) correlates with higher popularity

