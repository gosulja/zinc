# zinc
Zinc or blinxscript is a scripting language written for learning.

# Usage
1. Download the `zinc-us-1.0` release.
2. Extract the zip.
4. Place the binary in your working directory or in system env variables.
3. Create a file with the `.zc` extension.
4. Run `zinc [file.zc]`
5. Enjoy

# Learn
Zinc doesn't have a learning reference, but it's similar to any programming language.

### Variables and Constants
```ts
const name = "John";
let age = 23;
```
Semi-colons are optional.

Zinc supports type annotations, but it doesn't do anything.
```ts
const name string = "John";
```

### Arrays and Objects
Zinc has the traditional array and object constructs, and can be used like this.

```ts
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```
Arrays are initialized with brackets, whereas objects are initlialized with braces.

```ts
const person = {
    name: "John",
    age: 23
};
```

### Member access
Zinc has a few interesting symbols to allow you to access members in objects. For example:

```ts
const person = {
    name: "John",
    age: 23
};

-- this is a comment

-- Classic dot notation
let name = person.name;

-- Arrow notation
let name2 = person->name;

-- Scope notation
let name3 = person::name; 
```

Note that these symbols all do the same thing, but in other languages such as `C++`; the `->` and `::` are used for different things, this shouldn't be mixed up with Zinc.
Member assignment has not been added yet.

### Statements
Without logic, you cannot program. Zinc has while statements, if statements, for statements. Everything is a statement.
The way Zinc handles some statements varies.

#### If statements
```ts
let age = 20;

if 





