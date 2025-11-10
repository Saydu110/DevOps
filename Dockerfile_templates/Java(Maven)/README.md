
---

## ☕ `java/README.md`
```markdown
# ☕ Java (Maven) Docker Image

This folder contains a multi-stage `Dockerfile` for a Java project built using Maven.

## 🧱 Base Images
- `maven:3.9.0-eclipse-temurin-17` (for build)
- `eclipse-temurin:17-jre` (for runtime)

## 🧰 Build and Run
### 1️⃣ Build:
```bash
docker build -t java-app .
