
Data that a [[component]] manages internally. When this data changes, React automatically triggers a **[[Re-render]]** of the [[component]].

* **Primary Hook:** [[useState]]
* **Golden Rule:** State changes should always be treated as immutable (you replace the old value with a new one, you don't directly modify it).
* **Connections:** Crucial for dynamic UIs. Avoid storing derived values in state.