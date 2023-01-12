# Boxing

How is it that we access the value on `studentNameElem.length > 50  => Boxing.`

It's a form of explicit coercion in spirit => You have this thing that is not an object and you are trying to use it as if it is an object, me, JS, I'm gonna make it into an object for you.

{% hint style="info" %}
This Boxing method could be one of the main reasons why people say everything in JS is an object.

But this is not an object, it can behave like one, but it's not one => It is a primitive string that has an optimization in it where you can access a property as if it where an object.
{% endhint %}
