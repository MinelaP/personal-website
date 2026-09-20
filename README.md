# Minela Piljug — Software Engineer & UI/UX Developer Portfolio

A responsive personal portfolio and engineering showcase built with modern WebGL GLSL Shaders, clean HTML5/CSS3 UI components, and verified FlyRank AI credentials.

![Production Preview](https://img.shields.io/badge/Production-Live-success?style=for-the-badge&logo=vercel)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**Live Production URL:** [https://minelapiljug-personal-website.vercel.app](https://minelapiljug-personal-website.vercel.app)

---

## 🚀 Overview & Featured Projects

This portfolio serves as a central hub for my software engineering and UI/UX projects:

1. **CIS System Redesign (UI/UX Case Study):** Modernizing a complex system with a focus on data clarity and responsive web/mobile layouts.
2. **HN Logistic Desktop App (UI/UX):** Full-cycle design for a logistics desktop application, from requirements to interactive prototype.
3. **HN Logistic Desktop Application (Java):** Robust desktop application developed in Java (IntelliJ IDEA) focusing on backend logic and management tools.
4. **HN Logistic Web Solution (Web Development):** Responsive web solution for logistics management with clean UI and efficient data handling.
5. **Cinema (UI/UX):** Web and mobile concepts for cinema booking, focusing on intuitive user flows and seat selection.
6. **Film Search Application (film-tracker):** Real-time movie search web app integrated with dynamic Movie API endpoints.
7. **Hifa Petrol Ecosystem (UI/UX):** Loyalty mobile app and robust admin panel design for user management.
8. **FE-06 Streaming AI Chat (AI Engineering):** Token-by-token streaming AI chat interface powered by Next.js, Vercel AI SDK, and Llama 3.3.

---

## 🛠️ Environment Variables & Abuse Protection

To safeguard API resources and ensure production hygiene across deployed routes:

| Variable Name | Required | Default Value | Description |
| :--- | :--- | :--- | :--- |
| `NEXT_PUBLIC_VERCEL_ENV` | Yes | `production` | Production deployment target flag |
| `MAX_REQUESTS_PER_MIN` | Yes | `20` | Rate-limit threshold per IP to avoid credit exhaustion |
| `MAX_RESPONSE_DURATION` | Yes | `15s` | Maximum execution duration cap for streaming API handlers |

---

## 💻 Local Run Instructions

To clone and inspect this repository locally:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/MinelaP/personal-website.git](https://github.com/MinelaP/personal-website.git)
   cd personal-website