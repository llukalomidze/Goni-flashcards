# Goni Backend

The Goni backend accepts study text or a PDF and uses Google Gemini to generate
flashcards for the web app.

## Run locally

1. Install dependencies:

   ```sh
   npm install
   ```

2. Create a `.env` file in this directory and provide your Gemini API key:

   ```env
   GEMINI_API_KEY=your_api_key
   PORT=5000
   ```

   `PORT` is optional and defaults to `5000`.

3. Start the server:

   ```sh
   npm start
   ```

## API

`POST /api/generate` accepts either:

- JSON with a `text` string; or
- `multipart/form-data` with a PDF in the `file` field.

On success, the response contains a `flashcards` array with question (`front`)
and answer (`back`) fields. Errors are returned as JSON with an `error` field.
