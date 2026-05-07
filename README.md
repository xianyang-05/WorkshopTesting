# 🛠️ Workshop Handbook: Building DailyFit with Antigravity & MCP

Welcome to the **DailyFit** workshop! This handbook will guide you through the journey of building a premium, AI-powered fitness tracking application from scratch using the modern agentic stack.

---

## 📋 Part 1: Prerequisites

Before we begin, make sure you have the following tools installed or prepared.

### 1. Node.js Installation
Node.js is required to run development tools and manage dependencies.
- **Download**: Visit [nodejs.org](https://nodejs.org/) and install the **LTS version**.
- **Verify installation**:
  ```bash
  node -v
  # Sample Output: v22.14.0
  npm -v
  # Sample Output: 11.2.0
  ```

### 2. Antigravity Installation
Antigravity is the AI coding workspace used in this workshop.
- **Make sure**:
  - Antigravity is installed
  - You are logged in
  - You have access to the required AI models

### 3. Docker Desktop Installation
Docker is needed to run some MCP servers locally, especially GitHub MCP.
- **Download**: Install [Docker Desktop](https://www.docker.com/products/docker-desktop/) for your operating system.
- **Make sure**:
  - Docker Desktop is installed
  - Docker Desktop is running before connecting GitHub MCP
  - Docker is using Linux containers
- **Verify installation**:
  ```bash
  docker --version
  # Sample Output: Docker version 27.3.1, build ce12230
  ```
- **Verify Docker engine is running**:
  ```bash
  docker info
  ```
> [!TIP]
> If `docker info` shows an error, open Docker Desktop and wait until it is fully running.

### 4. Accounts Required
Please sign in or create accounts for:
- [Stitch](https://stitch.withgoogle.com/)
- [Firebase](https://console.firebase.google.com/)
- [GitHub](https://github.com/)

### 5. Recommended Preparation
Before the workshop, prepare:
- A website URL for UI design reference
- A simple app idea
- A GitHub repository name
- Access to your Google account for Firebase and Stitch

---

## 🚀 Part 2: Step-by-Step Implementation

### 💡 Overview
In this workshop, participants will build a web app using:
- **Stitch** — to design the frontend UI
- **Antigravity** — to build the app from the Stitch design
- **Stitch MCP** — to let Antigravity access the Stitch project
- **Firebase MCP** — to set up authentication
- **GitHub MCP** — to push and manage the project code

> [!IMPORTANT]
> **The only required condition**: The app must include an authentication page with Sign In and Sign Up.

---

### Phase 1: Choose Your App Idea
Before opening Stitch, choose a simple app idea. Your app should include at least:
1. Landing page
2. Authentication page (Sign In/Up)
3. Dashboard page

---

### Phase 2: Build Frontend Design with Stitch

#### 1. Open Stitch
Open Stitch in your browser and sign in with your Google account.

#### 2. Create a new Stitch project
Create a new project using your app name (e.g., `DailyFit`).

#### 3. Paste a website URL as design reference
Paste a website URL that has the UI style you want to follow (e.g., `https://glaido.com/`). Stitch uses this for:
- Layout style & Spacing
- Color theme & Typography
- Card and Button design

#### 4. Use this prompt in Stitch
> "Create a modern web app called **[Your App Name]** based on the UI style of the website URL I provided. The app is for **[briefly describe your app idea]**. Include 3 main pages: Landing, Authentication (Sign In/Up), and Dashboard. The app should feel clean and consistent."

#### 5. Refine the design
Make the design cleaner and more premium. Improve the spacing, buttons, cards, and page consistency. **Keep the Stitch project open** for the next steps.

---

### Phase 3: Open Project Folder in Antigravity

#### 1. Create a new folder
Create a folder on your computer using your app name (e.g., `C:\Users\User\Documents\DailyFit`).

#### 2. Open Antigravity
Launch the Antigravity application.

#### 3. Open the project folder
In Antigravity: `File` → `Open Folder` → Select your project folder.

---

### Phase 4: Connect Stitch MCP with Antigravity

#### 1. Get Stitch API key
In Stitch: `Settings` → `API Keys` → `Create API Key`. Copy it (keep it private!).

#### 2. Connect Stitch MCP
In Antigravity: `MCP Servers` → `Add Stitch MCP` → Paste API Key → `Connect`.

#### 3. Test Connection
Ask Antigravity: *"List my Stitch projects."*
If you see your project name in the list, the MCP is connected successfully!

---

### Phase 5: Build UI from Stitch Design

#### 1. Build the app UI
Prompt Antigravity:
> "Use my Stitch design as the visual reference.Build the UI for [Project Name] based on the Stitch design.Match the Stitch UI style and add working navigation between the pages."

#### 2. Improve Interaction
Ask Antigravity to refine buttons:
- "Get Started" → Auth Page
- Switch between Sign In/Up
- Login → Dashboard
- Logout → Landing Page

#### 3. Preview the app
Run the app and verify all pages and navigation.

---

### Phase 6: Connect Firebase MCP

#### 1. Create and Configure Firebase project
- Go to [Firebase Console](https://console.firebase.google.com/) and create a project (e.g., `DailyFit`).
- **Enable Email/Password Auth**:
  - Go to **Authentication** → **Get Started**.
  - Under **Sign-in method**, choose **Email/Password**.
  - Toggle **Enabled** and click **Save**.

#### 2. Connect Firebase MCP
In Antigravity: `MCP Servers` → `Add Firebase MCP` → Connect your account.

#### 3. Install Firebase Tools
In the terminal:
```bash
npm install -g firebase-tools
firebase login
```

#### 4. Set up Authentication
Prompt Antigravity:
1. *"List my Firebase projects."*
2. *"Use my **[Your Firebase Project Name]** to set up email/password authentication. Connect the forms, handle redirects to the dashboard after login, and add a logout function."*

#### 5. Test & Verify
Sign up in your app, then check the **Users** tab in your Firebase Console to see the new entry.

---

### Phase 7: Connect GitHub MCP

#### 1. Prepare Docker
Ensure **Docker Desktop** is running and using Linux containers.
```bash
docker info
```

#### 2. Create GitHub Repo & Token
- Create a new repo on GitHub.
- Generate a **Fine-grained token** with `Contents: Read/Write` and `Metadata: Read-only` permissions.

#### 3. Connect GitHub MCP
In Antigravity: `MCP Servers` → `Add GitHub MCP` → Paste Token → `Connect`.

#### 4. Push the project
Prompt Antigravity:
> "Use GitHub MCP to connect this project to my GitHub repository. Initialize Git, commit everything, and push to main with message 'Initial commit: app UI with Firebase authentication'."

---

## 🎯 Summary
By the end of this workshop, you have successfully built a full-stack application using an **Agentic Workflow**. You've moved from a simple text prompt to a live, authenticated, and version-controlled project!

---
*Happy Coding!* 🚀