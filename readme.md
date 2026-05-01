# Fake Live Server JSON

A Node.js backend project using JSON Server to provide a fake REST API for development and testing. This project is designed to work as a standalone backend service or deployed to Render.

## Project Setup & Deployment Notes (JSON Server + Render)

### 1. Project Initialization

- Created an empty project folder
- Opened it in VS Code
- Initialized Node.js project using:
  ```
  npm init -y
  ```

### 2. Fake Backend Setup

- Created a file named `db.json`
- Added fake data for:
  - courses
  - teachers

### 3. JSON Server Setup

- Installed JSON Server (if needed):

  ```
  npm install json-server
  ```

- Added custom script in `package.json`:

  ```json
  "server": "json-server --watch db.json --port 5000"
  ```

- This allows running backend server using:
  ```
  npm run server
  ```

### 4. Port Configuration

- Changed default JSON server port to 5000
- Ensures consistency for frontend API calls

### 5. Public Folder Setup (for deployment)

- Created a folder named `public`
- Added a `.gitkeep` file inside it
  (to ensure Git tracks the empty folder)

**Note:** In deployment platforms, important static/public files are often required to be present in tracked folders.

### 6. GitHub Deployment

- Pushed project to GitHub repository
- Ensured `db.json` and project structure are included properly

### 7. Render Deployment (Backend Hosting)

- Logged in to Render using GitHub account
- Created a new Web Service project
- Selected:
  - Language: Node.js

- Build Command:

  ```
  npm install
  ```

- Start Command:

  ```
  npm run server
  ```

- Render runs the JSON server using the script defined in `package.json`

### 8. Final Result

- JSON Server backend is now live on Render
- Data is accessible through hosted API endpoints
- Frontend can connect using deployed Render URL instead of localhost
