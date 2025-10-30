Deploy to Render - Warehouse App (Option A)
==========================================

This package prepares your app for deployment on Render.com using Docker containers.

Steps to deploy on Render:
1. Create a Git repository and push your project root (ensure backend/ and frontend/ folders exist).
2. Edit `render.yaml` and replace REPLACE_WITH_YOUR_REPO_URL with your repo URL.
3. Import the repo or create services manually on Render:
   - Create a managed Postgres DB (starter plan).
   - Create a web service for backend using backend/Dockerfile and set DATABASE_URL env var to the DB URL.
   - Create a web service for frontend using frontend/Dockerfile.
4. Deploy and check logs. Backend should be reachable at its public URL; frontend will be served by nginx.

If you want, I can prepare the Git repo layout and give you a ZIP ready to push to GitHub.
