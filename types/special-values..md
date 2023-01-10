# Special values.

### NaN

NaN => It's better to have it as not a valid number instead of not a number.

{% code lineNumbers="true" %}
```javascript
var myAge = Number("0o46");        // 38
var myNextAge = Number("39");    // 39
var myCatsAge = Number("n/a");    // NaN
myAge - "my son's age";        // NaN

myCatsAge === MyCatsAge;        // false OOPS! 

isNaN(myAge);                    // false
isNaN(myCatsAge);                // true
isNaN("my son's age");            // true OOPS!

Number.isNaN(myCatsage);         // true
Number.isNaN("my son's age");    // false
```
{% endcode %}

The "n/a" is something we should take a deeper look at, 0 should not be the way we do the absence of a thing, 0 is indeed a number and it's a special one, numerically and in programming, we should not use 0 for the absence of something.

in line 4, we get NaN, because JS is seen as the - operator saying I should be getting a number so I can continue with the operation, so it turns the string into a number, getting an invalid one.

NaN is the only value in JS that does not have the identity property, meaning it is not equal to itself, that's why we get that result in line 6.



### Negative Zero



```javascript
var trendRate = -0;
trendRate === -0;            // true

trendRate.toString();        // "0" OOPS! Historical error
trendRate === 0;            // true OOPS
trendRate < 0;              // false
trendRate > 0;              // false

Object.is(trendRate, -0);   // true
Object.is(trendRate, 0;     // false;
```

\*\* Would like to know how I could use this in my code, coz it was not cleat to me how to use it :B \*
