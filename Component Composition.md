# 🧱 Component Composition

**Tags:** #React #Components #Composition #Reusability #Architecture  
**Links:** [[Components|Components as Building Blocks]] [[The-Children-Prop-Reusable-Button|The Children Prop Reusable Button]] [[Props|Props Immutability and One-Way Data Flow]] [[State-vs-Props|State vs Props]]

---

## ⚡ Core Idea
**Composition** means combining small, focused components to build more complex UIs.  
In React, you don’t inherit behavior — you **compose** it by nesting and passing props or children.

---

## 💡 Key Principles
- **Small, reusable parts** → one component per concern.  
- Components can **contain** or **wrap** others.  
- Avoid deep inheritance hierarchies — React favors **composition over inheritance**.  

---

## 🔍 Example — Card Composition
```jsx
function Card({ title, children }) {
  return (
    <div className="card">
      <h2>{title}</h2>
      <div className="content">{children}</div>
    </div>
  );
}

function App() {
  return (
    <Card title="Hello World">
      <p>This content is passed via children!</p>
    </Card>
  );
}
```

Here, `Card` provides structure, while `children` provides dynamic content.

---

## ⚙️ Variants Through Composition
Instead of multiple component types, use composition for variation:  
```jsx
<Card title="User">
  <Avatar />
  <UserDetails />
</Card>
```

This keeps your UI modular and adaptable.

---

## 🧩 Visualization
```
App
 ├── Card
 │    ├── Avatar
 │    └── UserDetails
 └── Footer
```

Each piece does one job well — combined, they form a complete interface.

---

## 🧠 Summary
Composition is React’s design secret:  
> “Build bigger things by assembling smaller ones — not by rewriting them.”
