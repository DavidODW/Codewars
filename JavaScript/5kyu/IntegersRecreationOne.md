# Integers: Recreation One

## My Solution

```javascript
function listSquared(m, n) {
    let squared = [];
    range(m, n).forEach(v => {
        let sum = getDivisors(v).reduce(
            (carry, accumulator) => carry + accumulator * accumulator,
            0
        );

        if (sum % Math.sqrt(sum) == 0) {
            squared.push([v, sum]);
        }
    });

    return squared;
}

function getDivisors(n) {
    var divisors = [];

    for (var i = 1; i <= n / 2; ++i) {
        if (n % i) {
            continue;
        }

        divisors.push(i);
    }

    return divisors.concat([n]);
}

function range(start, end) {
    return Array(end - start + 1)
        .fill()
        .map((_, idx) => start + idx);
}
```

## Most upvoted solution

```javascript
function listSquared(m, n) {
    var matches = [];

    for (var i = m; i <= n; ++i) {
        var sum = getDivisors(i).reduce((sum, n) => sum + n * n, 0);
        var ok = Number.isInteger(Math.sqrt(sum));

        if (ok) {
            matches.push([i, sum]);
        }
    }

    return matches;
}

function getDivisors(n) {
    var divisors = [];

    for (var i = 1; i <= n / 2; ++i) {
        if (n % i) {
            continue;
        }

        divisors.push(i);
    }

    return divisors.concat([n]);
}
```

## Learning

* Use `sum % Math.sqrt(sum) == 0` to find the number is perfect square.
* Use `Array.fill()` to generate a sequential number array.
* When find the divisors, ignore the latter `number / 2` to reduce the extra calculation.
