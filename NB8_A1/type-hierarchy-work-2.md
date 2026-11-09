**Type Hierarchy work:**
1. any bypass normal type checking.
2. unknown is the safest top type because almost any value can be assigned to it.
3. never is the bottom type because it can be assigned to any other type, but normally no value can be assigned to never.

In TypeScript, any unknown and never are special types that control how values are handled in the type system.

**any:**
1. Allows any type of value.
2. Disables TypeScript type checking.
3. Can cause runtime errors if used incorrectly.

**Example:**

let value: any = "Hello";
value = 100;
value.toUpperCase();

**unknown:**
1. Can store any type of value.
2. Requires type checking before performing operations.
3. Provides better type safety than any.

**Example:** 
let value: unknown ="Hello";
if (typeof value === "string"){
    console.log(value.toUpperCase());
}

**never:** 
1. Represents a value that never occurs.
2. USed for functions that never return normally, such as function that throw errors or run indefinitely.
3. Also used for exhaustive type check 

**Example:**

function throwError(): never{
    throw new Error("Somethig wrong");
}

**Why is unknown always Preferred over any?**
=> uknown is preferred because it provides type safety. TypeScript requires us to check the type before using a value whereas any allows operation without checking, which may cause errors.
unknown is preferred over any because it maintains type safty. While never represents impossible values and any disables type checking.