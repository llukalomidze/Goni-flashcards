# Goni

Goni is a flashcard study app. Paste study material or upload a digital PDF to
generate flashcards, then flip through the questions and answers.

## Run locally

1. Start the backend by following the setup instructions in
   [goni-backend/README.md](../goni-backend/README.md).
2. In this directory, install dependencies and start the Vite development
   server:

   ```sh
   npm install
   npm run dev
   ```

The frontend sends generation requests to `http://localhost:5000` by default.
To use a different backend URL, set `VITE_API_URL` in a local `.env` file in
this directory.

## Available scripts

- `npm run dev` starts the development server.
- `npm run build` creates a production build in `dist/`.
- `npm run preview` serves the production build locally.
- `npm run lint` runs ESLint.
