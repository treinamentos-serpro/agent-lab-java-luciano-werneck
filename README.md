🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

# Soc Ops 🎯

Build a playful **Social Bingo** web app while learning modern **GitHub Copilot agent workflows**.

Find people who match bingo prompts, mark cards in real time, and race to 5 in a row.

🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

[🎮 Live Demo](https://copilot-dev-days.github.io/agent-lab-java/) • [📚 Lab Guide](workshop/GUIDE.md) • [📖 Workshop Docs](docs/)

---

## Why this project?

- Learn by building a complete Java + Spring Boot app
- Practice context engineering and multi-agent development
- Deliver visible, interactive frontend improvements quickly

---

## 🚀 Quick Start

### Prerequisites
- [Java 21 JDK](https://adoptium.net/) or higher
- [Apache Maven 3.9+](https://maven.apache.org/) (or use the included Maven Wrapper)

### Run locally
```bash
cd socops
./mvnw spring-boot:run
```

Open: http://localhost:8080

### Build and test
```bash
cd socops
./mvnw clean package
./mvnw test
```

---

## 📚 Lab Journey

| Part | Title |
|------|-------|
| [**00**](workshop/00-overview.md) | Overview & Checklist |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering |
| [**02**](workshop/02-design.md) | Design-First Frontend |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development |

> 📝 Prefer offline reading? Use the [`workshop/`](workshop/) folder.

---

Deploys automatically to GitHub Pages on push to `main`.
