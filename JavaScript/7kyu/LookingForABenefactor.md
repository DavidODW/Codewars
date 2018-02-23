# Looking for a benefactor

## My Solution

```javascript
function newAvg(arr, newavg) {
    let newNumber = newavg * (arr.length + 1) - arr.reduce((carry, el) => carry + el, 0);
    if (newNumber < 0) {
        throw "";
    }

    return Math.ceil(newNumber);
}
```
