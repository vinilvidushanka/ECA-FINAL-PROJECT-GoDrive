# ITS 2130 ECA Project Submission - GoDrive Full-stack

Polyrepo architecture with Git submodules, implemented with **Spring Boot/Cloud** and **Next.js**, fully deployed on **Google Cloud Platform (GCP)**.

---

## 1. Student Information

| Field | Value |
| :--- | :--- |
| **Module** | ITS 2130 Enterprise Cloud Application |
| **Program** | HDSE @ IJSE |
| **Student Name** | Vinil Vidushanka |
| **Student ID** | 2301692013 |
| **Submission Date** | 2026-03-31 |
| **Main Repository** | https://github.com/vinilvidushanka/ECA-FINAL-PROJECT-GoDrive-backend.git |
| **GCP Project ID** | godrive-eca-project |

---

## 2. Project Overview

GoDrive is a modern vehicle rental platform built on a **Microservices Architecture**. 
* This repository acts as the **Main Orchestrator**, managing the entire system through Git Submodules.
* It follows a **Polyrepo model**, where each service is an independent repository.
* The system uses **Spring Cloud** for backend infrastructure and **Next.js** for the frontend.
* Deployed as non-containerized applications on **GCP Compute Engine**, managed by **PM2**.

---

## 3. Live Public URLs (Mandatory)

| Component | Public URL |
| :--- | :--- |
| **Frontend Application** | http://34.128.152.230:80 |
| **Eureka Dashboard** | http://34.93.114.63:8761/ |
| **API Gateway** | http://http://34.93.114.63:8080 |

---

## 4. Repository Structure (Polyrepo + Submodules)

### 4.1 Main Submodules
| Path | Repository | Purpose |
| :--- | :--- | :--- |
| `eca-platform` | [eca-platform](https://github.com/vinilvidushanka/eca-platform.git) | Infrastructure (Config, Eureka, Gateway) |
| `eca-services` | [eca-services](https://github.com/vinilvidushanka/eca-services.git) | Business services parent repo |
| `eca-webapp`   | [eca-webapp](https://github.com/vinilvidushanka/GoDrive-Frontend.git) | Next.js Frontend application |

### 4.2 Nested Submodules (Architecture Overview)
* **Platform Layer:** Config Server, Service Registry (Eureka), API Gateway.
* **Services Layer:** Booking Service, Customer Service, Vehicle Service.

---

## 5. Spring Cloud Components Implemented

* **Centralized Configuration:** Managed via Spring Cloud Config Server and Git-backed repo.
* **Service Discovery:** Implemented using Netflix Eureka for dynamic scaling.
* **API Gateway:** Predicate-based routing and centralized request handling.
* **Inter-service Communication:** Synchronous communication using OpenFeign.

---

## 6. High Availability and Auto Scaling

### 6.1 Microservice Auto Scaling
| Check | Value |
| :--- | :--- |
| Horizontal scaling supported | **YES** |
| Autoscaler configuration | **YES** |
| Multi-zone deployment | `asia-southeast1-a`, `asia-southeast1-b`, `asia-southeast1-c` |

---

## 7. PM2 Process Management

As per the non-containerized deployment requirements, all services are managed by PM2 for high availability and auto-restart capability.

| Requirement | Status |
| :--- | :--- |
| Applications managed by PM2 | **YES** |
| Auto-restart on failure | **YES** |
| PM2 starts on VM reboot | **YES** |

---

## 8. Screen Recording Submission
**Recording URL:** https://drive.google.com/file/d/1hVu1FWFhgjEtpV5_8yO1UhFG2QkR1V_X/view?usp=sharing

---

## 9. How to Clone This Repository

To clone the entire project with all nested submodules (Platform + Services):

```powershell
git clone --recurse-submodules [https://github.com/vinilvidushanka/ECA-FINAL-PROJECT-GoDrive-backend.git](https://github.com/vinilvidushanka/ECA-FINAL-PROJECT-GoDrive-backend.git)
cd ECA-FINAL-PROJECT-GoDrive-backend
git submodule update --init --recursive
git submodule status --recursive
```
