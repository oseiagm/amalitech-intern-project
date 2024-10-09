# Skin Condition Analyzer

An AI-powered dermatological screening tool designed to improve access to skin health diagnostics in Ghana and other regions with limited dermatological care resources.

## 🌍 Background

In Ghana, there is approximately 1 dermatologist per 1.4 million people, with only 23 dermatologists serving a population of over 32 million. This severe shortage of specialized healthcare providers, particularly in rural areas, creates significant barriers to accessing dermatological care. Our project aims to bridge this healthcare gap using artificial intelligence and computer vision technologies.

## 🔍 Project Overview

This application serves as a preliminary screening tool for skin conditions, leveraging the Llama 3.2 vision model through OpenRouter API to analyze uploaded images and provide:
- Potential condition descriptions
- Common treatment suggestions
- Voice-enabled analysis results (TTS version)

### Key Features

- 📸 Image upload and analysis
- 📝 Detailed condition descriptions
- 💊 Treatment recommendations
- 🔊 Text-to-Speech capability (TTS version)
- 📊 Analysis history tracking
- 🌐 User-friendly Streamlit interface

  
### Prerequisites

- Python 3.8+
- OpenRouter API key
- Required Python packages (see requirements below)

## ⚙️ Installation

1. Clone the repository:
```bash
git clone https://github.com/oseiagm/derma-assist.git
cd derma-assist
```

2. Create and activate a virtual environment (recommended):
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

3. Install required dependencies:
```bash
pip install streamlit requests Pillow gTTS
```


## 🔑 Configuration

1. Create a `.streamlit` directory in your project root:
```bash
mkdir .streamlit
```

2. Create a `secrets.toml` file inside the `.streamlit` directory:
```bash
touch .streamlit/secrets.toml
```

3. Add your OpenRouter API key to `secrets.toml`:
```toml
OPENROUTER_API_KEY = "your_api_key_here"
```

## 🚀 Running the Application

Run the standard version:
```bash
streamlit run skin.py
```
Run the TTS-enabled version
```bash
streamlit run skintts.py
```

Open your web browser and navigate to the URL shown in the terminal (typically `http://localhost:8501`)

## 💡 Usage

1. Upload an image of the skin condition using the file uploader
2. Click the "Analyze Image" button
3. View the analysis results in the right column
4. Previous analyses are stored and can be viewed in the "Previous Analyses" section

## ⚠️ Disclaimer

This application is for educational purposes only and should not replace professional medical advice. Always consult with a healthcare provider for proper diagnosis and treatment of skin conditions.

## 🔒 Security Notes

- Never commit your `secrets.toml` file to version control
- Add `.streamlit/secrets.toml` to your `.gitignore` file
- Keep your API keys confidential
