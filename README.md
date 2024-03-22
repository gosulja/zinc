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

### If statements
```ts
let age = 20;

if age > 18 {
    print("Access Granted.");
} else {
    print("Access Denied.");
}
```
Note, if statements only has an else branch available, even though theres an `elif` keyword, it isn't functional and will error.

### While statements
```ts
let count = 0;

while count < 10 {
    count = count + 1;
}

print(count)
```

While statements continuously run until the condition is false. All relational expressions result to a bool value.

### For statements
Zinc contains two iterables currently: arrays and strings.

```ts
const nums = [1, 2, 3, 4, 5, 6];
let sum = 0;

for num : nums {
    sum = sum + num;
}

print(sum);
```

The for statement is structured like this:

`for <item_identifier> : <iterable> { <body> }`

The `item_identifier` doesn't have the `let` keyword to initialize it.

### Functions
Zinc has functions like any other language, and anonymous functions. Zinc does not have a return keyword, so any identifier or literal which is at
the end of the function will be returned.

```rs
fn adder(a, b) {
    a + b
}

print(adder(5, 5));
```

### Anonymous functions
Like mentioned before, you can use anonymous functions.

```rs
const adder = fn(a, b) {
    a + b
}

print(adder(5, 5));
```

### Imports and Exports
Zinc has the feature to export and import functions and variables. With the use of the `pub` keyword before the `let` or `const` keyword, it can be achieved.

name.zc
```rs
pub const name = "John";
```

main.zc
```rs
import("name")

print(name);
```

#### In-built functions and libraries
Zinc has a small list of in-built functions and libraries.

* print
* as
* type
* len
* import

* os
* io

#### `print`
Zinc will print the value if it supported or not. Can print: `string`, `number`, `boolean`, `null`, `array`, `object`

#### `as'
Zinc will convert the given value to the one provided. Example:
```ts
print(as(5, "string"))
```

#### `type`
Zinc will return the type of the value provided.

#### `len`
Zinc will return the length of the iterable as a number value.

#### `import`
Zinc will import the given scripts exported environment variables into the current environment.

### Libraries

#### `os`
Contains:
* time -> Number
* clock -> Number

#### `io`
Contains:
* input -> String | Null
