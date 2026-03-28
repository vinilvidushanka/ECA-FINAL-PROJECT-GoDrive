# 🚗 GoDrive - Enterprise Cloud Vehicle Management System

## 1. Project Overview
**GoDrive** is a cloud-native, microservice-based vehicle management system developed for the **Enterprise Cloud Architecture (ITS 2130)** module. The system is designed to evaluate cloud-native patterns, including high availability, fault tolerance, and automatic horizontal scaling, all deployed on the **Google Cloud Platform (GCP)**.

---

## 2. Student Information
| Field | Details |
| :--- | :--- |
| **Module** | ITS 2130 - Enterprise Cloud Architecture |
| **Program** | HDSE @ IJSE |
| **Student Name** | Vinil Vidushanka |
| **Submission Date** | 22nd March, 2026 |
| **GCP Project ID** | `godrive-eca-project-a38366f2347c` |

---

## 3. Technology Stack 🛠️
* **Backend:** Java 25+, Spring Boot, Spring Cloud (Gateway, Eureka, Config).
* **Databases:**
    * **Relational:** Cloud SQL (MySQL) for core structured data.
    * **Non-Relational:** MongoDB for flexible metadata storage.
* **Cloud Infrastructure (GCP):** VPC Network, Compute Engine (VMs), Cloud Storage Buckets, Load Balancer, Cloud NAT Gateway.
* **Process Management:** **PM2** (Used for mandatory automatic restart and system reliability).

---

## 4. System Architecture
This project follows a **Polyrepo architecture** utilizing **Git Submodules** for centralized management of all services.

* **Config Server:** Centralized and externalized configuration management.
* **Eureka Service Registry:** Used for real-time service registration and discovery.
* **API Gateway:** Serves as the single entry point for all backend microservices.
* **Auto-Scaling:** Backend services are deployed using Managed Instance Groups to support automatic horizontal scaling based on load.

---

## 5. Mandatory Verification Links 🔗
* **Eureka Dashboard (Public URL):** [http://34.93.114.63:8761](http://34.93.114.63:8761)
* **Frontend Application:** [http://34.93.114.63:80](http://34.93.114.63:80)

---

## 6. Process Management (PM2) 🚀
To ensure process-level fault tolerance, all application services are managed by **PM2**. This setup ensures that services restart automatically upon failure or system reboot.

```bash
# Execute these commands on the VM to verify status:
pm2 monit
pm2 list
