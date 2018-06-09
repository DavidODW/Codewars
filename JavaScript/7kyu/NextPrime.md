# Next Prime

## My Solution

```javascript
function isPrime(number) {
    for (let j = 2; j <= Math.sqrt(number); j++) {
        if (number % j == 0) return false;
    }

    return true;
}

function nextPrime(n) {
    if (n == 0 || n == 1) return 2;

    for (let i = n + 1; i <= n * 2; i++) {
        if (isPrime(i)) return i;
    }
}
```
