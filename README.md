# Spotify Song Recommendation and Visualization

This project integrates with the Spotify API to provide song recommendations based on seed tracks. The recommended songs are visualized using a scatter plot that includes the 30-second playtime feature, and album images can be saved and retrieved locally.

## Features

- **Spotify API Integration:** 
  - Retrieve song recommendations based on seed tracks.
  - Authenticate using Spotify's client credentials.

- **Visualization:** 
  - Display recommended songs in a scatter plot where:
    - The x-axis represents song names.
    - The y-axis represents song duration in seconds.
    - The size of each point represents the song's popularity.
    - Colors indicate whether a song is explicit or not.
  - Visualize the 30-second playtime of songs.

- **Album Image Handling:**
  - Save album images for the recommended songs locally.
  - Retrieve and display album images.

## Installation

1. Clone this repository:
   ```bash
   https://github.com/123kiran17/music_analytics_app.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Spotify_Streamlit_Project/Spotify-Streamlit_App
   ```
3. Install the required dependencies:
   ```python
   pip install spotipy pandas streamlit matplotlib
   ```
## Usage

### Spotify Authentication
To access the Spotify API, you'll need to authenticate using your Spotify Developer credentials.

**Get the Access Token:**
Use the `get_token(clientId, clientSecret)` function, where `clientId` and `clientSecret` are your Spotify API credentials.

### Get Track Recommendations
Use the `get_track_recommendations(seed_tracks, token)` function to get track recommendations.

- `seed_tracks`: A list of seed track IDs to base the recommendations on.
- `token`: The access token obtained from the Spotify API.

### Visualize Song Recommendations
The `song_recommendation_viz(reco_df)` function visualizes the song recommendations in a scatter plot, including:

- **Song Duration:** Represented on the y-axis in seconds.
- **Popularity:** Indicated by the size of each point.
- **30-Second Playtime:** Displayed in the plot to show the relative length of the song's playtime.
- **Explicit Content:** Different colors are used to indicate whether a song is explicit or not.

### Save and Retrieve Album Images
Use the `save_album_image(img_url, track_id)` function to save album images locally.

Use the `get_album_image(track_id)` function to retrieve and display the album image.

### Streamlit Integration
The code is also integrated with Streamlit, allowing you to build an interactive web application.

## Running the Application

To run the Streamlit application, use the following command:

```bash
streamlit run app.py
```

## Dependencies

To install the required dependencies, make sure you have the following packages:

- `requests`
- `base64`
- `seaborn`
- `numpy`
- `matplotlib`
- `streamlit`
- `spotipy`
- `PIL` (Python Imaging Library)

## Acknowledgements

- **Spotify API**: For providing access to music data.
- **Matplotlib and Seaborn**: For visualization tools.
- **Streamlit**: For building the web app interface.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

For more details, please refer to the documentation and the project repository.
