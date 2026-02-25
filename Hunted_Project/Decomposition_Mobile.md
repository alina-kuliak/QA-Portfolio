# 🧩 Functional Decomposition: Huntd Mobile

This document outlines the structural breakdown of the Huntd mobile application. It serves as the foundation for the Requirement Traceability Matrix (RTM) and test suite design.

---

## 🗺️ High-Level Map
The application is divided into three primary states based on user authentication and role selection.

```mermaid
graph TD
    A[Huntd Mobile App] --> B[Unauthorized State]
    A --> C[Authorized: Recruiter]
    A --> D[Authorized: Candidate]

    B --> B1[Home Screen]
    B --> B2[Sign In / Forgot Password]
    B --> B3[Sign Up / Social Auth]

    C --> C1[Chats & Archive]
    C --> C2[Profile Management]
    C --> C3[Company/Role Setup]

    D --> D1[Chats & Archive]
    D --> D2[Detailed Resume/Role]
    D --> D3[Expectations & Experience]
