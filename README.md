## Welcome to Useful Code Snippets - Typescript

## Variables and Types

```typescript

// Variable

let x: string;

// Array

let list: number[] = [1, 2, 3];

let list2: Array<number> = [1, 2, 3];

// Enum

enum Color {Red = 1, Green, Blue}
let colorName: string = Color[2];

alert(colorName);

// Any

let notSure: any = 4;
notSure = "maybe a string instead";
notSure = false; // okay, definitely a boolean

let list3: any[] = [1, true, "free"];

// Void

function warnUser(): void {
    alert("This is my warning message");
}
```

## Assertions

Type assertions have two forms. One is the "angle-bracket" syntax < >:

```typescript
let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;
```

The other is the as-syntax:
```typescript
let strLength2: number = (someValue as string).length;
```

## Interfaces
```typescript
interface LabelledValue {
    label: string;
}

// Optional Properties
interface SquareConfig {
    color?: string;
    width?: number;
}

// Readonly properties
interface Point {
    readonly x: number;
    readonly y: number;
}
```

## Function Types
```typescript
interface Search {
    (source: string, subString: string): boolean;
}

let mySearch: Search;
mySearch = function(src: string, sub: string): boolean {
    let result = src.search(sub);
    return result > -1;
}
```
## Classes

### Simple Class
```typescript
class Speaker {
    speech: string;
    constructor(message: string) {
        this.speech = message;
    }
    speaking() {
        return "Hello, " + this.speech;
    }
}

let speaker = new Speaker("world");
```
### Private and Protected
```typescript
class Person {
    protected name: string;
    protected constructor(name: string) { this.name = name; }
}

class Employee extends Person {
    private department: string;

    constructor(name: string, department: string) {
        super(name);
        this.department = department;
    }

    public presentation() {
        return `Hello, my name is ${this.name} and I work in ${this.department}.`;
    }
}
let james = new Employee("James", "Sales");
```

### Readonly Modifier
```typescript
class Animal {
    readonly name: string;
    readonly numberOfLegs: number = 4;
    constructor (theName: string) {
        this.name = theName;
    }
}
let lion = new Animal("Lion");
```


### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/acqfel/node-test/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

