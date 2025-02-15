# Automating Our Browser with AI Agents

## 🚀  Summary
This project utilizes AI agents to automate repetitive browser tasks such as web navigation, data entry, and content retrieval. By integrating AI-powered decision-making with browser automation tools, users can streamline workflows and reduce manual effort. This implementation is beneficial for developers, testers, and professionals aiming to optimize their online tasks.

## ✨ Features
- AI-driven browser automation
- Execution of tasks on personal browsers (Google Chrome)
- Integration with Google AI Studio API for intelligent decision-making
- Ability to perform complex actions such as logging into LinkedIn

## 🛠️ Tech Stack
- **Programming Language:** Python
- **Automation Tools:** Browser Use WebUI, Playwright
- **AI Model:** Google AI Studio API (Gemini)
- **Web Framework:** FastAPI
- **Other Tools:** Uvicorn, Jinja2, dotenv

## 📂 Folder Structure
```
project-root/
│── src/
│   ├── agents/
│   ├── config/
│   ├── utils/
│── tests/
│── public/
│── .env.example
│── package.json
│── README.md
```

## 🛠️ Installation & Setup
### Prerequisites
- 300MB of available storage
- Google Chrome installed
- Python 3.11+
- Git installed

### Installation Steps
#### Mac Users:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install python
brew install pip
brew install uv
brew install git
```

#### Verify Installation:
```sh
brew --version
python3 --version
pip3 --version
uv --version
git --version
```

## 🚀 Setting Up WebUI
### Step 1: Clone the WebUI Repository
```sh
cd ~/Documents
git clone https://github.com/browser-use/web-ui.git
cd web-ui
pwd  # Confirm correct directory
```

### Step 2: Set Up Python Environment
```sh
uv venv --python 3.11
source .venv/bin/activate
```

### Step 3: Install Dependencies
```sh
uv pip install -r requirements.txt
playwright install
```

### Step 4: Configure Environment
```sh
cp .env.example .env
```

### Step 5: Run WebUI
```sh
python webui.py --ip 127.0.0.1 --port 7788
```

## 🎯 Running Your AI Agent
1. Open [WebUI](http://127.0.0.1:7788)
2. Generate an API key from Google AI Studio ([Get API Key](https://aistudio.google.com/app/apikey))
3. Configure LLM settings to use Gemini (Google AI Studio)
4. Input agent prompts, e.g., "Go to Google.com and search for OpenAI."

## 🔥 Advanced Configuration
### Running on a Personal Browser (Google Chrome)
1. Open and edit the `.env` file:
```sh
nano .env
```
2. Update `CHROME_PATH` and `CHROME_USER_DATA`:
```sh
CHROME_PATH="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
CHROME_USER_DATA="/Users/yourusername/Library/Application Support/Google/Chrome"
```
3. Restart WebUI:
```sh
set -a
source .env
set +a
python webui.py --ip 127.0.0.1 --port 7788
```

## 🧪 Running Tests
```sh
pytest tests/
```

## 🔄 Uninstall & Cleanup
```sh
# Stop WebUI
deactivate

# Remove Virtual Environment
rm -rf .venv

# Delete Repository
cd ..
rm -rf web-ui

# Uninstall UV
pip3 uninstall uv -y

# Clean Up Homebrew
brew cleanup
```

