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


<figure><img src="../.gitbook/assets/Screen Shot 2023-01-19 at 16.32.31.png" alt=""><figcaption><p>As we can see, we instantly de-bunk the first saying in most of the JS devs.</p></figcaption></figure>

Example:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-19 at 16.34.33.png" alt=""><figcaption></figcaption></figure>

Strict Equality Comparison ( === )\
The comparison x === y, where x and y are values, produces true or false. Such a comparison is performed as follows:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-19 at 16.36.39.png" alt=""><figcaption><p>As on abstract, they both check types.</p></figcaption></figure>



Example 2:

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-19 at 16.38.57.png" alt=""><figcaption><p>JS does identity checking when it comes to equality, workshop1 and workshop2, even though, they have the same content in their object, they are not the same object, hence, giving false when checking for equality.</p></figcaption></figure>

So =>&#x20;

\== => Allows coercion ( types different )

\=== => Disallways coercion ( types same )



### Double equals Algorithm.

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-22 at 13.17.29.png" alt=""><figcaption></figcaption></figure>

By understanding that the == prefers to do numeric coercion, we can understand the behavior.

Example:&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-22 at 13.20.10.png" alt=""><figcaption><p>Line 4 its pretty useless when we have the double equals algorithim in JS.</p></figcaption></figure>

A bad coercion example ( Even when it works) =>&#x20;

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-22 at 13.26.05.png" alt=""><figcaption><p>This is something you should never code, even though it works why would you try to compare a number to an array??</p></figcaption></figure>

\
The most important learning about this example is not that you should use === here, is the fact that you should never ever program something like this, to fix the root problem, which is why would you try to compare a number to an array with numbers.\


### Summary of double equals =>&#x20;

If the types are the same: ===

If null or undefined: equal

If non-primitives: ToPrimitive

Prefers: ToNumber

### == Corner Cases

<figure><img src="../.gitbook/assets/Screen Shot 2023-01-22 at 13.35.26.png" alt=""><figcaption><p>The algorithm in line 4 is been faced with a bogus corner case, something that should never ever happen in your code.<br>In line 13, we are effectively doing an identity question, so yeah, this is something we could use in real code.</p></figcaption></figure>



<figure><img src="../.gitbook/assets/Screen Shot 2023-01-22 at 13.41.07.png" alt=""><figcaption><p>Line 9 and 16 are cases that we should never ever do, we dont need coercion in here, we just need to convert to boolean.</p></figcaption></figure>

#### Avoid corner cases:

* \== with 0 or "" (or even " ")
* \== with non-primitives
* \== true or == false: allow ToBoolean or use ===

#### The case for preferring ==

Knowing types is always better than not knowing them.

Static types are not the only ( or even necessarily the best ) way to know your types.

\== is not about comparisons with unknown types.

\== is about comparisons with known type(s), optionally where conversions are helpful.

If you know the type(s) in a comparison:\
If both types are the same, == is identical to ===

Using === would be unnecessary so prefer the shorter ==

If the types are different, using one === would be broken.

Prefer the more powerful == or don't compare at all

If the types are different, the equivalent of one == would be two (or more!) === (ie, "slower")

The faster argument is not the main point here, which is that not always the === is better than the ==, killing what many people say about the ===, that should always be used, and that == is useless.

If the types are different, two (or more!) === comparisons may distract the reader.

If you don't know the type(s) in a comparison:\
Not knowing the types means not fully understanding that code. So best to refactor so you do know the types.

The uncertainty of not knowing types should be obvious to the reader. The most obvious signal is === (This is because you don't know the types).

Not knowing the types is equivalent to assuming type conversion.

Summary: if you can't or won't use known and obvious types, === is the only reasonable choice.

Even if === would always be equivalent to == in your code, using it everywhere sends a wrong signal: "Protecting myself since I don't know/trust the types" => meaning the next dev could do what you didn't do, refactor so that the types are known.

Summary 2.0: Making types known and obvious leads to better code. If types are known, == is best.

Otherside, fall back to ===

