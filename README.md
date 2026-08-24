# Chibi AI Character (Local Version)

This project contains a fully local, 3D talking AI character. It runs 100% on your own hardware without needing any paid APIs or internet connections for the AI brain. 

## Project Location
- **Main Folder:** D:\projects\stu\
- **Application File:** chibi_character_talking.html
- **Source Zip (Backup):** chibi_source.zip

---

## How to Run the App Manually

Because this app uses an advanced local AI and a 3D engine, you must start two background processes before opening the app. 

### Step 1: Start the AI Engine (Ollama)
We have configured Ollama to run locally off your D:\ drive so it doesn't take up space on your C:\ drive.

1. Open a new **PowerShell** window.
2. Copy and paste the following command, then press **Enter**:
   $env:OLLAMA_MODELS="D:\OllamaModels"; $env:CUDA_VISIBLE_DEVICES=""; D:\Ollama\ollama.exe serve
3. **Leave this PowerShell window open** in the background. If you close it, the AI will stop thinking and the character won't be able to talk.

### Step 2: Start the Web Server
Web browsers block 3D assets (like the character model) from loading if you just double-click the HTML file. You must run a local web server to display it.

1. Open a **second PowerShell** window.
2. Navigate to your project folder by typing:
   cd D:\projects\stu\
3. Start the server by typing:
   python -m http.server 8000
4. **Leave this window open** as well.

### Step 3: Open the App in your Browser
Now that both the AI and the Web Server are running, open your favorite web browser (like Chrome or Edge) and navigate to:

👉 http://localhost:8000/chibi_character_talking.html

*(Note: If the layout ever looks broken, you can add ?v=final to the end of the URL to bypass your browser's cache, like this: http://localhost:8000/chibi_character_talking.html?v=final)*
