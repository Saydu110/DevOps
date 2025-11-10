
---

## 💠 `.NET/README.md`
```markdown
# 💠 .NET (ASP.NET Core) Docker Image

This folder contains a multi-stage `Dockerfile` for .NET applications.

## 🧱 Base Images
- `mcr.microsoft.com/dotnet/sdk:7.0` — for building the app.
- `mcr.microsoft.com/dotnet/aspnet:7.0` — for running it.

## 🧰 Build and Run
### 1️⃣ Build:
```bash
docker build -t dotnet-app .
