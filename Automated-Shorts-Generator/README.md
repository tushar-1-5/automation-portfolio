# Automated Shorts Generator (With Human-in-the-Loop)

## 📌 Overview
An automated video generation pipeline that creates vertical short-form content. This workflow handles everything from content sourcing to final rendering, utilizing command-line tools directly within the n8n container.

<img width="2195" height="842" alt="image" src="https://github.com/user-attachments/assets/2bcdee61-3056-4551-89b3-88733af487fc" />
Shorts Creation (Easy)
<img width="2251" height="807" alt="image" src="https://github.com/user-attachments/assets/9e0070b8-5420-450e-b7cd-120228079bf2" />
Shorts Creation (Complex)


## 🏗 Architecture & Logic
This workflow proves the ability to integrate external APIs with local machine processing:

* **Content Sourcing:** Uses the Pexels API to pull relevant portrait imagery based on randomized prompts, and fetches audio assets from Google Drive.
* **Human-in-the-Loop:** Integrates a Telegram Bot. Before the video is rendered, the bot messages the admin with the chosen image and AI-generated caption. The workflow pauses and waits for explicit human approval via Telegram buttons before proceeding.
* **Local Rendering:** Executes complex `ffmpeg` commands via the n8n Execute Command node to scale, crop, apply text overlays, fade audio/video, and render the final MP4.
* **Distribution:** Automatically uploads the final rendered `.mp4` directly to YouTube via their official API.

