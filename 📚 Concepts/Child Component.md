A child [[component]] is a [[component]] that’s **rendered inside another [[Parent Component | parent component]]**.  
The parent can **pass data down** using **[[props]]**.

**example**

```jsx
function Child({ message }) {
  return <p>{message}</p>;
}

function Parent() {
  return <Child message="Hello from the parent!" />;
}
```

**Mental model**  
Think of the parent as the _caller_ and the child as the _callee_.  
The parent decides **what to show** and **what data to send**, while the child decides **how to display it**.

**Key idea**
- Data flows **downward** (Parent → Child) via [[props]].
    
- Children can trigger changes _upward_ through callbacks passed as [[props]].
