# AI Sports Technique Analysis (React + Django + LLM)

Full‑stack application to analyze canoe sprint videos, compute metrics, and generate coach‑style feedback using an LLM.

## Tech Stack

- Frontend
  - React 18 + Vite (React SWC plugin)
  - TypeScript
  - Tailwind CSS (+ tailwindcss-animate)
  - shadcn/ui (built on Radix UI)
  - React Router v6
  - TanStack React Query
  - Recharts (charts)
  - Lucide React (icons)
- Backend
  - Django 5 (ASGI)
  - Django Channels 4 + Daphne (WebSockets)
  - django-cors-headers
  - SQLite (default)
- Vision & Analytics
  - OpenCV
  - MediaPipe 0.10.14
  - NumPy, Pandas
  - Pillow, Matplotlib, Seaborn
- AI / External APIs
  - Hugging Face Inference API (model: google/flan-t5-base)
- Tooling
  - ESLint (typescript-eslint, react-refresh)
  - clsx, class-variance-authority
  - Vite alias @ → src/

---

## Requirements

- Node.js 18+ and npm
- Python 3.10.x (recommended: 3.10.8)
  - Important: Python 3.13.x is not compatible with MediaPipe; use 3.10.8 to avoid errors.
- pip and virtualenv (or python -m venv)

---

## Project Structure
backend/ # Django + Channels + analysis pipeline (OpenCV/MediaPipe) 
frontend/ # React (Vite, TS, Tailwind, shadcn/ui) 
## Quick Start

### 1) Backend (Django + Channels)

```bash
cd backend
pip install -r requirements.txt
# Run ASGI server via Daphne
python app.py
# Default: http://127.0.0.1:8000

### 2) Frontend (React + Vite)
npm install
npm run dev
# Default: http://localhost:8080
