# 🧩 What is “Thinking in React”?

**Tags:** #React #Architecture #Components #StateManagement #DesignThinking  
**Links:** [[State-vs-Props|State vs Props]] [[Components]] [[Component Composition]] [[Props|Props Immutability and One-Way Data Flow]]

---

## ⚡ Core Idea
“Thinking in React” means designing your UI around **components**, **data flow**, and **state management** — instead of HTML pages or templates.  
It’s a mindset: break complex UIs into simple, reusable, and state-driven parts.

---

## 💡 The 5 Steps of Thinking in React

1. **Break the UI into a Component Hierarchy**
   - Identify logical, reusable pieces of UI.  
   - Example:
     ```
     App
     ├── SearchBar
     ├── ProductTable
     │   ├── ProductCategoryRow
     │   └── ProductRow
     ```

2. **Build a Static Version (no state yet)**
   - Just use props to pass data down.  
   - Focus on layout and structure.

3. **Identify the Minimal Representation of State**
   - Ask: *What data changes?* and *where should it live?*  
   - Keep only essential, changing data in state.

4. **Identify Where State Should Live**
   - If multiple components need the same data → **lift state up** to their common ancestor.  
   - Example: search filter shared by SearchBar and ProductTable.

5. **Add Inverse Data Flow**
   - Pass event handlers (functions) down to children via props so they can communicate changes back up.

---

## 🧩 Visualization
```
Data (state ↑) → Props (↓) → UI Components (render)
                 ↑ Events (callbacks)
```
One-way data flow keeps everything predictable.

---

## 🧠 Summary
Thinking in React means:  
> “Design components around data flow, not around pages — state goes up, props go down.”
