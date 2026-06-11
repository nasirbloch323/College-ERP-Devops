# 🎓 College ERP — DevOps Deployment

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white)

> A College Management System built with Django — Containerized with Docker and deployed on AWS EC2.

---

## 🌐 Live Demo
```
http://YOUR_EC2_IP:8000
```

---

## 🛠️ Tech Stack
| Technology | Usage |
|-----------|-------|
| Python/Django | Backend |
| SQLite | Database |
| Docker | Containerization |
| AWS EC2 | Cloud Deployment |
| Nginx | Web Server |

---

## 🚀 Deployment Steps

### Step 1: Clone Repository
```bash
git clone https://github.com/nasirbloch323/College-ERP-Devops.git
cd College-ERP-Devops
```

### Step 2: Dockerfile
```dockerfile
FROM python:3.10-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
RUN python manage.py migrate
EXPOSE 8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```

### Step 3: Build Image
```bash
docker build -t college-erp .
```

### Step 4: Run Container
```bash
docker run -d \
--name college-app \
-p 8000:8000 \
college-erp
```

### Step 5: Verify
```bash
docker ps
```

---

## 🔐 Login Credentials
| Role | Username | Password |
|------|----------|----------|
| Admin | admin | project123 |
| Student | samarth | project123 |
| Teacher | trisila | project123 |

---

## ✨ Features
- ✅ Student Management
- ✅ Teacher Management
- ✅ Attendance Tracking
- ✅ Marks & Performance
- ✅ Admin Dashboard
- ✅ Dockerized Deployment

---

## 📚 What I Learned
```
✅ Writing Dockerfile
✅ Building Docker Images
✅ Running Docker Containers
✅ AWS EC2 Deployment
✅ Security Group Configuration
```

---

*Made with ❤️ by Nasir Baloch — DevOps Journey 🚀*
