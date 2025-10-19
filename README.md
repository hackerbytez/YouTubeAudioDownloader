# 🎧 YouTube Audio Downloader & WebM to MP3 Converter

This project provides two simple Python scripts for downloading YouTube audio and converting WebM audio files to MP3 format.  
It uses **pafy** and **moviepy** libraries to handle audio extraction and conversion efficiently.

---

## 📁 Project Files

| File Name | Description |
|------------|-------------|
| **YouTubeAudioDownloader.py** | Downloads the best quality audio stream from a YouTube video. |
| **WebmToMp3.py** | Converts a downloaded WebM audio file to MP3 format. |
| **requirements.txt** | Contains all required Python dependencies for the project. |

---

## ⚙️ Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/hackerbytez/YouTube-Audio-Downloader.git
   cd YouTube-Audio-Downloader
``

2. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## 📦 Requirements

Add the following to your `requirements.txt` file:

```txt
moviepy
pafy
youtube_dl
```

> ⚠️ If `pafy` or `youtube_dl` shows errors, install `yt-dlp` instead and link it with pafy:
>
> ```bash
> pip install yt-dlp
> ```

---

## ▶️ Usage

### 1. **Download YouTube Audio**

Edit the `YouTubeAudioDownloader.py` file and replace:

```python
url = "insert_url_to_youtube_video_here"
```

with your desired YouTube video URL.

Then run:

```bash
python YouTubeAudioDownloader.py
```

It will display video details and download the **best audio** stream available (usually in `.webm` format).

---

### 2. **Convert WebM to MP3**

Edit the `WebmToMp3.py` file and replace:

```python
clip = mp.AudioFileClip("insert_path_to_webm_file").subclip()
clip.write_audiofile("insert_path_to_save_mp3_file")
```

with your actual file paths. Example:

```python
clip = mp.AudioFileClip("downloads/audio.webm").subclip()
clip.write_audiofile("downloads/audio.mp3")
```

Run:

```bash
python WebmToMp3.py
```

The script will convert your WebM audio to an MP3 file.

---

## 🧠 How It Works

* **`pafy`** handles fetching video details and selecting the best available audio stream.
* **`moviepy`** reads the downloaded WebM file and re-encodes it into MP3 format.
* Both scripts can be easily integrated into larger automation or media projects.

---

## 🧰 Example Output

**YouTubeAudioDownloader.py**

```
_________VIDEO__DETAILS_________
Title: Peaceful Piano Music
Rating: 4.8
View Count: 1203845
Author: Relaxing Sounds
Length: 360 seconds
```

---

## 💡 Tips

* For better performance, keep both scripts in the same directory.
* You can automate the conversion step after download by combining both scripts.
* Make sure `ffmpeg` is installed and available in your system PATH (required by `moviepy`).

---

## 🧑‍💻 Author

**Uday Raut**
📧 [[your-email@example.com](mailto:your-email@example.com)]
🌐 [https://github.com/hackerbytez](https://github.com/hackerbytez)

---

## 📜 License

This project is licensed under the **MIT License** – feel free to use and modify it.

 
