# Compilation & scope.

<pre class="language-javascript" data-line-numbers><code class="lang-javascript"><strong>
</strong><strong>
</strong><strong>var teacher = "Kyle"; // Formal declaration, we are creating a marble into the
</strong><strong>// global scope ( color of the marble ).
</strong><strong>// The compiler asks the global scope, have you ever heard of this thing called
</strong>// teacher? - If it knows about the word teacher, it doesn't need to do anything
// If its the first time, it creates a marble and drops it into the global
// bucket

// same process here, it creates a marble and drops it into the global bucket.
// but since the function can have its own scope, it creates a new bucket.
// ( a bucket inside a bucket )
// Same conversation happens but instead of the global bucket, we are inside
// the new one, for the function otherClass scope, do it does not know about the
// var teacher of the global one. so it creates a new marble but for the local 
// scope.
function otherClass(){
    var teacher = "Suzy";
    console.log("Welcome");
}

// same process here, it creates a marble and drops it into the global bucket.
// we create a new bucket since we have a new function, different from the one
// created by the otherClass function.
function ask(){
    var question = "Why?";
    console.log(question);
}

otherClass();     // Welcome
ask();            // Why?
</code></pre>

All of the bucket and marble stuff is happening at Compile time, the reason this is important is that it leaves the JS engine to do its work at a better pace, since all of the scope sortings have been done before runtime.

### Execution time!

Virtual machine ( JS engine ) enters into the game =>

JS Engine: Hey scope manager, I have a target reference for a variable named teacher, do you know about it?\
\
Global bucket: Yes ( Remember that at formal time, we declared, that's why it knows it )

Lines 3 and 8 are declarations, so execution time jumps from line 1 to 13.

Line 13 is in a source position, we want to know the value that it has. and the JS does the same thing as with line one.

But what happens when we execute and we get to line 5 ? We never created a target for the console. Well JS is kind of like an auto-global scope, where the console is at.

What we need to understand, and we saw this on the other FMCourse JS hard part, is that if we do not get a reference for the target in the local scope ( the otherClass bucket ), we go up a level, we go into the global bucket and ask for that declaration.

