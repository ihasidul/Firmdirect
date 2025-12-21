# FirmDirect

## Overview

This is a platform where farmers can list their products for sale and general consumers can buy directly from the farmers. An additional feature will be that Other businesses and small stores can also post for their needs, and the platform will gather products from multiple farmers to serve the business's larger needs.


## How to run this project

### Backend

**Prerequisites:** Python and pip (virtual environment recommended).

**Run locally:**
```bash
cd backend
python -m venv .venv
source .venv/bin/activate  # on Linux/macOS
pip install -r requirements.txt

cp .env.example .env # Change the values on .env file 

# Apply database migrations (Alembic)
alembic upgrade head

# Start FastAPI (development server)
uvicorn main:app --reload --host 0.0.0.0 --port 8000
# API docs available at http://127.0.0.1:8000/docs
```

**Notes:**
- If you need to change configuration (e.g., SECRET_KEY or DB settings), add a `.env` file in `backend/` (the app uses `python-dotenv`).
- The backend defaults to a SQLite DB (`./database.db`) defined in `apps/common/database.py`. Replace with your production DB and update Alembic config as needed.


### Frontend 

**Prerequisites:** Node.js and npm installed (use your system package manager or nvm/yarn as preferred).

**Run locally:**
```bash
cd frontend
npm install
cp .env.example .env # Change the values on .env file 
npm run dev
# Vite dev server usually runs at http://localhost:5173
```

