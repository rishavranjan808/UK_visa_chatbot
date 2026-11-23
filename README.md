# 🇬🇧 VisaGuide AI — UK Immigration Assistant

VisaGuide AI is a Streamlit web application that answers questions about UK visas, immigration routes, and eligibility rules grounded in official **GOV.UK** guidance via **Groq**.

## Features

- **Official GOV.UK Retrieval:** Queries the GOV.UK search API (`gov.uk/api/search.json`) and extracts text from official `gov.uk` / `www.gov.uk` pages.
- **Grounded Answers & Citations:** Uses Groq (`openai/gpt-oss-120b`) with guardrails to avoid guessing rules, cite sources (`[1]`, `[2]`, etc.), and attach direct GOV.UK links below responses.
- **Broad Immigration Coverage:** Supports questions across Graduate, Skilled Worker, Health and Care Worker, Student, Family/Spouse, Standard Visitor, Innovator Founder, Global Talent, Scale-up Worker, High Potential Individual routes, sponsor licences, self-sponsorship context, ILR, and British citizenship.
- **Interactive Chat UI:** Built with Streamlit, including multi-turn conversation context and a sidebar topic reference + conversation reset button.

## Project Structure

```text
uk-visa-chatbot/
├── app.py              # Main Streamlit application (replace with your script filename)
├── requirements.txt    # Python dependencies
├── .env                # Local environment variables (not committed to Git)
└── README.md
```

## Setup & Installation

1. **Clone the repository**
   ```bash
   git clone [https://github.com/rishavranjan808/uk-visa-chatbot.git](https://github.com/rishavranjan808/uk-visa-chatbot.git)
   cd uk-visa-chatbot
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv .venv
   # Windows (PowerShell):
   .venv\Scripts\Activate.ps1
   # macOS / Linux:
   source .venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   Create a `.env` file in the project root and add your Groq API key:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

5. **Run the app**
   ```bash
   streamlit run app.py
   ```
   *(Replace `app.py` with the actual name of your Python file.)*

## Disclaimer

This tool is for general informational purposes only and does **not** constitute regulated legal or immigration advice. Always verify current rules directly on [GOV.UK](https://www.gov.uk/) and consult an appropriately regulated immigration adviser for personal cases.
