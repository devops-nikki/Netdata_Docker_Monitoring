# Task 7 – Monitor System Resources Using Netdata

## 📌 Objective
Install and configure **Netdata** to visualize system and application performance metrics in real time.

---

## 🛠 Tools Used
- **Netdata** – Free, open-source monitoring tool
- **Docker** – Containerized Netdata deployment
- **Browser** – For dashboard access (http://localhost:19999)

---

## 📖 Steps to Implement

### 1️⃣ Run Netdata in Docker
```bash
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
```

---

##  2️⃣ Access the Dashboard

 - Open your browser and visit:
   ```bash 
   http://localhost:19999
   ```

 - You will see a real-time monitoring dashboard.


## 3️⃣ Explore Metrics

 - CPU Usage – % user, % system, load averages.

 - Memory Usage – Used, free, cached, buffers.

 - Disk I/O – Read/write throughput, IOPS.

 - Docker Containers – Resource usage per container.

 - Alerts Panel – Active warnings or critical alerts.


## 4️⃣ View Logs

```bash
docker exec -it netdata bash
cd /var/log/netdata
ls
cat error.log
```

---

📸 Screenshots


## 🖥️ System Overview
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/System_Metric.png" alt="System Overview" width="800">
</div>

## 📦 Netdata Container
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/netdata_running.png" alt="Netdata Container Running" width="800">
</div>

## 💻 CPU Metrics
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/CPU_Metrics.png" alt="CPU Metrics" width="800">
</div>

## 🧠 Memory Metrics
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/Memory_Metrics.png" alt="Memory Metrics" width="800">
</div>

## 💽 Disk Metrics
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/Disk_Metrics.png" alt="Disk Metrics" width="800">
</div>

## 📊 Live Docker Container Metrics
<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/Live_Container_Metric.png" alt="Docker Container Metrics 1" width="800">
</div>

<div style="border: 1px solid #ddd; padding: 10px; margin-bottom: 15px;">
  <img src="screenshots/Live_Container_Metric_2.png" alt="Docker Container Metrics 2" width="800">
</div>

- Netdata Installed & Container is Running
![Netdata Container](screenshots/netdata_running.png)

🖥 System Overview
![System Overview](screenshots/System_Metric.png)

⚙ CPU Metrics
![CPU Metrics](screenshots/CPU_Metrics.png)

💾 Memory Metrics
![Memory Metrics](screenshots/Memory_Metrics.png)

📀 Disk Metrics
![Disk Metrics](screenshots/Disk_Metrics.png)

🐳Live Docker Container Metrics
![Docker Container Metrics](screenshots/Live_Container_Metric.png)
![Docker Container Metrics](screenshots/Live_Container_Metric.2.png)
---

## 🎯 Outcome

 - Successfully installed and ran Netdata in Docker.

 - Monitored CPU, RAM, Disk, and Docker container metrics in real time.

 - Understood lightweight monitoring for servers and applications.

---

## 📬 Contact
**Nikki Goyal** – DevOps Intern  
📧 Email: nikkigoyal679@gmail.com  
🔗 LinkedIn: [Nikki Goyal](https://www.linkedin.com/in/nikki-goyal-devops)

---