# Docker GPTR Evaluation Dashboard
## Description

This repository contains a Large Language Model (LLM) evaluation dashboard powered by FastAPI (backend) and Next.js (frontend), containerized with Docker.

## It provides:

Backend (FastAPI): Manages LLM research runs, stores results in SQLite, and exposes APIs.

Frontend (Next.js): Interactive dashboard for visualizing benchmarks, reports, and citations.

SQLite: Lightweight embedded database to store experiment results (no external DB required).

# DRAFT - Documentation du Projet


## Installation
To set up the project, follow these steps:

1. Clone the repository: 
   ```bash
   git clone [repository_url]
   ```
2. Navigate to the project directory:
   ```bash
   cd GPT_Researcher_docker/
   ```
3. Ensure the docker-compose.yaml file is present in the repository
4. create a .env file and add the variables : 
    ```     
    DATABASE_URL="sqlite:///./research.db"
    TAVILY_API_KEY=""
    OPENAI_API_KEY=""
    GOOGLE_API_KEY=""
    MISTRAL_API_KEY=""

    ```
5. Clone the frontend and backend repositories inside the docker directory
    ```bash
    git clone [backend_package_url] 
    ```
    ```bash
    git clone [frontend_package_url] 
    ```
Make sure after you clone, your folder structure looks like this
```
GPT_Researcher_docker/
├── GPT_Researcher_backend/
│   ├── app/
│   ├── Dockerfile
│   └── requirements.txt
├── GPT_Researcher_frontend/
│   ├── app/
│   ├── Dockerfile
│   ├── package.json
│   └── next.config.js
└── docker-compose.yml
```
6. Build the containers:
```bash
docker compose build
```
7. Start the containers:
```bash
docker compose up
```
8. Stop containers:
```bash
docker compose down
```
9. Check logs:
```bash
docker compose logs -f
```

