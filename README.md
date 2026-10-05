# DevOps Practice Project

A small Flask API used to practice a full DevOps pipeline: version control, automated testing, containerization, CI/CD, infrastructure as code, and monitoring.

## Live app
https://devops-project-iac.onrender.com/status

## What this project covers
- **Version control** — Git & GitHub
- **Testing** — automated tests with pytest
- **Containerization** — Docker
- **CI** — GitHub Actions runs tests on every push
- **CD** — auto-deploys to Render on every push to `main`
- **Infrastructure as Code** — the Render service is defined in `render.yaml`, not clicked together by hand
- **Monitoring** — UptimeRobot checks `/status` every 5 minutes and alerts on downtime

## Run it locally
\`\`\`bash
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install -r requirements.txt
python app.py
\`\`\`

## Run it in Docker
\`\`\`bash
docker build -t devops-app .
docker run -p 5000:5000 devops-app
\`\`\`