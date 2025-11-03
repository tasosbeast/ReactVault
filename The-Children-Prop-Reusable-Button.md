# 🧒 The children Prop: Making a Reusable Button

**Tags:** #React #Props #Components #Children #Reusability  
**Links:** [[Components]] [[Props]] [[Component Composition]] [[State-vs-Props|State vs Props]]

---

## ⚡ Core Idea
The **children prop** is a special built-in prop in React that lets you pass **content between opening and closing component tags**.  
It’s what makes components **truly reusable and composable**.

---

## 💡 Key Points
- Every React component automatically receives a `children` prop.  
- Whatever you put **inside** the component’s tags becomes the `children` value.  
- Use it to wrap content, not to configure logic.  

---

## 🔍 Example — Reusable Button
```jsx
function Button({ children, onClick }) {
  return (
    <button className="btn" onClick={onClick}>
      {children}
    </button>
  );
}

function App() {
  return (
    <div>
      <Button onClick={() => alert("Clicked!")}>Click Me</Button>
      <Button>Cancel</Button>
    </div>
  );
}
```
Here, `"Click Me"` and `"Cancel"` are passed as `children`.

---

## 🧩 Visualization
```
<Button>Click Me</Button>  →  children = "Click Me"
<Button><Icon /> Save</Button>  →  children = [<Icon />, "Save"]
```

You can pass **text**, **HTML elements**, or even **other components** as children.

---

## 🧠 Summary
The `children` prop enables React’s composability:  
> “It lets components wrap any content — making them flexible, elegant, and reusable.”
