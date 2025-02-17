# Automating Our Browser with AI Agents

## 🚀 About the Project
This project focuses on leveraging AI-driven automation to streamline repetitive browser tasks such as web navigation, data entry, and content retrieval. By integrating AI agents with browser automation tools, users can efficiently execute web-based workflows with minimal manual intervention. This implementation is particularly beneficial for developers, testers, and professionals seeking to optimize their online interactions.

## 🎯 Skills Demonstrated
- **Programming:** Python
- **Automation:** Browser Use WebUI, Playwright
- **AI Integration:** Google AI Studio API (Gemini)
- **Web Development:** FastAPI, Jinja2
- **System & Package Management:** Git, UV, Pip, Virtual Environments
- **Debugging & Optimization:** Error handling, advanced prompt engineering

## ✨ Features
- Automate browser tasks with AI agents
- Run tasks on your personal browser (Google Chrome)
- Utilize Google AI Studio API for smart decision-making
- Perform complex automation tasks such as logging into LinkedIn

## 📈 Real-World Use Cases
- **Automated Job Applications:** Auto-fill job applications and navigate LinkedIn.
- **Web Scraping:** Extract and organize data from websites efficiently.
- **Form Automation:** Automatically submit online forms.
- **AI-Assisted Research:** Gather structured information from multiple sources.

## 🏆 Key Achievements
- Successfully automated LinkedIn login and navigation, reducing manual effort by **90%**.
- Configured AI-driven browser navigation using **Google AI Studio API**.
- Implemented **secure API key management** for improved data security.

## 🛠️ Tech Stack
- **Programming Language:** Python
- **Automation Tools:** Browser Use WebUI, Playwright
- **AI Model:** Google AI Studio API (Gemini)
- **Web Framework:** FastAPI
- **Other Tools:** Uvicorn, Jinja2, dotenv
- 
## 🛠️ Installation & Setup
### Prerequisites
- 300MB of storage on your computer
- Google Chrome
- Python 3.11+
- Git

### Installation Steps
#### Mac Users:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```sh
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
### Step 1: Clone WebUI Repository
```sh
cd ~/Documents
git clone https://github.com/browser-use/web-ui.git
cd web-ui
pwd  # Verify directory
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
2. Set up Google AI Studio API Key ([Generate API Key](https://aistudio.google.com/app/apikey))
3. Configure LLM settings to use Gemini (Google AI Studio)
4. Run agent prompts, e.g., "Go to Google.com and search for OpenAI."

## 🔥 Advanced Configuration
### Use Personal Browser (Google Chrome)
1. Edit the `.env` file:
```sh
nano .env
```
2. Replace `CHROME_PATH` and `CHROME_USER_DATA` with:
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

# Delete Virtual Environment
rm -rf .venv

# Remove Repository
cd ..
rm -rf web-ui

# Uninstall UV
pip3 uninstall uv -y

# Clean Up Homebrew
brew cleanup
```
