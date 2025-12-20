This project is a personal career dashboard for tracking job applications, interviews, and professional growth in one place. It treats the job search as a structured system rather than a collection of disconnected notes, spreadsheets, and calendar events.

This project is being built as a modern full-stack web application with an emphasis on clean architecture, data-driven insights, and thoughtful user experience.


# Core Goals

Log and manage job applications with a clear lifecycle

Track interview schedules and preparation

Analyze application outcomes and trends over time

Centralize personal projects, skills, and technical practice

Serve as a practical demonstration of modern web engineering

# Planned Features
## Job Application Tracking

Company, role, and application metadata

Status progression (Applied → Interview → Offer → Outcome)

Notes, reflections, and context per application

## Analytics & Insights

Application funnel metrics

Time-to-response and time-to-offer analysis

Trends by role type, source, and company

## Interview Calendar

Internal interview scheduling

Time zone handling and reminders

Calendar export and external integrations (planned)

## Personal Growth Tracking

Personal and professional projects

Skills and technical practice (e.g. LeetCode)

GitHub activity integration (planned)

## AI-Assisted Tools (future)

Resume-to-job matching insights

Interview preparation assistance

Semantic search across notes and reflections

## Tech Stack

Frontend: React, TypeScript, Vite

Backend: Supabase (PostgreSQL, Auth, Row Level Security)

Tooling: Modern browser APIs, ESLint

## Project Status

Early development

Current focus:

Establishing core data models

Authentication and secure data access

Building the first vertical slice (Add → View → Edit job applications)

____________________________________________

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is currently not compatible with SWC. See [this issue](https://github.com/vitejs/vite-plugin-react/issues/428) for tracking the progress.

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

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

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
