
---

## 🦫 `go/README.md`
```markdown
# 🦫 Go Docker Image

This folder contains a `Dockerfile` for a Go application using multi-stage builds.

## 🧱 Base Image
- `golang:1.21-alpine` (for build)
- `scratch` (for runtime)

## 🧰 Build and Run
### 1️⃣ Build:
```bash
docker build -t go-app .
