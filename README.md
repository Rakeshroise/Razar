# Razar
An AI-powered university campus helpdesk that answers student questions about academics, exams, placements, hostel, library, and administration using supplied campus information.
# AI Campus Helpdesk

A student helpdesk prototype for the TECHNOPIA 2.0 challenge. Students can ask questions about academics, attendance, examinations, placements, the library, hostel, administration, and events.

The app uses the supplied sample campus information. It should say when an answer isn’t available instead of inventing details.

## Requirements

- Node.js 18 or newer
- An OpenAI API key for AI-generated answers

## Run locally

Open a terminal in this project folder. In PowerShell, set your API key and start the server:

```powershell
$env:OPENAI_API_KEY="your-api-key"
node server.js
```

Then open [http://localhost:3000](http://localhost:3000).

Keep the terminal running while you use the app. If you open a new terminal, set the API key again.

## AI integration

The Node.js backend sends the student’s question and the sample campus information to the OpenAI Responses API. The API key is kept on the server and should never be added to the frontend or committed to GitHub.

If no API key is set, or the AI request fails, the backend uses a basic keyword-based fallback with the supplied campus facts.

The default model is `gpt-4.1-mini`. You can change it by setting the `OPENAI_MODEL` environment variable to a model available to your API account.

## Project files

- `index.html` — chat interface and page styling
- `server.js` — Node.js server and AI API connection
- `package.json` — project settings and start command
- `.gitignore` — prevents local environment files from being uploaded

This prototype does not require a database, student login, or a complete university management system.
