# Rotate for a Max

## Solution

```javascript
function maxRot(n) {
    let numbers = [n];

    let digitArray = (n + "").split("");

    let number = digitArray.slice();
    for (let i = 0; i < digitArray.length - 1; i++) {
        let digitToKeep = number.splice(0, i);
        number.push(number.shift());

        number = digitToKeep.concat(number);
        numbers.push(Number(number.join("")));
    }

    return numbers.sort((a, b) => a - b).pop();
}
```
