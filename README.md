# GSoC 2025 Proposal: CCSync – TaskServer II

## 📌 Project Title

**TaskServer II – Making Task Synchronization Effortless**

## 🏢 Organization

**CCExtractor**
[GitHub](https://github.com/CCExtractor)

## 👤 Student Information

**Name:** Nileshkumar Yadav
**College:** Shree L. R. Tiwari College of Engineering, University of Mumbai
**GitHub:** [Ni1esh-Yadav](https://github.com/Ni1esh-Yadav)
**LinkedIn:** [linkedin.com/in/ni1esh-yadav](https://linkedin.com/in/ni1esh-yadav)
**Zulip:** [CCExtractor Zulip](https://ccextractor.zulipchat.com/#user/866756)

## 🔎 Abstract

CCSync is a lightweight task sync server and web UI/API for TaskWarrior clients. The aim of this GSoC project is to transition CCSync to production-readiness by:

* Removing Firebase dependency
* Implementing secure Google OAuth and JWT-based authentication
* Adding IndexedDB-based offline support
* Enhancing API scalability and security
* Strengthening mobile (Flutter app) integration
* Enabling easy self-hosting via Docker

## 🎯 Why This Project?

**To Me:** I love contributing to open source and solving real-world problems. This project combines my interest in backend systems, scalable architectures, and usability.
**To the Community:** CCSync offers a self-hosted, cost-free alternative to task managers with offline sync, cross-device compatibility, and extensible architecture.

## 🧩 Problem Statement

CCSync is not production-ready due to:

* Stateful authentication with no token refresh
* Firebase dependency limits self-hosting
* Web UI lacks essential features
* No offline sync on mobile
* Lack of automated testing

## ✅ Goals / Deliverables

1. **Authentication**: Google OAuth + JWT with refresh & expiration
2. **Session Management**: API keys, sync tokens, rate limiting
3. **Sync Logic**: Two-way syncing with Taskchampion Sync Server
4. **Mobile Support**: Background sync and conflict resolution
5. **Web UI**: Task filtering, sorting, bulk editing, IndexedDB cache
6. **Self-Hosting**: Docker Compose setup + deployment scripts
7. **Monitoring**: Add Sentry and log aggregation
8. **Testing**: 90%+ coverage, CI/CD pipeline
9. **Documentation**: Setup, API, and user guides
10. **Stretch Goals**: RSS feeds, push notifications, task history

## 🧱 System Architecture

* React frontend communicates with Go backend using HTTP
* Backend uses utils/tw to call TaskWarrior CLI & Sync Server
* IndexedDB stores local tasks; sync occurs on demand
* Mobile app uses SQLite and syncs via Taskchampion Sync Server

## ⚙️ Self-Hosting Plan

* Use Docker Compose with two services: backend + sync server
* Environment config via `.env`
* Optional NGINX proxy with HTTPS
* Deployable on Oracle Cloud Free Tier

## 🧪 Testing Strategy

* **Unit Tests:** React (Jest), Go (Testify)
* **CI/CD:** GitHub Actions with caching, parallel tests
* **Load Testing:** Use `k6` for backend stress testing (optional)

## 📚 Documentation

* API reference with Swagger
* Deployment, setup, and troubleshooting guides
* Integration guide for mobile
* Weekly blog updates (Medium or similar)

## 💻 My Tech Experience

* Backend: Go, Node.js, REST APIs
* Frontend: React, Redux, IndexedDB, Dexie.js
* Tools: Docker, GitHub Actions, CI/CD
* Contributions to CCExtractor, CCSync, TaskWarrior Flutter, and more

## 🗓️ Timeline

Refer to the [timeline document](./Gsoc%20Timeline%20Ccsync.md) for a detailed week-by-week breakdown.

## 📆 Commitment & Availability

* Final semester ends in May → 40–50 hrs/week available
* No other job/internship planned
* Daily mentor reporting + active participation on Zulip

## 🤝 Why CCExtractor?

My first open-source contributions were to CCExtractor. The welcoming community, interesting projects, and strong mentorship inspired me to go deeper. I’ve been consistently contributing and would love to grow with the org.

## 🛑 Other Organizations

I’m only applying to **CCExtractor** for GSoC 2025.

## 🙏 Final Words

GSoC is a dream opportunity for me to make a meaningful open-source contribution. With my backend strength, frontend experience, and passion for open-source, I believe I can bring CCSync to production readiness with high quality and community impact.

Thank you for reading!
