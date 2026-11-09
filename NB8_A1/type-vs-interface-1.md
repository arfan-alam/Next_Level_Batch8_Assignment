Core Difference Between type Aliases and interface in TypeScript:

In TypeScript, both type aliases and interface are used to define the structure of data. However they have some differences.

**type Alias:**

1. Can define object, primitives, unions and tuples.
2. Uses & for combining types.
3. Does not support declaration merging.
4. Supports union types.
5.Can create complex type combinations.

**Example of type:**

type User = {
    name: string;
    age: number;
};
type Id = string | number;

**Interface:**

1. Mainly defines object structures.
2. Uses extends for inheritance.
3. Supports declaration merging.
4. Does not directly support union types.
5. Best suited for object-oriented structures.

**Example of interface:**

interface User{
    name: string;
    age: number;
}
interface Student extends User{
    studentId: number;
}

When choose One Over the Other:

Type aliases and interfaces both play an important role in TypeScript programming. Despite similarities in functionality, the use of both constructs is different because of their goals. 

My recommendation: Use interface when desiging object structures and type in the case of unions, intersections, primitive types etc. Though it must be stated that it is only a suggestion and not a rule since both constructs can be used. 

