# Js-EventsContainer [Demo](https://prefect9.github.io/Js-EventsContainer/demo/)
## Examples
```html
<div class="btn" id="btn">CLICK!</div>
```
```javascript
var click_events = new EventsContainer()
    .add(function (arg) {
        alert("Handler #1, seed: "+arg)
    })
    .add(function (arg) {
        alert("Handler #2, seed: "+arg)
    })
document.getElementById("btn").addEventListener("click", function (e) {
    e.preventDefault()
    click_events.trigger(Math.random())
})
```



## API
### Object methods
#### .add(function(...args){ ... })
Add an event handler. Several handlers can be added.

#### .trigger(...args)
Execute event handlers with passed arguments.

#### .clear()
Clear event handlers.