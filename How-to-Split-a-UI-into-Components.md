# 🧩 How to Split a UI into Components

**Tags:** #React #Architecture #Components #Design #UI  
**Links:** [[What-is-Thinking-in-React]] [[Component Composition]] [[Component-Categories]] [[Props]]

---

## ⚡ Core Idea
A React app is built from **small, reusable pieces** called components.  
To split a UI effectively, identify **logical chunks of the interface** — each should handle one job and be reusable across the app.

---

## 💡 Steps to Split a UI

### 1️⃣ Identify Logical Groupings in the Design
- Look for **sections** that repeat or serve a clear purpose.  
- Example: a dashboard might have `Header`, `Sidebar`, `Card`, and `Chart` components.

### 2️⃣ One Responsibility per Component
Each component should do *one thing well*.  
If it grows too large or does multiple jobs, split it further.

### 3️⃣ Reuse Through Composition
If two sections look similar but differ slightly → create one base component and pass data via **props**.

### 4️⃣ Start from the Top, Work Down
Break the UI into a **tree**:
```
App
 ├── Header
 ├── Main
 │    ├── SearchBar
 │    ├── ProductList
 │    └── ProductItem
 └── Footer
```
Each branch can be built independently.

### 5️⃣ Name Components by Role
Names should describe *what* they represent (`UserCard`, `SearchBar`, `ProductRow`) — not *how* they look.

---

## 🔍 Example
From this HTML:
```html
<div class="product">
  <img src="shirt.jpg" />
  <h3>Blue Shirt</h3>
  <p>$29.99</p>
</div>
```

We get this React component:
```jsx
function ProductItem({ product }) {
  return (
    <div className="product">
      <img src={product.image} alt={product.name} />
      <h3>{product.name}</h3>
      <p>{product.price}</p>
    </div>
  );
}
```

---

## 🧩 Visualization
```
Big UI → Logical Sections → Components → Props → Composition
```

---

## 🧠 Summary
Splitting a UI into components means:  
> “Find repeating patterns, isolate responsibilities, and let each component own one clear purpose.”
