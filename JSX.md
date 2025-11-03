# 🧠 What is JSX?

**Tags:** #React #JSX #Syntax #Frontend  
**Links:** [[Components|Components as Building Blocks]] [[Props]] [[Separation-of-Concerns|Separation of Concerns]] [[Rendering]] 

---

## ⚡ Core Idea
**JSX** stands for **JavaScript XML**.  
It’s a **declarative syntax** that lets you write HTML directly *inside* JavaScript — [[React]] then compiles it to efficient JavaScript code.

---

## 💡 Key Points
- JSX combines **HTML + JavaScript logic** in one place.  
- It makes UI structure easier to visualize.  
- Under the hood, JSX is converted into **React.createElement()** calls.  
- JSX can include **expressions** inside `{ }` braces.  

---

## 🔍 Example
```jsx
function Welcome({ name }) {
  return <h1>Hello, {name}!</h1>;
}
```

This compiles to:
```js
React.createElement("h1", null, "Hello, ", name, "!");
```

---

## ⚠️ Rules of JSX
1. Must have **one parent element**.  
2. Use **camelCase** for attributes (`className`, not `class`).  
3. JS expressions go inside `{ }`.  
4. You can’t use `if` directly inside JSX — use **ternaries** or **logical &&**.

```jsx
{isLoggedIn ? <User /> : <Login />}
```

---

## 🧩 Visualization
```
JSX → React.createElement() → Virtual DOM → Real DOM → UI
```

---

## 🧠 Summary
JSX is:  
> “A syntax extension that lets you write UI like HTML inside JavaScript — making [[React]] both expressive and declarative.”



# 📜 The Rules of JSX

---

## ⚡ Core Idea
JSX looks like HTML, but it’s actually **syntactic sugar for JavaScript**.  
To make it work properly, React enforces specific rules that ensure your UI code compiles cleanly and behaves predictably.

---

## 💡 Main Rules of JSX

1. **One Parent Element**  
   Every JSX block must return a **single parent element**.  
   ```jsx
   // ✅ Correct
   return (
     <div>
       <h1>Hello</h1>
       <p>World</p>
     </div>
   );
   ```
   ```jsx
   // ❌ Wrong
   return (
     <h1>Hello</h1>
     <p>World</p>
   );
   ```

2. **Use camelCase for Attributes**  
   JSX attributes follow JS naming conventions:  
   `className`, `onClick`, `tabIndex` instead of `class`, `onclick`, `tabindex`.

3. **JS Expressions Inside { }**  
   Insert dynamic content using curly braces:  
   ```jsx
   <p>{user.name}</p>
   ```

4. **No if/else Statements Inside JSX**  
   Use **ternary operators** or **logical &&** instead.  
   ```jsx
   {isLoggedIn ? <Dashboard /> : <Login />}
   ```

5. **Close All Tags**  
   Both HTML and custom components must be closed: `<img />`, `<Button />`.

---

## 🧩 Visualization
```
(JSX) → React.createElement() → Virtual DOM → UI
```

JSX is just syntax — the rules keep it consistent and machine-readable.

---

## 🧠 Summary
JSX Rules exist because:  
> “It’s not HTML — it’s JavaScript disguised as HTML, so it follows JS logic and structure.”
