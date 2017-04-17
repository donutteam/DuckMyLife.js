# DuckMyLife.js
A PJAX solution that is simple, so you don't have to **d**ucking hate your life.

# Installation
We do not recommend hacking this into an existing site, because it requires you to take a little different route than usual. We gotcha though fam.

## 1. Reference the library.
Add this in your ``HEAD`` element or to the bottom of your document.
```html
<script type="application/javascript" src="/path/to/DuckMyLife.js"></script>
```
## 2. Add this snippet (or something similar)
This will start DuckMyLife when you're ready to use it, you can add this to a script tag or put it in your favourite JavaScript file.
```js
document.addEventListener("DOMContentLoaded", DuckMyLife.Initialise);

DuckMyLife.AssociateContext("Body", "dml-context"); // (ContextName, ClassName)
DuckMyLife.AssociateContext("Navbar", "dt-nav");
DuckMyLife.AssociateContext("Footer", "footer");
```

## 3. That's about it, client-side.
Yeah, that's really it.

## 4. Optional Extras for the client.

We use [NProgress](http://ricostacruz.com/nprogress/) to show the user that something is happening:
```js
document.addEventListener("DMLPageLoadStarted", NProgress.start);
document.addEventListener("DMLResourceLoaded", NProgress.inc);
document.addEventListener("DMLPageLoaded", NProgress.done);
```
