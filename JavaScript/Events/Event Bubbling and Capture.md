**Bubbling** - When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

<style> body * { margin: 10px; border: 1px solid blue; } </style> 
<form onclick="alert('form')">FORM 
	<div onclick="alert('div')">DIV 
		<p onclick="alert('p')">P</p> 
	</div>
 </form>
First event will be called  p, after div and the last one form.

**Event capturing** is the event starts from top element to the target element.  It is rarely used in real code, but sometimes can be useful.
Caputres from the HTML where you clicked and storing elemetns.
Bubbling triggering the captured elements.

In the **capturing** phase:

-   The browser checks to see if the element's outer-most ancestor ([`<html>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/html)) has a `click` event handler registered on it for the capturing phase, and runs it if so.
-   Then it moves on to the next element inside `<html>` and does the same thing, then the next one, and so on until it reaches the direct parent of the element that was actually selected.
In the **target** phase:

-   The browser checks to see if the [`target`](https://developer.mozilla.org/en-US/docs/Web/API/Event/target "target") property has an event handler for the `click` event registered on it, and runs it if so.
-   Then, if [`bubbles`](https://developer.mozilla.org/en-US/docs/Web/API/Event/bubbles "bubbles") is `true`, it propagates the event to the direct parent of the selected element, then the next one, and so on until it reaches the `<html>` element. Otherwise, if [`bubbles`](https://developer.mozilla.org/en-US/docs/Web/API/Event/bubbles "bubbles") is `false`, it doesn't propagate the event to any ancestors of the target.

In the **bubbling** phase, the exact opposite of the **capturing** phase occurs:

-   The browser checks to see if the direct parent of the element selected has a `click` event handler registered on it for the bubbling phase, and runs it if so.
-   Then it moves on to the next immediate ancestor element and does the same thing, then the next one, and so on until it reaches the `<html>` element.

Handlers added using `on<event>`-property or using HTML attributes or using two-argument `addEventListener(event, handler)` don’t know anything about capturing, they only run on the 2nd and 3rd phases.

To catch an event on the capturing phase, we need to set the handler `capture` option to `true`:

elem.addEventListener(..., {capture: true}) 
// or, just "true" is an alias to {capture: true} 
elem.addEventListener(..., true)

The standard [DOM Events](http://www.w3.org/TR/DOM-Level-3-Events/) describes 3 phases of event propagation:

1.  Capturing phase – the event goes down to the element.
2.  Target phase – the event reached the target element.
3.  Bubbling phase – the event bubbles up from the element.

[[Event Delegation]]