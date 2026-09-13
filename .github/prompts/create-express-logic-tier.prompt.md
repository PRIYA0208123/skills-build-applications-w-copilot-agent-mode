---
mode: 'agent'
model: GPT-5.5
description: 'Create the Node.js logic tier for the Octofit multi-tier application'
---

Create the logic tier in `octofit-tracker/backend` for the Octofit Tracker multi-tier application.

Scaffold the implementation as a self-contained TypeScript Node.js project. Use path-qualified commands from the current directory and do not change directories.

Requirements:

1. Do not change directories; use path-qualified commands.
2. Initialize a TypeScript Node.js API with Express.
   - Create the package metadata, TypeScript configuration, and source files under `octofit-tracker/backend`.
   - Use a JSON API with CORS and JSON-body parsing enabled.
3. Configure scripts for build/dev/start.
   - `build` must compile TypeScript to a disposable build directory.
   - `dev` must run the TypeScript server with automatic reloads.
   - `start` must run the compiled JavaScript server.
4. Add route handlers for:
   - `/api/users/`
   - `/api/teams/`
   - `/api/activities/`
   - `/api/leaderboard/`
   - `/api/workouts/`
   - Register each route under `/api`, use trailing-slash-compatible paths, and return valid JSON responses with suitable HTTP status codes. Keep handlers modular and easy to replace with persistence later.
5. Keep server port on `8000`.
   - Bind to a host suitable for local development and Codespaces.
6. Add Codespaces-aware API URL support using `CODESPACE_NAME`.
   - Expose a reusable API base URL that uses `https://${CODESPACE_NAME}-8000.app.github.dev` when `CODESPACE_NAME` is set, and `http://localhost:8000` otherwise.
   - Document the resulting setup and commands in a backend README.

After scaffolding, verify the project with the build command and report the files created and verification result. Do not implement a frontend or modify files outside `octofit-tracker/backend`.
