# Fit-Buddy-Ai-fitness-plan-generator-using-gemini-models 

FitBuddy is a FastAPI + Jinja2 + SQLite web application based on the supplied project documentation. It generates a structured 7-day workout plan, a nutrition/recovery tip, and an updated plan from user feedback.

## Project structure

```text
FitBuddy/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── config.py
│   ├── database.py
│   ├── schemas.py
│   ├── routes.py
│   └── ai/
│       ├── __init__.py
│       ├── gemini_client.py
│       ├── gemini_generator.py
│       ├── gemini_flash_generator.py
│       └── updated_plan.py
├── templates/
│   ├── index.html
│   ├── result.html
│   └── all_users.html
├── static/
│   └── style.css
├── data/
├── .env
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

## VS Code setup

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Open `http://127.0.0.1:8000` and API docs at `http://127.0.0.1:8000/docs`.

## Gemini

The included `.env` uses `DEMO_MODE=true`, so the application works without an API key. For live Gemini generation, put your key in `.env` and set `DEMO_MODE=false`.

Do not commit a real API key to Git.
