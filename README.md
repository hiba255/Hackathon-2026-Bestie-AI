# Bestie Tunisia

Bestie Tunisia is a wellness-focused web application designed to support students, young graduates, and women in transition into the job market in their daily lives. It combines mood tracking, stress management, self-care routines, academic planning, and AI-powered support in a simple, warm, and private environment.

## Overview

Bestie helps users to:

- identify their emotional state and energy level;
- receive personalized guidance based on their current context;
- organize their schedule, study tasks, and rest moments;
- build healthy daily habits;
- keep a discreet record of their cycle without turning it into a diagnosis;
- chat with a supportive wellbeing assistant in French.

The solution is designed as a lightweight, useful, accessible, and privacy-conscious digital companion.

## Key Features

### 1. Mood and emotional tracking
- daily mood selection;
- stress and energy assessment;
- contextual suggestions based on the selected need: calm, study, affirmation, career, or rest.

### 2. Supportive AI assistant
- secure Express backend;
- calls to a local Ollama model to generate recommendations;
- structured responses and safety validations to reduce harmful or inappropriate guidance;
- free-form chat with a wellbeing support assistant.

### 3. Planning and time management
- personal calendar;
- academic task and rest scheduling;
- emphasis on today’s priorities and upcoming commitments.

### 4. Me Time and habit tracking
- scheduling of rest and self-care moments;
- tracking of simple daily habits;
- visual insights into weekly trends and patterns.

### 5. Optional cycle tracking
- enable or disable tracking at any time;
- log periods and symptoms;
- estimate upcoming cycle dates with a clear reminder that this is not medical advice.

### 6. Privacy and confidentiality
- data is stored locally in the browser;
- free-text entries are only sent to the AI when the user explicitly opts in;
- no unnecessary data is saved on the server.

## Tech Stack

- Frontend: React + Vite
- Backend: Express.js
- AI: Ollama (configurable via environment variables)
- Storage: browser localStorage
- Language: JavaScript / JSX

## Project Structure

```text
bestie-tunisia/
├── src/
│   ├── components.jsx
│   ├── App.jsx
│   ├── main.jsx
│   ├── lib/
│   ├── pages/
│   └── styles.css
├── server/
│   └── index.js
├── dist/
├── .env.example
├── .env
├── index.html
├── package.json
├── vite.config.js
├── README.md
└── package-lock.json
```

## Prerequisites

Before running the project, ensure you have:

- Node.js 18 or later
- npm
- Ollama installed locally
- a compatible model downloaded, for example:

```bash
ollama pull gemma3:4b
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/hiba255/Hackathon-2026-Bestie-AI.git
cd bestie-tunisia
```

2. Install dependencies:

```bash
npm install
```

3. Create the environment file from the example:

```bash
# macOS / Linux
cp .env.example .env

# Windows PowerShell
Copy-Item .env.example .env
```

4. Review and adjust the variables if needed:

```env
LLM_PROVIDER=ollama
LLM_BASE_URL=http://localhost:11434
LLM_MODEL=gemma3:4b
PORT=3001
```

> The `.env` file should not be shared publicly. It contains local runtime configuration.

## Running the Project

### Development mode

```bash
npm run dev
```

This starts both:
- the Express backend server;
- the Vite React frontend.

### Production build

```bash
npm run build
```

### Run the built application

```bash
npm start
```

## Available Scripts

In `package.json`:

- `npm run dev` — starts the app in development mode
- `npm run client` — launches only the Vite frontend
- `npm run server` — launches only the backend server
- `npm run build` — builds the app for production
- `npm start` — builds and starts the production server

## Usage

Once the project is running, open the app in your browser at the local port configured by the project, typically:

- http://localhost:5173 (frontend Vite)
- http://localhost:3001 (backend API)

The app allows users to:

- track their daily emotions;
- request personalized suggestions;
- organize tasks and rest time;
- chat with Bestie.

## Safety and Emergency Support

A safety layer has been added on the backend to:

- validate user input;
- filter sensitive content;
- prevent inappropriate responses in distress situations;
- encourage contact with a trusted person or emergency support when relevant.

Bestie is not a psychologist or doctor. It provides supportive guidance, not a diagnosis.

## Contributing

Contributions are welcome. Before proposing a change:

1. create a dedicated branch;
2. make a focused modification;
3. verify the project still runs correctly;
4. open a pull request with a clear description.

## License

This project is provided for demonstration and collaborative development purposes. Please verify your organization’s rules before deploying or sharing it publicly.

## Contact

Project developed as part of the 2026 Bestie AI Hackathon.


