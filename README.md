# 🚗 GoDrive - Enterprise Cloud Vehicle Management System

## 1. Project Overview
**GoDrive** is a cloud-native, microservice-based vehicle management system developed for the **Enterprise Cloud Architecture (ITS 2130)** module. This project demonstrates high availability, fault tolerance, and automatic horizontal scaling capabilities deployed on the **Google Cloud Platform (GCP)**.

This project uses Spring Cloud microservices in a **Polyrepo** model. Each platform component and business microservice is maintained in its own GitHub repository, with this main repository acting as the central entry point using **Git Submodules**.

---

## 2. Student Information
| Field | Details |
| :--- | :--- |
| **Module** | ITS 2130 - Enterprise Cloud Architecture |
| **Program** | HDSE @ IJSE |
| **Student Name** | Vinil Vidushanka |
| **Student Number** | 2301692013 |
| **Submission Date** | 22nd March, 2026 |
| **GCP Project ID** | `godrive-eca-project-a38366f2347c` |

---

## 3. Technology Stack 🛠️
* **Backend:** Java 25, Spring Boot, Spring Cloud (Gateway, Eureka, Config).
* **Databases:**
    * **Relational:** Cloud SQL (MySQL) for core vehicle records.
    * **Non-Relational:** MongoDB for flexible metadata storage.
* **Cloud Infrastructure (GCP):** VPC, Compute Engine (VMs), Cloud Storage Buckets, Load Balancer, Cloud NAT Gateway.
* **Process Management:** **PM2** (Mandatory for automatic restart and system reliability).

---

## 4. Live Public URLs (Mandatory)
| Component | Public URL |
| :--- | :--- |
| **Frontend Application** | [http://34.93.114.63:80](http://34.93.114.63:80) |
| **Eureka Dashboard (Mandatory)** | [http://34.93.114.63:8761](http://34.93.114.63:8761) |

---

## 5. Repository Structure (Polyrepo + Submodules)
This project follows a polyrepo architecture as required. Each service is included as a Git submodule.

### 5.1 Main Submodules
| Path | Purpose |
| :--- | :--- |
| **Platform** | Platform layer parent repo (Gateway, Registry, Config) |
| **Services** | Business services parent repo (Vehicle Management) |
| **Webapp** | Frontend application |

---

## 6. Spring Cloud Components Implemented
* **Spring Cloud Config Server:** Centralized configuration management.
* **Spring Cloud Netflix Eureka Server:** Service registration and discovery.
* **Spring Cloud API Gateway:** Single entry point for all backend services.

---

## 7. High Availability and Auto Scaling (Mandatory)

### 7.1 Microservice Auto Scaling
| Check | Value |
| :--- | :--- |
| **Horizontal scaling supported** | YES |
| **Autoscaler configuration** | YES |
| **Instance group details** | YES |

### 7.2 Platform High Availability
| Check | Value |
| :--- | :--- |
| **Multi-instance deployment** | YES |
| **Multi-zone deployment** | asia-southeast1-a, asia-southeast1-b, asia-southeast1-c |
| **Fault-tolerance evidence** | YES |

---

## 8. PM2 Process Management and Auto Restart (Mandatory)
Since the deployment is non-containerized, **PM2** is used to manage all application processes.

### 8.1 PM2 Verification Commands
```bash
pm2 status
pm2 monit
pm2 startup
pm2 save
```

## 9. Screen Recording Submission (Mandatory)

Recording URL: https://drive.google.com/file/d/12L4fkenJXVYBrzwBsfufipEPKwNqd9bQ/view?usp=drive_link
