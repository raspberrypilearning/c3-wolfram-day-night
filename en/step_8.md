## Challenge: Building a Tooltip

If you are using Wolfram in a desktop application, rather than in a browser, try to use a `Tooltip` instead of a `Dynamic` sentence to show information about the country. A `ToolTip` allows the user to hover their mouse over the country, and see the information in a little box.

`ToolTip` takes two arguments: the object the user will hover over (the `Polygon`), and the information the user will see when they hover (the `If` statement with `Daytime` and `Nighttime` information).

--- hints---

--- hint ---

You can use the same code for your `If` statement as you did in the main project.


--- /hint---
--- hint---

`ToolTip` needs to go around `Polygon[x]`. `Polygon[x]` should be the first argument in `ToolTip`, followed by your `If` statement.

--- /hint---

---/hints---