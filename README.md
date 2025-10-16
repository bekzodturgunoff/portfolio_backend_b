# Portfolio API (Back End)

Simple Express API used by the portfolio front end.

## Endpoints
- `GET /health` — health check
- `POST /api/contact` — send a message via email (uses SMTP)

## Setup
1. Copy `.env.example` to `.env` and fill credentials.
2. Install deps and start:

```
npm install
npm run dev
```

The API runs on http://localhost:5001 (as configured in `.env`).
Change `PORT` in `.env` if you need a different port.
