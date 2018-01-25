# Sum of Triangular Numbers

## My Solution

```javascript
function sumTriangularNumbers(n) {
    if (n < 0) {
        return 0;
    }

    let sum = 0;

    for (let i = 1; i <= n; i++) {
        sum += i / 2 * (i + 1);
    }

    return sum;
}
```

## Most upvoted solution

```javascript
function sumTriangularNumbers(n) {
    return n < 0 ? 0 : n * (n + 1) * (n + 2) / 6;
}
```

## Learning

* The nth of triangular number formulae is `n / 2 * (n + 1)`
* Summation of triangular number formulae is `n * (n + 1) * (n + 2) / 6`
