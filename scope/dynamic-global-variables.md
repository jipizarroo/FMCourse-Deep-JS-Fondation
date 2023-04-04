# Dynamic Global Variables

{% code lineNumbers="true" %}
```javascript
var teacher = "Kyle"

function otherClass(){
    teacher = "Suzy";
    topic = "React";
    console.log("Welcome");
}

otherClass();     // Welcome!
teacher;          // ??
topic;            // ??
```
{% endcode %}

Well, this is a weird JS dynamic, it's there so we must know about it.

After compilation, we have 2 things declared in the global scope ( apart from other things that are already there by default), teacher and our otherClass,

So, at line 9, when we execute our function, we go in, we ask the local function scope for the value teacher and it gives us back "Suzy", we overwrote the declaration that was on line 1.

But something even weirder happens when we ask for "topic", we get a no from both the local scope and the global one ( and this is one of the historical errors about JS ), instead of JS saying, no I don't know this, imma give you an error, what it does is dynamically create a global scope, so now we get the target "topic" with the value React into the global scope.

DO NOT MAKE THIS, THIS IS A BAD THING TO DO, WE DO NOT WANT TO CREATE DYNAMICALLY GLOBAL VARIABLES.&#x20;

### "use strict"

We do the same code, we get to line 7, ask the global scope, do we know "topic" => "nope" ReferenceErrror
