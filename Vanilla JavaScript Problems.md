# 🍝 Vanilla JavaScript Problems

**Tags:** #JavaScript #Frontend #React #Theory  
**Links:** [[Why-Do-Front-End-Frameworks-Exist|Why Do Front-End Frameworks Exist]] [[React|What is React]]

---

## ⚡ Core Idea
Building dynamic UIs with **plain JavaScript** quickly becomes messy and error-prone.  
As apps grow, managing the **DOM manually** and keeping it in sync with changing data becomes a nightmare.

---

## 💡 Common Problems

1. **Manual DOM Manipulation**
   - You must manually select, update, and remove elements.  
   - Each change in data requires multiple `querySelector` or `innerHTML` calls.  
   ```js
   document.querySelector("#name").textContent = user.name;
   ```

2. **Data Stored in the DOM**
   - [[State]] often lives in HTML elements themselves, not in structured JS variables.  
   - Makes debugging and scaling difficult.

3. **Spaghetti Code 🍝**
   - Interwoven logic and UI updates.  
   - One small change can break multiple parts of the app.

4. **Hard to Reuse and Maintain**
   - No clear structure or modularization.  
   - Adding features increases complexity exponentially.

---

## 🧩 Visualization
```
Data ↔ DOM ↔ Event Handlers ↔ UI Updates  (tangled cycle)
```

React solves this by introducing **[[state]]**, **virtual DOM**, and **declarative components** — breaking the cycle.

---

## 🧠 Summary
Vanilla JS problems can be summed up as:  
> “Too much manual control, not enough abstraction. React brings order to the chaos.”
