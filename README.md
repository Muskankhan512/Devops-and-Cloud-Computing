Different HTML on Port 80 and Port 8080

This project demonstrates how a single machine can serve different HTML pages on different ports.

🔧 How it works

Port 80 → Serves index.html

Port 8080 → Serves index8080.html

🧪 Test using curl
curl localhost
curl localhost:8080

📚 What you’ll learn

Basics of ports & networking

How web servers handle multiple services

Practical usage of curl

Real-world server configuration concept
🚀 FastAPI Setup using pipx & Uvicorn

Today I learned how to set up and run a FastAPI application using pipx and uvicorn.

✔ Installed pipx for isolated Python tools  
✔ Installed FastAPI with standard dependencies  
✔ Used uvicorn to run the application  
✔ Learned how to run the server with reload and multiple workers  
✔ Practiced basic Linux commands and networking check using ss

Commands practiced:
- sudo apt update
- sudo apt install pipx
- pipx install "fastapi[standard]"
- pipx inject uvicorn fastapi
- uvicorn main:app --reload
- uvicorn main:app --workers 2
- ss -ntlp

This is part of my backend development learning journey.
