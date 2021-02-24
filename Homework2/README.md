
## Question 5
![plot](https://github.com/Ulq1517/CMSI488-2021/blob/main/Homework2/CMSI 488 HW 2 Q5.jpg)
## Question 6
![plot](https://github.com/Ulq1517/CMSI488-2021/blob/main/Homework2/CMSI 488 HW 2 Q6.jpg)

## Question 7a
```js
export class Program {
    constructor(instructions) {
        this.instructions = instructions
    }
}
 
export class SimpleInstruction {
    constructor(symbol) {
        this.symbol = symbol
    }
}
 
export class LoopInstruction {
    constructor(instructions) {
        this.instructions = instructions
    }
}
```
## Question 7b

```js

const astBuilder = Brainfuck.createSemantics.addOperation("ast", {
    Program(instructions) {
        return new ast.Program(instructions.ast())
    },
    SimpleInstruction(_symbol) {
        return new ast.SimpleInstruction(_symbol.ast())
    },
    LoopInstruction(_left, instructions, _right) {
        return new ast.LoopInstruction(instructions.ast())
    }
})
```