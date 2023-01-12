# Abstract Operations

**JS spec:**\
\
_**Abstract operations:**_\
These operations are not part of the ECMAScript language; they are defined here solely to aid the specification of the semantics of the ECMAScript language. Other, more specialized abstract operations are defined throughout this specification.

_**Type conversion:**_\
The ECMAScript language implicitly performs automatic type conversion as needed. To clarify the semantics of certain constructs it is useful to define a set of conversion abstract operations. The conversion abstract operations are polymorphic; they can accept a value of any ECMAScript language type. But no other specification types are used with these operations.



ToPrimitive(hint) => If we have something non-primitive, like one of the object types ( object, array, function, etc. ), and we need to make it into a primitive, this is the abstract operation that's going to be involved in doing that.

{% hint style="info" %}
Abstract operations are not a function that the JS engine could somehow call, they may, in fact, be actual methods inside the JS engine, conceptual operations.
{% endhint %}

What does the hint mean in this? => In other words, if you have something that is not primitive tell me what you think you would like, and what kind of type you would like it to be.

{% hint style="info" %}
The algorithms within JS are inherently recursive.\
If the return result from ToPrimite is not a primitive ( another non-primitive), then it's gonna get evoked again and it's gonna keep getting invoked until we can get something that's a primitive or an error.
{% endhint %}

The way it works:

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 11.05.45.png" alt=""><figcaption></figcaption></figure>

### ToString

It takes any value and gives us the representation of that value in a string form.

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 11.09.15.png" alt=""><figcaption></figcaption></figure>

If we call the ToString(object) => under the hood it does the following => ToPrimitive(string)

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 11.11.15.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 11.12.51.png" alt=""><figcaption></figcaption></figure>

### ToNumber

Anytime we need to do something numeric and we don't have a number, we invoke the ToNumber

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 12.10.35.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 12.12.40.png" alt=""><figcaption></figcaption></figure>

So when we use ToNumber on non-primitive that's not a string, it invokes the ToPrimitive with the hint number.

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 12.14.48.png" alt=""><figcaption><p>This will always produce a primitive string</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 12.16.10.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 12.17.13.png" alt=""><figcaption></figcaption></figure>

### ToBoolean

Anytime you have any value that is not a Boolean, and it's used in a place that needs a Boolean, this operation occurs.

&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-12 at 16.15.56.png" alt=""><figcaption><p>If its not on the "Flasy" list, it is always a "Truthy", thouse on the "Truthy" list are some examples of it.</p></figcaption></figure>

When we do the ToBoolean, there is no coercion stuff happing, it just looks on this table to see if it's on the Falsy list, meaning that an empty object is a Truthy.
