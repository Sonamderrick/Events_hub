# Practical IV - Quick Check Answers

### Q1: If validate.js runs BEFORE main.js and calls a function defined only in main.js, what error appears in the Console?
**Answer:** `Uncaught ReferenceError: [functionName] is not defined`. This occurs because JavaScript executes scripts synchronously line by line, so a function cannot be called before the file defining it has been loaded and parsed by the browser.

### Q2: Uncomment document.write() after the page has fully loaded (or paste it in Console). What happens to the page? Why is innerHTML safer for updates?
**Answer:** `document.write()` erases the entire current document and overwrites it with the new content. `innerHTML` is much safer because it updates only the content inside a specific target element without destroying the rest of the existing page structure or DOM.

### Q3: Click Cancel on the confirm dialog. Does the form clear? Which method call stopped the default action?
**Answer:** No, the form does not clear. The `e.preventDefault()` method call inside the event listener stopped the browser's default form reset action.

### Q4: Paste console.log(b) after an if { let b=2; } block. What error do you get, and what does that prove about let? Also write typeof null.
**Answer:** It throws `Uncaught ReferenceError: b is not defined`. This proves that variables declared with `let` are block-scoped and only exist inside the nearest `{}` block where they are declared. `typeof null` evaluates to `"object"`.

### Q5: Change Inter-College Football seats from 0 to 5 in the events array and reload. What happens to the card and the Register button?
**Answer:** The badge changes from grey "Sold out" to green "5 seats", the status text updates to "Filling fast!", and the greyed-out "No seats left" text is replaced with an active blue "Register" button.

### Q6: What does seatsMessage(0) return? What does seatsMessage(12) return?
**Answer:** 
- `seatsMessage(0)` returns `"Sold out"`.
- `seatsMessage(12)` returns `"Filling fast!"`.

### Q7: Submit the form with an empty email. Which line stops the browser from leaving the page? What would happen without e.preventDefault()?
**Answer:** `e.preventDefault()` stops the browser from leaving or reloading the page. Without `e.preventDefault()`, the browser would immediately submit the form to the server action URL and reload the page, causing all validation error messages on the screen to disappear instantly.

### Q8: Is document.querySelectorAll("nav a") a NodeList or an HTMLCollection? Does forEach work on it in modern browsers?
**Answer:** It returns a `NodeList`. Yes, `forEach()` works directly on a `NodeList` in all modern web browsers.