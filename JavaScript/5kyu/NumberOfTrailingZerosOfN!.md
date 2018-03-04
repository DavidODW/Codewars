# Number of trailing zeros of N!

## My Solution

```javascript
function zeros(n) {
    let trallingZero = 0;

    for (let i = 5; n / i > 1; i *= 5) {
        trallingZero += Math.floor(n / i);
    }

    return trallingZero;
}
```

## Learning

*   Understand a theory to quicky to find out the trailing zero from [website](https://brilliant.org/wiki/trailing-number-of-zeros/).
