1. Challenge 1:
  - Answer: b
  
  - Explanation:
  * The variable foo is declared globally with the value "abc".
  * The function bar() modifies foo to "xyz", which affects the global variable.
  * Inside bar(), console.log(foo); prints "xyz".
  * After calling bar(), the global variable foo remains "xyz", so console.log(foo); prints "xyz" again.


2. Challenge 2:
  - Answer: c
  - Explanation:
* The variable a is declared globally with the value 1.
* The function example(a) takes a as a parameter, creating a new local a inside the function.
* Inside the function, the local a is reassigned to 10, but this does not affect * the global a.
* console.log(a); inside the function prints 10 because it's logging the local a.
* After calling example(a), the global a remains unchanged (1), so console.log(a); after the function prints 1.


3. Challenge 3:
  - Answer: c
  - Explanation:
  * The function is being hoisted, meaning the entire function is moved to the top of its scope before execution.
  * This allows you to call sayHi(); before its actual definition in the code.
  * When sayHi(); is executed, it correctly refers to the function, which logs "Hi there!" to the console.


4. Challenge 4:
  - Answer: c
  - Explanation:
  * a is assigned an object { num: 42 }.
  * b = a; does not create a copy of the object. Instead, both a and b reference the same object in memory.
  * When we do b.num = 90;, we are modifying the same object that a also references.
  * Therefore, when we log a, we see { num: 90 } instead of { num: 42 }.


5. Bonus - Challenge 5:
  - Answer: c
  - Explanation:
* Passing rabbit1 by reference:
** The function magicHat receives rabbit1 as obj.
** Since objects are passed by reference, obj initially refers to the same object as rabbit1.
** Modifying obj.age = 10, modifies the original object (rabbit1), so now rabbit1.age is 10

* Reassigning obj = { name: "Ada", age: 20 };:
** Here, obj is assigned a new object, { name: "Ada", age: 20 }.
** However, this does not change rabbit1, because now obj refers to a new object rather than the original one.
** Returning obj: The function returns { name: "Ada", age: 20 }, which gets assigned to rabbit2.

* Final Values:
** rabbit1 still references the original object, now modified to { name: "Bob", age: 10 }.
** rabbit2 references a new object { name: "Ada", age: 20 }.