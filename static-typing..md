---
description: >-
  This is kinda like a funny scenario where Kyle is saying adv. and cons of
  static types even tho he does not use Typescript or an IDE, where most of the
  Pros come from. But it's a good exercise to see.
---

# Static Typing.

Pros.

They make types more obvious in code.

Familiarity: They look like other languages' type systems.

Extremely popular these days. ( Big documentation && community ).

They're very sophisticated and good at what they do.

Cons.

They use "non-JS-standard" syntax (or code comments) => It is not what JS is doing.

They require\* a build process, which raises the barrier to entry. => a dozen tools in a pipeline to just ship the code into the browser.

Their sophistication can be intimidating to those without prior formal types of experience.  => I feel this is what happens to me when I do TS.

They focus more on "Static types" (Variables, parameters, returns, properties, etc) than value types. => "If you think of that JS really is and in fact any dynamic language, it's a language that is value typing, not variable typing."

Wrapping up.

JS has a ( dynamic ) type system, which uses various forms of coercion for value type conversion, including equality comparison.

However, the prevailing response seems to be: to avoid as much of this system as possible and use === to "protect" from needing to worry about types.

Part of the problem with avoidance of whole swaths of JS, like pretending === saves you from needing to know types, is that it tends to systematically perpetuate bugs.&#x20;

> I do not need to understand this whole part of the language ( types ) so ill leave it as it is and just use ===&#x20;

You simply cannot write quality JS programs without knowing the types involved in your operations.

Alternately, many choose to adopt a different "static types" system layered on top.

While certainly helpful in some respect, this is "avoidance" of a different sort.

Apparently, JS's type system is inferior so it must be replaced, rather than learned and leveraged.

Many claims that JS's type system is too difficult for newer devs to learn, and that static types are ( somehow ) more learnable.

My claim ( Kyle's ): the better approach is to embrace and learn JS's type system, and to adopt a coding style that makes types as obvious as possible.

By doing so, you will make your code more readable and more robust, for experienced and new devs alike.

{% hint style="info" %}
"As an option to aid in that effort, I created [typl](https://github.com/getify/TypL), which I believe embraces and unlocks the best parts of JS's type and coercion."
{% endhint %}







