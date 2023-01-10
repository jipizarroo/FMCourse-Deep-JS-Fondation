# Primitive Types

* Undefined
* String => string literal
* Number
* Boolean
* Object
* Symbol

What about these ones?\


* Undeclared?
* Null? => Historical error
* Function? => Sub-type of an object
* Array?
* Bigint? => Since this course was recorded, Bigint has been added to the language as another primitive.

They say in JS all values are Objects, but as we can see, most of the primitive types are actually not objects at all, not even close to them.

(In JS, variables don't have types, values do)



### typeof Operator

<pre class="language-javascript"><code class="lang-javascript"><strong>// We ask what is the typeof the value that's currently in the v?
</strong><strong>var v;
</strong>typeof v;    // "undefined"

v = "1";    
typeof v;    // "string"

v = 2;
typeof v;    // "number"

v = true;     
typeof v;    // "boolean"

v = {};     
typeof v;   // "object"  

v = Symbol();
typeof v;    // "symbol" 

typeof doesntExist;     // "undefined"

var v = null;        
typeof v;    // "object" OOPS!

v = function(){};
typeof v;    // "function" hmm?

v = [1,2,3]
typeof v;    // "object" hmm?
</code></pre>

The type null returning an object is just a bug, and for that reason when you check the type and returns object you must check that is not returning a null value.

The thing about functions and arrays is just a historical error, it's useful for functions to return functions but not for arrays, but fixing this would break a BUNCH of code everywhere, that's why we should learn how it works and simply work around them.

```
var v = 42n;
// or: BigInt(42)
typeof v;    // "bigint"
```

This is useful because numbers and bigint are not the same things and they do not mix well with each other, this type will help us work better around these types of numbers.

