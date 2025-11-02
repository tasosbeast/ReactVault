# Re-render
The process where React executes a [[component]]'s function again to determine what UI changes need to be made.

* **Triggers:**
    * A change in **[[State]]**.
    * A change in **[[Props]]** received from its parent.
* **Performance:** Unnecessary re-renders are a common cause of performance issues (see **[[Memoization]]**).