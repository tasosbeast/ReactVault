# 🧰 Setting Up a New [[React]] Project: The Two Options

**Tags:** #React #Setup #Vite #CRA #ProjectSetup  
**Links:** [[React|What is React]] [[Components|Components as Building Blocks]] [[React Ecosystem]]

---

## ⚡ Core Idea
There are **two main ways** to start a new [[React]] project:  
either use **Vite** (modern, fast build tool) or **Create React App (CRA)** (older, official starter).

---

## 💡 Option 1: Vite (Recommended 🚀)
- Super fast dev server and build system.  
- Supports modern JS (ESM) and hot module replacement.  
- Lightweight setup.

**Command:**
```bash
npm create vite@latest my-app -- --template react
cd my-app
npm install
npm run dev
```

---

## 💡 Option 2: Create [[React]] App (Legacy)
- Official Facebook starter template.  
- Includes Webpack setup under the hood.  
- Heavier and slower than Vite, but still fine for beginners.

**Command:**
```bash
npx create-react-app my-app
cd my-app
npm start
```

---

## 🧩 Visualization
```
Vite → Modern, fast dev experience
CRA  → Legacy, simple starter setup
```

---

## 🧠 Summary
[[React]] projects can be set up using either:
> “Vite for speed and flexibility, or Create React App for simplicity.”

Most developers today choose **Vite**.  
