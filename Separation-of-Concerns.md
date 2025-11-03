# 🧩 Separation of Concerns in [[React]]

**Tags:** #React #Architecture #BestPractices #JSX  
**Links:** [[JSX]] [[Components]] [[Props]] [[State]]

---

## ⚡ Core Idea
In traditional web development, **Separation of Concerns** means splitting HTML, CSS, and JS into different files.  
[[React]] challenges this idea — instead, it groups **logic and UI together by component**, not by file type.

---

## 💡 Key Points
- [[React]]’s philosophy: group code that **belongs together** logically.  
- Each component contains **its own structure (JSX)**, **style**, and **behavior (logic/[[state]])**.  
- This makes [[components]] **self-contained** and **reusable**.  

---

## 🔍 Example
**Traditional (by file type):**
```
index.html
style.css
script.js
```
**[[React]] (by concern):**
```
Button.jsx  → JSX + logic + styles
Card.jsx    → JSX + logic + styles
```

**Example:**
```jsx
function Button({ label }) {
  return <button className="btn">{label}</button>;
}
```

---

## 🧠 Why It Works
- UI logic and markup are **tightly connected**, so it makes sense to keep them in one place.  
- Improves **readability**, **maintainability**, and **scalability**.  

---

## 🧠 Summary
[[React]] redefines Separation of Concerns as:  
> “Put things that change together in the same place — [[components]], not file types.”
