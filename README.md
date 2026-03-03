# Hi, I'm Tatsapon Munsan 👋

I'm Software Developer specializing in **Mobile Architecture (Flutter)**, Experienced in building scalable, production-grade systems — from IoT-driven mobile applications to cloud-native microservices serving thousands of corporate clients.

Key highlights:

- Led mobile development for a **Cloud HR & Payroll platform** serving **2,000+ corporate clients**
- Engineered a **Go-based DB Transfer Engine** that reduced legacy data migration from **3 hours → 5 minutes** (97% improvement)
- Architected an **event-driven Email Microservice** deployed on Kubernetes with RabbitMQ and Kong Gateway
- Delivered end-to-end IoT mobile solution integrating **Nedap sensors** for real-time livestock management

---

## Technical Skills

| Domain | Technologies |
| --- | --- |
| **Mobile** | Flutter, GetX, Dio, Firebase (FCM), Biometric Auth, dio_cache_interceptor |
| **Backend** | Go (Golang), Java Spring Boot, JPA/ORM, RabbitMQ |
| **Frontend** | Next.js, Zustand (Slice Pattern), TanStack Query, shadcn/ui |
| **Infrastructure** | Kubernetes (K8s), Kong API Gateway, Grafana |
| **Security** | Firebase Auth, Microsoft SSO (multi-tenant), OAuth2, Microsoft Graph API, SMTP |
| **Databases** | MariaDB (legacy migration expertise) |

---

## Professional Experience

### Consultant Mobile Application Developer

**TigerSoft (1998) Co. Ltd.** · Bangkok, Thailand · *May 2024 – Present*

Lead mobile development of **TigerOpenSpace** — TigerSoft's flagship SaaS HRMS platform, modernizing HR & Payroll workflows for **2,000+ enterprise clients** across Thailand.

#### Mobile Architecture & Core Development

- Architected the application using **Flutter Clean Architecture** (Controller · Service · Model · View · Binding) with **GetX** for reactive state management, dependency injection, and centralized routing
- Built a resilient API communication layer with **Dio** featuring global interceptors for auto-token injection, silent token refresh, and centralized error handling — maintaining **99.9% session uptime**
- Implemented a **multi-layer client caching strategy** to optimize performance and enable offline-first behaviour:
  - **Dio Cache Interceptor** — HTTP response caching with configurable TTL, reducing redundant network calls for reference data (employee lists, leave types, org charts)
  - **SharedPreferences** — stored lightweight session state (auth tokens, user preferences, last-sync timestamps)
  - **In-memory cache (GetX controllers)** — held hot runtime data in reactive streams to eliminate repeated I/O within a session
- Integrated **Microsoft SSO (multi-tenant)**, and **Biometric Auth** (Face ID / Fingerprint) for PDPA-compliant protection of sensitive payroll and personal data — architected Microsoft SSO to support **multi-tenant authentication**, enabling a single app deployment to serve multiple corporate organizations under separate Azure AD tenants
- Developed a full suite of enterprise HR modules across ESS (Employee Self-Service) and MSS (Manager Self-Service) domains:
  - **Time Attendance** — GPS-verified clock-in/out with real-time record submission and approval workflow
  - **ESS & MSS Calendars** — dual-role calendar views for employees to submit requests and managers to review team schedules and resource coverage
  - **Leave Management** — end-to-end leave request, approval routing, and balance tracking
  - **Notification & Approval Engine** — real-time Push Notifications (FCM) across all app states (Foreground, Background, Terminated) driving approval workflows for time, leave, expense, and advance requests
  - **Welfare Module** — employee welfare entitlement tracking and claim submission
  - **Expense Management** — expense claim submission with receipt attachment and multi-level approval
  - **Advance Payroll Request** — in-cycle salary advance request with approval and payroll deduction integration
  - **To-Do / Task Management** — personal task tracking module integrated with notification reminders
- Created a reusable **TigerSoft Widget Library** (Custom Forms, Date Pickers, Modals), cutting new-feature development lifecycle by **30%**

#### Web Dashboard (Next.js)

- Developed internal dashboards using **Next.js** and **shadcn/ui**, applying Clean Architecture to decouple business logic from the UI
- Managed global client state with **Zustand (Slice Pattern)** and engineered a comprehensive server-state caching layer using **TanStack Query (React Query)**:
  - Tuned **`staleTime` / `gcTime`** per query domain — keeping frequently accessed data (leave balances, shift schedules) fresh in memory without over-fetching
  - Applied **optimistic updates** on mutation flows (leave submissions, attendance corrections) with automatic rollback on server error, delivering instant perceived performance
  - Used **query invalidation and selective refetch** after mutations to ensure cache consistency across related data without a full page reload
- Leveraged **Next.js fetch cache** (ISR with `revalidate`) for static-heavy pages, reducing server load on high-traffic report views while keeping data acceptably fresh

#### Backend & Infrastructure Engineering

- **DB Transfer Engine (Go):** Designed and built a concurrent data migration tool to transfer 1–2 GB of legacy customer data to modern schemas. Result: reduced migration runtime from **3 hours → under 5 minutes** (97% performance gain) via Go concurrency primitives
- **Enterprise Email Microservice:** Built an event-driven mailing service on **RabbitMQ** with multi-provider support (Microsoft Graph API, OAuth2, SMTP/Gmail)
- **Cloud Infrastructure:** Deployed services on **Kubernetes (K8s)** with **Kong API Gateway** for traffic management; established **Grafana** observability dashboards for real-time monitoring

---

### Junior Software Developer

**Zyntelligent** · Maha Sarakham, Thailand · *October 2023 – April 2024*

#### Project: SianWua (เซียนวัว) — Smart Livestock Management System

Led end-to-end development of a specialized mobile platform for cattle farm management, bridging real-time IoT sensor data with enterprise-grade mobile architecture.

- **IoT Integration:** Architected integration with **Nedap livestock sensors** via API for real-time monitoring of cow health, heat detection (estrus), and illness alerts — enabling data-driven farm management
- **Mobile Development (Flutter & GetX):** Built an offline-first mobile UI optimized for rugged farm environments with reactive state management
- **Networking & Alerts:** Managed complex data synchronization with **Dio** and implemented **Firebase Cloud Messaging (FCM)** for critical real-time alerts (health emergencies, breeding windows)
- **Backend Contribution (Java Spring Boot):** Developed backend services using **Spring Boot** with **JPA/ORM** for structured data persistence in MariaDB
- **Feature Engineering:** Designed and shipped core modules — Cattle Registration, Health Tracking, and Breeding Cycle Management

---

## Education

**Bachelor of Science in Information Technology**
Mahasarakham University · Graduated May 2024

---
