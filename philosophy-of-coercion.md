# Philosophy of Coercion

You don't deal with these types of conversion corner vases by avoiding coercions, not only on JS but on any language. We must adopt a coding style that makes value types plain and obvious.

A quality JS program embraces coercions, making sure the types involved in every operation are clear. Thus, corner cases are safely managed.

> Javascript's dynamic typing is not a weakness, it's one of its strong qualities

Part of the reason JS has such a low barrier to entry is that it doesn't force the reader to deal with a bunch of unnecessary detail.

<figure><img src=".gitbook/assets/Screen Shot 2023-01-14 at 23.20.28.png" alt=""><figcaption><p>Do i really need to say that im converting the number intro a string on line 4? or do i just go for coercion instead? </p></figcaption></figure>

## Understanding features.

> If a feature is sometimes useful and sometimes dangerous and if there is a better option then akways use the better option.

* Useful: when the reader is focused on what's important.
* Dangerous: when the reader can't tell what will happen.
* Better: when the reader understands the code.

It is _irresponsible_ to knowingly avoid the usage of a feature that can _**improve code readability**_.
