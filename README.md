<div align="center">

# 📊 WeightSmart Analytics
### Enterprise-Grade Weight Tracking & Data Visualization Platform

[![Java](https://img.shields.io/badge/Backend-Java%2021-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://spring.io/)
[![Kotlin](https://img.shields.io/badge/Mobile-Android%20Native-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Angular](https://img.shields.io/badge/Web-Angular%20%2B%20Nx-DD0031?style=for-the-badge&logo=angular&logoColor=white)](https://angular.io/)
[![PostgreSQL](https://img.shields.io/badge/Data-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![FHIR](https://img.shields.io/badge/Standard-HL7%20FHIR-firebrick?style=for-the-badge)](https://hl7.org/fhir/)

<p align="center">
  <b>Advanced Data Viz</b> • <b>HAPI FHIR Standard</b> • <b>Virtual Threads</b>
</p>

</div>

---

## 🎯 The Mission: Beyond Simple Logging

**WeightSmart** is an advanced health analytics platform designed to move beyond simple "input/output" logging. While most apps merely store data, WeightSmart focuses on **interpreting it**.

This project leverages enterprise architecture to provide:
1.  **Medical-Grade Data Integrity:** Storing weight and vitals using the international **HL7 FHIR** standard (via HAPI FHIR), ensuring data is ready for clinical integration.
2.  **High-Fidelity Visualization:** Transforming raw numbers into actionable intelligence through interactive, responsive dashboards that visualize trends, moving averages, and health correlations.

---

## 🏗️ The Architecture

Built to demonstrate how a modern, high-throughput health application should be architected in 2026.

### 1. The Core (Backend)
* **Language:** Java 21.
* **Key Feature:** Utilizing **Virtual Threads (Project Loom)** to handle high-concurrency data ingestion without the complexity of reactive chaining.
* **Standard:** Native **HAPI FHIR** implementation ensures every weight entry is a valid `Observation` resource, not just an arbitrary database row.
* **Security:** Stateless JWT authentication via strict **HttpOnly Cookies**, mitigating XSS risks common in health apps.

### 2. The Dashboard (Web)
* **Framework:** Angular 17+ (managed via **Nx**).
* **Focus:** **Advanced Data Visualization**.
* **Tech:** Leveraging standard charting libraries (e.g., Ngx-Charts/D3) to render complex, interactive time-series graphs that allow users to drill down from yearly trends to daily fluctuations instantly.

### 3. The Client (Mobile)
* **Language:** Kotlin (Android Native).
* **Pattern:** MVVM with Jetpack Compose.
* **Role:** A friction-free entry point for daily logging, optimized for speed and offline capability.

---

## ⚡ Technical Highlights

| Decision | Context |
| :--- | :--- |
| **Java 21 Backend** | Selected over Kotlin for the server to leverage **Virtual Threads** (simpler high-throughput concurrency) and native compatibility with the **HAPI FHIR** ecosystem. |
| **FHIR Compliance** | Data is stored as standard medical resources (`Observation`). This means the data isn't locked in a proprietary schema—it is technically ready to be read by hospital systems (Epic/Cerner) out of the box. |
| **Visualization First** | The Web Dashboard is architected as a pure analytics view. By decoupling the "Compute" (Java) from the "Display" (Angular), the server handles complex aggregations (e.g., rolling averages) so the client can render smooth, high-frame-rate visualizations. |

---

## 🛠️ Current Status

- [x] **Secure Identity Service:** Spring Security with HttpOnly Cookie rotation.
- [x] **Android Client:** Native Kotlin MVVM app for rapid data entry.
- [ ] **Analytics Engine:** Java service for calculating trend lines and health risk indicators.
- [ ] **Visualization Dashboard:** Angular frontend for interactive graphing.
