# 🛠️ monitoring-lab - Simple Monitoring Stack for Windows

[![Download monitoring-lab](https://img.shields.io/badge/Download-monitoring--lab-brightgreen)](https://github.com/rearward-plasmablast292/monitoring-lab)

---

## 📋 What is monitoring-lab?

monitoring-lab is a ready-to-use monitoring stack designed for Windows users who want to keep track of their systems and applications. It uses Docker Compose to run popular tools like Prometheus, Grafana, Zabbix, OpenSearch, and K3s all in one place. This helps detect problems faster and reduce downtime.

This tool is useful whether you run a personal project or a small business. It helps watch your system health, logs, and alerts without needing programming skills.

---

## 🖥️ System Requirements

Before you start, make sure your Windows computer meets the following:

- Windows 10 or newer, 64-bit version  
- At least 8 GB of RAM (16 GB recommended for larger setups)  
- Minimum 10 GB of free disk space  
- Docker Desktop installed and running  
- At least 4 CPU cores for smooth performance  
- Internet connection to download necessary components  

---

## 🚀 Getting Started

Follow these steps to download and run monitoring-lab on your Windows PC.

---

### 1. Download monitoring-lab

Head over to the main repository page to get all necessary files:

[![Get monitoring-lab](https://img.shields.io/badge/Download-https%3A%2F%2Fgithub.com%2Frearward--plasmablast292%2Fmonitoring--lab-blue)](https://github.com/rearward-plasmablast292/monitoring-lab)

This link takes you to the project page, where you can access the files and instructions.

---

### 2. Install Docker Desktop

monitoring-lab relies on Docker Compose. Install Docker Desktop if you don’t have it already.

- Go to [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)  
- Download the Windows version  
- Run the installer and follow the prompts  
- After installation, Docker Desktop should start automatically  

---

### 3. Clone or Download the project files

There are two easy ways to get the files:

- **Option A: Download ZIP**  
  - On the GitHub page, click the green **Code** button  
  - Choose **Download ZIP**  
  - Extract the files to a folder on your computer  

- **Option B: Use Git (optional)**  
  - If you have Git installed, open PowerShell or Command Prompt  
  - Run:  
    `git clone https://github.com/rearward-plasmablast292/monitoring-lab.git`  
  - This will download the project folder for you  

---

### 4. Open the project folder

Use File Explorer to find the folder where you saved or cloned monitoring-lab files.

Look for the file named `docker-compose.yml`. This file controls how the monitoring tools run together.

---

### 5. Run the monitoring tools

You will use PowerShell or Command Prompt to start the stack:

- Press **Windows + R**, type `powershell`, and press Enter  
- Navigate to the folder with `docker-compose.yml`. For example, if your folder is on the Desktop:  
  ```  
  cd "$Env:USERPROFILE\Desktop\monitoring-lab"  
  ```  
- Start the monitoring stack by running:  
  ```  
  docker-compose up -d  
  ```  

This command tells Docker to download and start all the monitoring services in the background.

---

### 6. Check if everything is running

Once the command finishes, check the status by opening your browser and visiting these addresses:

- Prometheus: [http://localhost:9090](http://localhost:9090)  
- Grafana: [http://localhost:3000](http://localhost:3000)  
- Zabbix: [http://localhost:8080](http://localhost:8080)  
- OpenSearch Dashboards: [http://localhost:5601](http://localhost:5601)  

If these pages load, your monitoring stack is up and running.

---

## ⚙️ How to Stop or Restart monitoring-lab

To stop all running tools, open PowerShell in the project folder and run:

```
docker-compose down
```

To restart, just run the start command again:

```
docker-compose up -d
```

---

## 🔧 Basic Configuration

You do not need to change anything to start seeing monitoring data right away. However, there are options to customize your setup.

- **Grafana Dashboards:** Preconfigured dashboards are available for common uses. Use the Grafana web interface at port 3000 to add or remove dashboards. Default login is usually `admin` / `admin`.  
- **Alerts:** Prometheus Alertmanager can notify you when things go wrong. You can configure alert rules in the `prometheus` folder inside the project files.  
- **Zabbix:** Use the Zabbix web UI to setup additional hosts and monitoring rules.  
- **OpenSearch:** Manage logs and search data with OpenSearch Dashboards.  

For more advanced setups, consult the official documentation of the individual tools linked on their websites.

---

## 🔄 Updating monitoring-lab

When a new version is released, you can update monitoring-lab with these steps:

1. Stop running stack with:  
   ```
   docker-compose down
   ```  
2. Delete old project folder (optional but recommended).  
3. Download the newest version again from the repository link above.  
4. Start it as before with:  
   ```
   docker-compose up -d
   ```  

---

## 🛠️ Troubleshooting Tips

- **Docker not running?** Make sure Docker Desktop is open and logged in if needed.  
- **Port conflicts?** If ports 3000, 9090, 8080, or 5601 are in use, stop other programs or change ports in the `docker-compose.yml` file.  
- **Slow performance?** Close other heavy apps and increase Docker memory settings in Docker Desktop preferences.  
- **Logs help:** Use `docker-compose logs` in PowerShell to see errors or messages from services.  

---

## 🔗 Useful Links

- GitHub project: https://github.com/rearward-plasmablast292/monitoring-lab  
- Docker Desktop: https://www.docker.com/products/docker-desktop  
- Prometheus docs: https://prometheus.io/docs/introduction/overview/  
- Grafana docs: https://grafana.com/docs/grafana/latest/  
- Zabbix docs: https://www.zabbix.com/documentation/current/manual  
- OpenSearch docs: https://opensearch.org/docs/latest/  

---

## 📂 Files Overview

- `docker-compose.yml` - Main file to run all monitoring services  
- `/prometheus/` - Prometheus configurations and alert rules  
- `/grafana/` - Grafana dashboard settings  
- `/zabbix/` - Zabbix configurations  
- `/opensearch/` - OpenSearch configuration files  
- `/k3s/` - Lightweight Kubernetes setup files  

---

## 🖱️ Download & Setup

Get started by visiting this page to download the files:

[https://github.com/rearward-plasmablast292/monitoring-lab](https://github.com/rearward-plasmablast292/monitoring-lab)