---
description: '== vs ==='
---

# Equality

\== checks value ( Loose equality)\
\=== checks value and type ( Strict equality)

Welp, this is not right.

JS Spect

Abstract equality comparison ( == )

The comparison x == y, where x and y are values, produces true or false. Such a comparison is performed as follows: \


<figure><img src=".gitbook/assets/Screen Shot 2023-01-19 at 16.32.31.png" alt=""><figcaption><p>As we can see, we instantly de-bunk the first saying in most of the JS devs.</p></figcaption></figure>

Example:&#x20;

<figure><img src=".gitbook/assets/Screen Shot 2023-01-19 at 16.34.33.png" alt=""><figcaption></figcaption></figure>

Strict Equality Comparison ( === )\
The comparison x === y, where x and y are values, produces true or false. Such a comparison is performed as follows:&#x20;

<figure><img src=".gitbook/assets/Screen Shot 2023-01-19 at 16.36.39.png" alt=""><figcaption><p>As on abstract, they both check types.</p></figcaption></figure>



Example 2:

<figure><img src=".gitbook/assets/Screen Shot 2023-01-19 at 16.38.57.png" alt=""><figcaption><p>JS does identity checking when it comes to equality, workshop1 and workshop2, even though, they have the same content in their object, they are not the same object, hence, giving false when checking for equality.</p></figcaption></figure>

So =>&#x20;

\== => Allows coercion ( types different )

\=== => Disallways coercion ( types same )\
\
