# Job Portal Frontend

A responsive, single-page web application for a Job Portal platform built with **React**. It provides an intuitive interface for job seekers to browse listings and apply for jobs, and for employers to post and manage openings.

---

## Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
  - [Running with Mock API](#running-with-mock-api)
- [Available Scripts](#available-scripts)
- [Connecting to the Backend](#connecting-to-the-backend)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The Job Portal Frontend is a React-based SPA that communicates with the [Job Portal Backend](https://github.com/talhath85/Job-Portal-Backend) REST API. It includes a local `db.json` file powered by [JSON Server](https://github.com/typicode/json-server) for rapid development and prototyping without needing the full backend running.

Key features include:

- Browse and search job listings
- View detailed job descriptions

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 (Create React App) |
| Language | JavaScript (ES6+) |
| Styling | CSS |
| Mock API | JSON Server (`db.json`) |
| Package Manager | npm |

---

## Project Structure

```
Job-Portal-Frontend/
├── public/                   # Static assets and index.html
├── src/
│   ├── components/
│   │   └── Search.jsx        # Search component
│   ├── App.js                # Root component and routing
│   ├── App.css               # App-level styles
│   ├── App.test.js           # App component tests
│   ├── index.js              # Entry point
│   ├── index.css             # Global styles
│   ├── logo.svg              # App logo
│   ├── reportWebVitals.js    # Performance reporting
│   └── setupTests.js         # Test configuration
├── db.json                   # Mock database for JSON Server
├── package.json
└── .gitignore
```

---

## Getting Started

### Prerequisites

Make sure you have the following installed:

- **Node.js 16+** — [Download](https://nodejs.org/)
- **npm** (comes with Node.js)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/talhath85/Job-Portal-Frontend.git
cd Job-Portal-Frontend
```

2. Install dependencies:

```bash
npm install
```

### Running the App

Start the development server:

```bash
npm start
```

The app will be available at [http://localhost:3000](http://localhost:3000). The page automatically reloads when you make changes to the source files.

### Running with Mock API

The project includes a `db.json` file that can be served locally using JSON Server, allowing you to develop without the Spring Boot backend.

1. Install JSON Server globally (if not already installed):

```bash
npm install -g json-server
```

2. Start the mock API server:

```bash
json-server --watch db.json --port 8080
```

The mock API will be available at [http://localhost:8080](http://localhost:8080).

---

## Available Scripts

| Script | Description |
|---|---|
| `npm start` | Runs the app in development mode at `http://localhost:3000` |
| `npm test` | Launches the test runner in interactive watch mode |
| `npm run build` | Builds the app for production into the `build/` folder |
| `npm run eject` | Ejects from Create React App (one-way, irreversible) |

---

## Connecting to the Backend

By default, API calls point to `http://localhost:8080`. To connect to the live [Job Portal Backend](https://github.com/talhath85/Job-Portal-Backend):

1. Make sure the Spring Boot backend is running on port `8080`.
2. Update the base API URL wherever fetch/axios calls are made in `App.js`:

```javascript
const BASE_URL = "http://localhost:8080/api";
```

3. To point to a deployed backend, replace the URL with your production endpoint.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a Pull Request
