# Music Playlist Clustering using KMeans and Spotify API


Welcome to my Music Playlist Clustering project! This project delves into the exciting world of music data analysis, employing advanced techniques to create personalized playlists from a vast collection of over 5000 songs. By utilizing KMeans clustering and leveraging audio features, i discovered the underlying patterns that define the music and curated 8 distinct playlists that cater to diverse musical preferences.

## Project Highlights

- **Dataset Exploration:** My journey began with a comprehensive music dataset encompassing various audio features like danceability, loudness, tempo, instrumentalness, mode, acousticness, duration_ms, energy, liveness, speechiness, time_signature, valence and key. To streamline our analysis, we selected the top 5 features that exhibited significant variance, ensuring that we capture the essence of each song.
  > acousticness: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.
  > danceability: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.
  > duration_ms: The duration of the track in milliseconds.
  > energy: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.
  > instrumentalness: Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.
  > key: The key the track is in. Integers map to pitches using standard Pitch Class notation . E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.
  > liveness: Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.
  > loudness: The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db.
  > mode: Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.
  > speechiness: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.
  > tempo: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.
  > time_signature: An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).
  > valence: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

- **KMeans Clustering:** Leveraging the power of unsupervised learning, i applied KMeans clustering to group songs with similar characteristics. i fine-tuned the number of clusters using both the elbow method and silhouette analysis. Ultimately, settling on 8 clusters allowed me to strike a balance between granularity and cohesion.

- **Spotify Integration:** Seamlessly integrating with the Spotify Developer API, i took the analysis a step further by translating clusters into playlists. The API facilitated the creation of 8 playlists, each curated to encapsulate the distinct musical traits of its corresponding cluster.

- **Genre Exploration:** While the genre of each song wasn't readily available, the Spotify API offered insight into the genre of the song's artist. By utilizing this information, i gained a deeper understanding of the musical landscape within each cluster.

- **Word Cloud Visualization:** To shed light on the distribution of genres across clusters, i employed a creative visualization approach: word clouds. These captivating visual representations provided a quick glance at the predominant genres that defined each playlist.

## Getting Started

1. **Dataset:** Music dataset is available. Dive into the audio features that served as the foundation for the clustering process.

2. **Code Exploration:** The Python code, which encompasses feature selection, KMeans clustering, playlist creation, genre retrieval, and word cloud generation, can be found in the python file. Feel free to explore, adapt, and build upon our methods.

3. **Results:** Discover the outcome of my clustering endeavor. Detailed insights, cluster compositions, playlist links, and genre distributions await.

4. **Visualization:** Uncover the genre distribution with innovative word cloud visualizations.

## Acknowledgments

My appreciation goes to the Spotify Developer API for enabling seamless integration of my clustering results with the Spotify platform. Additionally, the open-source community's contributions, including libraries such as `spotipy` and `scikit-learn`, were instrumental in the realization of this project's success.
