# Windows Instructions

General instructions for setting up and running the scripts on Windows

## Setup

In Windows PowerShell:

1. Clone the repository:

   ```
   git clone https://github.com/MikeBirdTech/automations.git; cd automations
   ```

2. Create and activate a virtual environment:

   ```
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

3. Install the required packages:

   ```
   pip install -r requirements.txt
   ```

4. Install FFmpeg:

   - Download the FFmpeg build from [ffmpeg.org](https://ffmpeg.org/download.html)
   - Extract the contents to a folder (e.g., `C:\ffmpeg`)
   - Add the `bin` folder to your system PATH:
     - Right-click on 'This PC' or 'My Computer' and select 'Properties'
     - Click on 'Advanced system settings'
     - Click on 'Environment Variables'
     - Under 'System variables', find and select 'Path', then click 'Edit'
     - Click 'New' and add the path to the FFmpeg bin folder (e.g., `C:\ffmpeg\bin`)
     - Click 'OK' to close all dialogs

   Verify the installation by opening a new PowerShell window and running:

   ```
   ffmpeg -version
   ```

5. Set up environment variables:

   ```
   $Env:EXA_API_KEY="<your exa api key>"
   $Env:GROQ_API_KEY="<your groq api key>"
   $Env:ANTHROPIC_API_KEY="<your anthropic api key>"
   $Env:FAST_OLLAMA_MODEL="<your preferred fast Ollama model>"
   $Env:OLLAMA_MODEL="<your preferred Ollama model, default is llama3.1>"
   ```

   Note: To make these environment variables persistent, you may want to add them to your Windows environment variables through the System Properties dialog.

## Running Scripts

Navigate to the specific script directory and refer to its README for detailed usage instructions.

For example:

- AI Commit: `cd ai_commit; python aicommit.py`
- AI CLI: `cd ai_cli; python ai_cli.py`
- Research Assistant: `cd research_assistant; python research_assistant.py`

Refer to each script's README for specific options and usage details.
