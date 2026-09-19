
# ✈️ AI TripMate

AI TripMate is an AI-powered travel planning and recommendation system designed to help users create personalized travel plans based on their destination, budget, trip duration, number of travellers, interests, and preferred transportation.

## 🚀 Project Overview

AI TripMate combines a modern web application with a Python-based recommendation system to provide travel recommendations that match the user's preferences and budget.

The system follows this architecture:

**React Frontend → Node.js/Express Backend → MySQL Database → Python Recommendation API**

## ✨ Features

* 🌍 Destination-based travel planning
* 💰 Budget-based recommendations
* 📅 Trip duration planning
* 👥 Number of travellers
* ❤️ Interest-based recommendations
* 🚌 Transportation preference
* 🤖 AI-based travel recommendation engine
* 🗄️ MySQL database for storing trip requests
* 🔗 REST API integration between frontend and backend

## 🛠️ Technologies Used

### Frontend

* React
* TypeScript
* Vite
* HTML
* CSS

### Backend

* Node.js
* Express.js
* Axios
* CORS

### Database

* MySQL
* MySQL Workbench

### Recommendation System

* Python
* Flask
* Pandas

## 📁 Project Structure

```text
AI-TripMate/
│
├── backend/
│   ├── server.js
│   ├── package.json
│   │
│   └── ml/
│       ├── destinations.csv
│       ├── recommendation.py
│       └── ml_api.py
│
├── src/
│   ├── App.tsx
│   ├── TripPlanner.tsx
│   └── ...
│
├── package.json
└── README.md
```

## 🔄 How It Works

1. The user enters their trip requirements through the React frontend.
2. React sends the trip information to the Node.js backend.
3. The backend stores the trip request in MySQL.
4. The backend sends the relevant information to the Python recommendation API.
5. The Python recommendation engine filters suitable destinations based on the user's preferences and budget.
6. The recommendations are returned to the backend.
7. The backend sends the recommendations back to the React application.

## ▶️ Running the Project

### 1. Start the Python Recommendation API

```bash
cd backend/ml
py ml_api.py
```

The API runs on:

```text
http://127.0.0.1:8000
```

### 2. Start t














# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])

```

You can also install [eslint-plugin-react-x](https://npmx.dev/package/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://npmx.dev/package/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])

```
