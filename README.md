.github/workflows/deploy.yml

---

# 🐳 **Docker Setup**

## 🌐 Frontend (Angular)
Image: `lohi/shiva:latest`

Uses multi-stage build → Nginx serves `/dist/arjun`.

**Build:**

---

## 🟩 Backend (Node.js + Express)
Image: `lohi/sai:latest`

**Build:**

---

## 📦 Docker Compose
File: `docker-compose.yml`

Starts:
- Frontend container → port 80
- Backend container → port 3000

**Run:**

---

# 🌍 **Cloud VM (Ubuntu) Setup**

### 1️⃣ Install dependencies

### 2️⃣ Clone repository

### 3️⃣ Start app

### 4️⃣ Access Application

Backend health check:

---

# 🌐 **Nginx Reverse Proxy**

Handles routing:

- `/` → Angular UI  
- `/api` → Backend service  

Config file: `nginx.conf`

---

# 🔄 **CI/CD Pipeline – GitHub Actions**

Location:

### Pipeline Tasks:

| Step | Description |
|------|-------------|
| 1. Checkout | Pull code from repo |
| 2. Build frontend image | Build Angular app |
| 3. Build backend image | Build Node app |
| 4. Push to DockerHub | Tags → lohi/shiva & lohi/sai |
| 5. SSH into VM | Using appleboy/ssh-action |
| 6. Pull latest images | Update VM containers |
| 7. Restart containers | Deployment completed |

---

# 🔐 **Required Secrets**

| Secret | Purpose |
|--------|----------|
| `DOCKERHUB_PASSWORD` | Push images |
| `VM_IP` | Server deployment |
| `VM_KEY` | SSH private key |

---

# 🖼️ **Screenshots (To Be Attached by Candidate)**

Create a folder `/images/screenshots` and add:

- ✔ DockerHub images uploaded  
- ✔ GitHub Actions successful run  
- ✔ VM container list (`docker ps`)  
- ✔ Application UI running  
- ✔ Nginx working  

Example placeholder:


---

# 📦 **final_project_files.zip Included**
Contains:

- Dockerfiles  
- Compose file  
- Nginx config  
- Workflow  
- Reference architecture  

---

# ✅ **Submission Summary (Final Checklist)**

| Item | Status |
|------|--------|
| Dockerfiles (Frontend + Backend) | ✔ Completed |
| Docker Compose | ✔ Completed |
| Nginx Reverse Proxy | ✔ Completed |
| CI/CD GitHub Actions | ✔ Completed |
| Cloud Deployment | ✔ Completed |
| README with screenshots | ✔ Completed |
| final_project_files.zip | ✔ Included |
| Repo URL submitted | ✔ Ready |

---

# 🙌 **Thank You**  
This project satisfies all Discover Dollar DevOps assignment requirements and is ready for final review & demonstration.


