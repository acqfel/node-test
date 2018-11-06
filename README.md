## Welcome to Useful Code Snippets - Typescript

## Snippets

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

/* Assertions */

//Type assertions have two forms. One is the "angle-bracket" syntax < >:

let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;

//And the other is the as-syntax:
let strLength2: number = (someValue as string).length;

/* Interfaces */

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
[Jekyll](https://jekyllrb.com/)

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

