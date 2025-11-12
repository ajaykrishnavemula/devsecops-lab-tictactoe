# End-to-End DevSecOps Implementation : Tic-Tac-Toe🎮

> A complete **DevSecOps pipeline** integrating **GitHub Actions, Trivy, Docker, Kubernetes, and Argo CD** — built around a simple React Tic Tac Toe app to demonstrate *secure CI/CD automation from code to deployment*.  
The core idea: **every commit → test → analyze → build → secure → deploy automatically!**

![Screenshot 2025-03-04 at 7 16 48 PM](https://github.com/user-attachments/assets/7ed79f9c-9144-4870-accd-500085a15592)


---

## 🔐 DevSecOps Workflow

### 🧱 Continuous Integration (GitHub Actions)
1. ✅ **Run Unit Tests** – Validate app logic & ensure reliability  
2. 🔍 **Static Code Analysis (Lint)** – Enforce clean, secure, and maintainable code  
3. ⚙️ **Build and Upload Artifact** – Bundle the frontend build  
4. 🐳 **Docker Build & Scan** –  
   - Build Docker image  
   - Scan for vulnerabilities with **Trivy** 🛡️  
   - Push to **GitHub Container Registry (GHCR)**  
5. 🧾 **Update Kubernetes Manifests** –  
   - Update image tag in `/kubernetes` manifests  



### ☸️ Continuous Delivery (Argo CD)
- **Argo CD monitors** the `/kubernetes` folder  
- On manifest updates → syncs desired state → **deploys automatically** to Kubernetes cluster  
- Ensures **GitOps-based delivery** 🔄  


---

## 🧩 Tech Stack

| Domain                         | Tools & Technologies                 |
|--------------------------------|--------------------------------------|
| 💻 **Source Control**          | GitHub                               |
| ⚙️ **CI Pipeline**             | GitHub Actions                       |
| 🧪 **Testing**                 | Jest / React Testing Library         |
| 🔍 **Static Code Analysis**    | ESLint                               |
| 🐳 **Containerization**        | Docker                               |
| 🛡️ **Vulnerability Scanning**  | Trivy                                |
| 📦 **Image Registry**          | GitHub Container Registry (GHCR)     |
| ☸️ **Deployment**              | Kubernetes                           |
| 🚢 **Continuous Delivery**     | Argo CD                              |
| 🧠 **Language & UI**           | React 18 + TypeScript + TailwindCSS  |

---

## 🚀 Project Overview

This project showcases an **end-to-end DevSecOps pipeline** implementing security, automation, and continuous delivery principles using a real-world workflow.  

![image](https://github.com/user-attachments/assets/5b2813a5-f493-4665-8964-77359b5be93a)


## 🌈 Application Features

- 🎮 Interactive Tic Tac Toe gameplay  
- 📊 Real-time score tracking  
- 🕒 Game history with timestamps  
- 🏆 Highlights winning moves  
- 🔁 Reset and replay options  
- 📱 Fully responsive design  


## 🧱 Project Structure

```bash
src/
├── components/
│   ├── Board.tsx       # Game board component
│   ├── Square.tsx      # Individual square component
│   ├── ScoreBoard.tsx  # Score tracking component
│   └── GameHistory.tsx # Game history component
├── utils/
│   └── gameLogic.ts    # Core game logic
├── App.tsx             # Main app component
└── main.tsx            # Entry point
kubernetes/
├── deployment.yaml
└── service.yaml
.github/
└── workflows/
    └── ci-cd.yml
```

## ⚖️ Game Logic Summary

- X always starts ✅  
- First to align 3 marks (row, column, diagonal) wins 🎉  
- Draw declared if all squares filled with no winner 🤝  
- Winning rows are highlighted for clarity 🔆  
- Tracks and displays live game statistics 📈  

---

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ajaykrishnavemula/devsecops-lab-tictactoe.git
   cd devsecops-lab-tictactoe
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn
   ```

3. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open your browser and navigate to `http://localhost:5173`

## Building for Production

To create a production build:

```bash
npm run build
# or
yarn build
```

The build artifacts will be stored in the `dist/` directory.

---

## 🔑 Skills Demonstrated

- 🔄 CI/CD with GitHub Actions  
- 🐳 Containerization & security scanning (Trivy)  
- 🔐 Shift-left security practices (Linting + scanning)  
- ☸️ Kubernetes deployments via GitOps (Argo CD)  
- 📜 Infrastructure as Code (Kubernetes YAML manifests)  
- 💡 Automated deployment with continuous feedback loop  


Thank you for exploring this project! Feel free to reach out or contribute. 🌟

