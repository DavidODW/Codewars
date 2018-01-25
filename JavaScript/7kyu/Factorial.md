# Recursion #1 - Factorial

## My Solution

```javascript
const factorial = n => {
    if (n == 0) return 1;
    return n * factorial(n - 1);
};
```

## Most upvoted solution

```javascript
const factorial = n => (n > 1 ? n * factorial(n - 1) : 1);
```
