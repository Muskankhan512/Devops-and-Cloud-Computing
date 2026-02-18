Today I learned the fundamentals of Kubernetes and the main problems it solves in real-world infrastructure.
🔹 Why Kubernetes is needed (Problems it solves)
Container lifecycle management

🔹 Important Control Plane Components
kube-scheduler
→ Schedules pods on available nodes
Controller Manager
→ Handles different controllers
→ Example: restart controller (state management)
Cloud Controller Manager
→ Handles network and cloud-specific communication
etcd
→ Distributed key-value store
→ Stores all cluster state and configuration data
🔹 Controllers & State Management
Controllers continuously watch the current state and make sure the desired state is always maintained.
Example: restarting failed containers automatically.
🔹 Leader Election (Leader Detection Algorithm)
Leader election is used so that only one active controller instance manages a task at a time.
This avoids conflicts in distributed systems and is configured at the control-plane component level.
🔹 Linux Namespace (Related Concept)
Linux namespaces are used for isolation of:
processes
network
filesystem
users
Kubernetes uses Linux namespaces internally for container isolation.
🔹 Monitoring & Observability Tools (Explored)
Datadog
Dynatrace
Sumo LogicDifferent HTML on Port 80 and Port 8080

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
# 🐧 Advanced Linux Commands

This repository covers advanced Linux commands used for system administration,
debugging, performance monitoring, and automation.

---

## 🔍 File Searching & Text Processing

### find
Search files recursively
find /var/log -name "*.log" -size +10M

### grep (advanced)
grep -rin "error" /var/log

### awk
Print specific columns
awk '{print $1, $3}' file.txt

### sed
Replace text in file
sed 's/root/admin/g' file.txt

---

## 📊 System Monitoring

### top / htop
Real-time process monitoring

### vmstat
Memory usage
vmstat 2

### iostat
Disk I/O statistics
iostat -x 1

### free
Memory usage
free -h

---

## ⚙️ Process & Job Control

ps aux | grep nginx  
kill -9 PID  
nice -n 10 process  
renice -5 PID  

---

## 🔐 Permissions & ACL

getfacl file.txt  
setfacl -m u:user:rwx file.txt  

---

## 🌐 Networking & Ports

ss -tulnp  
netstat -anp  
lsof -i :80  
tcpdump -i eth0  

---

## 📦 Disk & Storage

df -h  
du -sh /var/*  
mount | column -t  
lsblk  

---

## 🧵 Archiving & Compression

tar -cvf backup.tar /data  
tar -xvf backup.tar  
tar -czvf backup.tar.gz /data  
tar -xzvf backup.tar.gz  

---

## 🔄 Piping & Redirection

command1 | command2  
command > output.txt  
command >> output.txt  
command 2> error.txt  

---

## ⏱️ Scheduling & Automation

### cron
crontab -e
0 2 * * * /backup.sh

### at
echo "shutdown now" | at 23:00

---

## 🧠 Debugging & Tracing

strace ls  
ltrace ./a.out  
watch -n 2 df -h  

---

## 🐳 Containers & Virtualization (Basics)

docker ps  
docker exec -it container bash  
docker logs container  Today I learned the fundamentals of Kubernetes and the main problems it solves in real-world infrastructure. 🔹 Why Kubernetes is needed (Problems it solves) Container lifecycle management Network management between containers Change & configuration management
Network management between containers
Change & configuration management
🔹 Kubernetes Architecture
Kubernetes mainly works with two major parts: Why Kubernetes is needed (Problems it solves) Container lifecycle management Network management between containers Change & configuration management Network management between containers Change & configuration management 🔹 Kubernetes Architecture Kubernetes mainly works with two major parts

