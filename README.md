# subtitles

Generate JP and EN subtitles

[![Open All Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MisterX2000/subtitles/blob/main/subtitles.ipynb)

---

## How does this work?

1. **Extract vocals from input for better transcription**  
Using Mel-Band-Roformer:  
<https://github.com/KimberleyJensen/Mel-Band-Roformer-Vocal-Model>

1. **Generate Transcription**  
Using a variant of OpenAI Whisper:  
<https://github.com/Purfview/whisper-standalone-win>

1. **Translate to English**  
Using Google Gemini SRT Translator:  
<https://github.com/MaKTaiL/gemini-srt-translator>

## How to use the Colab file?

### 1. Choose an Input Method

#### Option A - Download via yt-dlp

![image](https://github.com/user-attachments/assets/81864f48-cdb8-4d7c-b364-85adec590304)

#### Option B - Google Drive

* Upload the video to Google Drive.
* Then specify the path to the file in Google Drive.
* Keep it simple. No spaces or special characters. No effort was made to accomodate those.
![image](https://github.com/user-attachments/assets/8ef1bb6e-c0d5-4404-8d88-ba39b1fc2c0a)

#### Option C - Local File

* Upload the video to the local Colab file system or mount the path to your local file system.
* Keep it simple. No spaces or special characters. No effort was made to accomodate those.
* Mount your local file system like so in the [Google Colab local instance](https://research.google.com/colaboratory/local-runtimes.html):
  
  ```sh
  docker run --gpus=all -p 127.0.0.1:9000:8080 -v "F:\Path\to\MyDrive:/content/drive/Local" us-docker.pkg.dev/colab-images/public/runtime
  ```

### 2. Choose an Output folder in your Google Drive or Local folder

![image](https://github.com/user-attachments/assets/4f9889e7-a378-4355-934c-87de38873fde)

### 3. Input Google Gemini API key(s)

You need at least 1 key.
If desired, you can specify 2 keys from different accounts to try to get around Google free API limits.

#### Option A - Just fill in the keys

![image](https://github.com/user-attachments/assets/150dff67-4f90-4bea-921d-93616368a9a8)

#### Option B - Use Colab's Secret (Better)

Put your keys in Colab's Secret by clicking the key icon.
Make sure that Notebook access is enabled.
Key names are `GEMINI_API_KEY_1` and `GEMINI_API_KEY_2`.

![image](https://github.com/user-attachments/assets/b7b428b4-a65e-4c52-8ca1-12e33cc2901a)

### 4. Specify the runtime settings

#### A. Make sure that you enable GPU

![image](https://github.com/user-attachments/assets/839d8b65-891d-49d7-9f80-0c23d5a7bb1b)
![image](https://github.com/user-attachments/assets/45cd6710-b621-4d00-9732-0b651517823d)

#### B. Connect to the local runtime

1. In Colab, click the "Connect" button and select "Connect to local runtime...".
2. Enter the URL from the local console in the dialog that appears and click the "Connect" button.
3. After this, you should now be connected to your local runtime.

### 5. Run

![image](https://github.com/user-attachments/assets/6c07802b-2219-436e-b7d9-c33407e528d0)