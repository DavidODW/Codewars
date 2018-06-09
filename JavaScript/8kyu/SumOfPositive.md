# Sum Of Positive

## My Solution

```javascript
function positiveSum(arr) {
    return arr.filter(n => n > 0).reduce((a, b) => a + b, 0);
}
```
