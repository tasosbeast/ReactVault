# 🧩 Components as Building Blocks

**Tags:** #React #Components #UI #Theory  
**Links:** [[React|What is React]] [[JSX]] [[Props]] [[Component Composition]]

---

## ⚡ Core Idea
In [[React]], **components** are the *fundamental building blocks* of user interfaces.  
Each component represents an **independent, reusable piece** of UI that manages its own structure, style, and behavior.

---

## 💡 Key Points
- Components are like **functions that return UI**.  
- They can be **nested**, **reused**, and **composed** to build complex UIs.  
- Components make the code **modular**, **readable**, and **easy to maintain**.  
- Each component can have its own **[[state]]** and receive **[[props]]** (data).  

---

## 🧱 Types of Components
1. **Functional Components (Modern)**  
   ```jsx
   function Header() {
     return <h1>Welcome!</h1>;
   }
   ```
2. **Class Components (Legacy)**  
   ```jsx
   class Header extends React.Component {
     render() {
       return <h1>Welcome!</h1>;
     }
   }
   ```

---

## 🧩 Visualization
```
App
├── Header
├── Main
│   ├── Search
│   └── Results
└── Footer
```

Each component handles its own small task, together forming the full app.

---

## 🧠 Summary
Components are:  
> “Small, independent pieces of UI that can be combined like Lego blocks to form entire applications.”
