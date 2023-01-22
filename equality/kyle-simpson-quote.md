# Kyle Simpson Quote

Like every other operation, is coercion helpful in an equality comparison or not?

"It is helpful to understand what the types are. Like any other operation, you have to ask yourself, if I know the types, is coercion here helpful or not?

It's a critical analysis. It shifts the discussion away from double equals is bad and unpredictable to do I wanna allow a coercive comparison or do I not wanna allow that?

In this particular case, is it more helpful to me to do so or not? Is it more safe or is it less safe? In other words, _**you need to be critical, analytical thinkers**_, and look at your code.

Essentially the decision about double equals and triple equals is a _**trailing indicator of whether you actually understand your program.**_

Your choice to use triple equals, it's not just because some guy wrote in a book that you should always use triple equals. Your actual choice to use triple equals is a trailing indicator that points back to the fact that you don't know something about the types in that comparison and so you have to protect yourself.

In my opinion, if at all possible, maybe it would be better to fix the root problem, which is that I don't know what the types are in this comparison. It's too unpredictable, it's too polymorphic.

_**That's gonna lead to better code with fewer bugs regardless of whether you use double or triple equals.**_

Deciding what your types are, making it obvious what those are. "\
Coercive equality in Equality Chapter.
