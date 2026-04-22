# Himanshu Prajapat Portfolio

A modern dark portfolio for Himanshu Prajapat with glassmorphism UI, animated sections, and a Claude-powered portfolio chatbot.

## Tech Stack

- Frontend: React, Vite, Tailwind CSS, AOS, tsParticles
- Backend: Node.js, Express
- AI: Anthropic Claude Messages API

## Setup

1. Install dependencies:

   ```bash
   npm run install:all
   ```

2. Add your Anthropic key in `.env`:

   ```bash
   ANTHROPIC_API_KEY=your_real_key
   ANTHROPIC_MODEL=claude-sonnet-4-5
   PORT=8787
   INQUIRY_TO_EMAIL=hp81790@gmail.com
   SMTP_HOST=smtp.gmail.com
   SMTP_PORT=587
   SMTP_SECURE=false
   SMTP_USER=your_email@gmail.com
   SMTP_PASS=your_gmail_app_password
   ```

3. Run frontend and backend together:

   ```bash
   npm run dev
   ```

4. Open the frontend URL printed by Vite, usually `http://localhost:5173`.

## Production Build

```bash
npm run build
npm start
```

The backend serves API routes from `/api/*`. In production, serve `frontend/dist` with your preferred static host and keep the backend API deployed separately, or configure your host to proxy `/api` to the Express server.

## Notes

- The Claude API key is read only on the backend and is never exposed to the browser.
- Himanshu's resume is served from `frontend/public/himanshu-resume.pdf`.
- Himanshu's profile photo is served from `frontend/public/himanshu.png`.
- Contact email is set to `hp81790@gmail.com`.
- The inquiry form sends mail through SMTP. For Gmail, use a Google App Password in `SMTP_PASS`.
