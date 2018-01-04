# Rotate for a Max

## Solution

```javascript
function maxRot(n) {
    let numbers = [n];

    // Convert number into an array of digit. 123 => ['1', '2', '3]
    let digitArray = (n + "").split("");

    let number = digitArray.slice();

    // Repeat rotate process until last digit.
    for (let i = 0; i < digitArray.length - 1; i++) {
        // Extract out the first i digits from digit array
        let digitToKeep = number.splice(0, i);

        // Rotate the remaining part of digit array
        number.push(number.shift());

        number = digitToKeep.concat(number);

        // Join the digit array and convert them to number
        numbers.push(Number(number.join("")));
    }

    // Return the biggest number in the array
    return numbers.sort((a, b) => a - b).pop();
}
```

## Most upvoted solution

```javascript
function maxRot(n) {
    var str = n.toString();
    var arr = [str];
    for (var i = 0; i <= str.length - 1; i++) {
        str = str.slice(0, i) + str.slice(i + 1) + str[i];
        arr.push(str.split().join());
    }
    return Math.max.apply(null, arr);
}
```

## Learning

* `Math.max` accepts infinite arguments, convert them to number and return the largest number.
  > If no arguments are given, the result is `-Infinity`.
  > If at least one of arguments cannot be converted to a number, the result is `NaN`.
  >
  > * [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/max)
* `array.push(array.shift())` is inverse of `array.unshift(array.pop())`
