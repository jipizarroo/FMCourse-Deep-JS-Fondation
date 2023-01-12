---
description: >-
  With those as our foundation, those abstract operations, it is time to switch
  gears and really tackle the topic of coercion.
---

# Cases of Coercion

Is coercion evil, and must be avoided at all causes? Welp, in this example, will see that everybody uses coercion at some point while writing code in JS.

```javascript
var numStudents = 16;

console.log(
`There are ${numStudents} students.`
);

// "There are 16 students."

/* This is been done by coercion */
/* Coercion: string concatenation (number to a string) */

var msg1 = "There are ";
var numStudents = 16;
var msg2 = " students.";
console.log(msg1 + numStudents + msg2);

/* SPEC STUFF
    The Addition Operator (+)
    The addition operator either performs string concatenation or numeric addition.
*/

// "There are 16 students."

/* Recall Falsy vs Truthy */

if (studentsInputElem.value){
    // what if studentsInputElem has a bunch of empty spaces in it?? now it's truthy.
    numStudents = Number(studentsInputElem.value);
}

while (numStudents.length){
    // what happens when it's NaN ??
    enrollStudent(numStudents.pop());
}

/* FIX */
if (!!studentsInputElem.value){
    // Become a boolean with the !! or use Boolean()
    numStudents = Number(studentsInputElem.value);
}

while (numStudents.length > 0){
    // Protects for some semantic errors, not all of them, but it's more explicit too.
    enrollStudent(numStudents.pop());
}

```
