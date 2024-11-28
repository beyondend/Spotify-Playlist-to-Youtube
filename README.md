# Spotify to YouTube Music

You can use the following tool to transfer your Spotify playlists to YouTube Music: [spotify_to_ytmusic](https://github.com/linsomniac/spotify_to_ytmusic?tab=readme-ov-file).

## Steps

1. **Download Miniforge Prompt**
   - Download it from [here](https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Windows-x86_64.exe).

2. **Open Miniforge Prompt**

3. **Create an Environment for Spotify to YouTube Music Transfer**
   - Type: 
     ```bash
     conda create --name spotify_to_youtube
     ```

4. **Activate the Environment**
   - Type: 
     ```bash
     conda activate spotify_to_youtube
     ```

5. **Install Python**
   - Type: 
     ```bash
     pip install python
     ```

6. **Install the Transfer Tool**
   - Type: 
     ```bash
     pip install spotify2ytmusic
     ```

7. **Generate Log-in Tokens for YouTube Music and Download Spotify Playlists**
   - Create a directory:
     - Type: 
       ```bash
       mkdir spotify_to_youtube
       ```
   - Go to that directory:
     - Type: 
       ```bash
       cd spotify_to_youtube
       ```

8. **Generate Token for YouTube Music**
   - Type: 
     ```bash
     ytmusicapi oauth
     ```
   - Follow the instructions on the pop-up.

9. **Download Playlist from Spotify**
   - Download the Python file for downloading playlists: [spotify-backup.py](https://raw.githubusercontent.com/caseychu/spotify-backup/master/spotify-backup.py).
   - Move the file to the `spotify_to_youtube` folder (this can be done manually).

10. **Download the Spotify Playlists and Liked Songs**
    - Type: 
      ```bash
      python spotify-backup.py playlists.json --dump=liked,playlists --format=json
      ```

11. **Like All the YouTube Music Songs that are from Your Spotify**
    - Type: 
      ```bash
      s2yt_load_liked
      ```

12. **That's
