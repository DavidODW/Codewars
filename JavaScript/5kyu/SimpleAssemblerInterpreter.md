# Simple assembler interpreter

## My Solution

```javascript
function zeros(n) {
    function simple_assembler(program) {
        let pointer = 0;
        let dictionary = {};
        while (pointer < program.length) {
            let [operator, variable, value] = program[pointer].split(" ");
            if (operator == "jnz" && dictionary[variable] !== 0) {
                pointer += parseInt(value);
            } else {
                dictionary = compiler(dictionary, operator, variable, value);

                pointer++;
            }
        }
        return dictionary;
    }

    function compiler(dictionary, operator, variable, value) {
        switch (operator) {
            case "mov":
                number = parseInt(value);
                dictionary[variable] = Number.isInteger(number) ? number : dictionary[value];
                break;
            case "inc":
                ++dictionary[variable];
                break;
            case "dec":
                --dictionary[variable];
                break;
            default:
                break;
        }
        return dictionary;
    }
}
```

## Most upvoted solution

```javascript
function simple_assembler(program) {
    const mem = {};
    for (let i = 0; i < program.length; ++i) {
        const [op, reg, val] = program[i].split(" ");
        if (op === "mov") {
            mem[reg] = isNaN(val) ? mem[val] : +val;
        } else if (op === "inc") {
            mem[reg] = (mem[reg] || 0) + 1;
        } else if (op === "dec") {
            mem[reg] = (mem[reg] || 0) - 1;
        } else if (op === "jnz") {
            if (mem[reg] !== 0) {
                i += val - 1;
            }
        }
    }
    return mem;
}
```
