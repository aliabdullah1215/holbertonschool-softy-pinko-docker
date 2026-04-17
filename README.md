# 🚀 Holberton School - Softy Pinko Docker Project

This project demonstrates how to build, containerize, and scale a full-stack web application using **Docker**, **Docker Compose**, and **Nginx**.

The application consists of:

* A **Flask API (Back-end)**
* A **Static Front-end (HTML/CSS/JS)**
* An **Nginx Proxy Server**
* **Docker Compose orchestration**
* **Horizontal scaling (load balancing)**

---

## 📁 Project Structure

```
holbertonschool-softy-pinko-docker/
│
├── task0/   # Basic Docker image
├── task1/   # Flask API server
├── task2/   # Front-end + Back-end separation
├── task3/   # Front-end connected to Back-end
├── task4/   # Docker Compose setup
├── task5/   # Nginx reverse proxy
└── task6/   # Horizontal scaling (multiple API servers)
```

---

## 🧩 Technologies Used

* Docker
* Docker Compose
* Nginx
* Python 3
* Flask
* Flask-CORS
* HTML / CSS / JavaScript (AJAX)

---

## 🛠️ Tasks Overview

### 🔹 Task 0 - First Docker Image

* Built a Docker image using Ubuntu
* Updated system packages
* Printed `"Hello, World!"`

---

### 🔹 Task 1 - Back-end (Flask API)

* Installed Python3, pip, and Flask
* Created an API endpoint:

```
/api/hello → "Hello, World!"
```

---

### 🔹 Task 2 - Front-end + Back-end Separation

* Structured project into:

  * `back-end/`
  * `front-end/`
* Served front-end using Nginx

---

### 🔹 Task 3 - Connect Front-end to Back-end

* Added AJAX request in `index.html`
* Enabled CORS in Flask using `flask-cors`
* Displayed dynamic content from API

---

### 🔹 Task 4 - Docker Compose

* Created `docker-compose.yml`
* Ran multiple services together:

  * Back-end
  * Front-end

---

### 🔹 Task 5 - Proxy Server (Nginx)

* Added reverse proxy server
* Routed requests:

```
/      → front-end
/api   → back-end
```

* Removed direct access to services

---

### 🔹 Task 6 - Horizontal Scaling

* Scaled API servers using:

```
docker-compose up --scale back-end=2
```

* Implemented load balancing (Round Robin)

---

## 🚀 How to Run the Project

### 🔧 Build & Run with Docker Compose

```bash
docker-compose build
docker-compose up
```

### 🌐 Access the App

```
http://localhost
```

---

## ⚖️ Load Balancing

To run multiple API servers:

```bash
docker-compose up --scale back-end=2
```

Requests will be distributed automatically between instances.

---

## 📡 API Endpoint

```
GET /api/hello
```

Response:

```
Hello, World!
```

---

## 🧪 Testing

You can test the API using:

```bash
curl http://localhost/api/hello
```

---

## ⚠️ Notes

* Only the proxy server exposes ports to the host
* Internal services communicate via Docker network
* Nginx acts as:

  * Static server
  * Reverse proxy
  * Load balancer

---

## 💡 Best Practices Applied

* Clean Dockerfile structure
* Separation of concerns (front-end / back-end / proxy)
* Use of Docker Compose for orchestration
* Proper port exposure
* Scalable architecture

---

## 👨‍💻 Author

* Holberton School Student

---

## 📌 Conclusion

This project demonstrates a complete containerized architecture including:

* API development
* Front-end integration
* Reverse proxying
* Service orchestration
* Horizontal scaling

---

🔥 This setup is a simplified version of real-world production architectures.
