# stack-snippet-console
Creates an output console in the results pane of Stack-Snippets on the StackExchange network.

Notes:
- All calls to `console.log()` are passed along to the actual console
- Loosely imitates Chrome's output (colors and styles excluded)
- An `HTMLElement` will be printed as its `outerHTML`
- Objects are printed using `JSON.stringify()` with an `Object.prototype.toString()` failover
- Works by injecting elements into the page... so, it obviously pollutes the DOM.
- The number of entries is now limited to 50 by default. You can modify this limit by calling `console.config({maxEntries:25})`.
- Now logs unhandled errors.