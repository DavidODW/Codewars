# Build a pile of Cubes

## My Solution

```javascript
function findNb(m) {
    // your code
    let n = 0;
    let total = 0;
    while (total <= m) {
        total += Math.pow(n, 3);
        if (total == m) {
            return n;
        }
        n++;
    }

    return -1;
}
```

## Most upvoted solution

```javascript
function findNb(m) {
    var n = 0;
    while (m > 0) m -= (++n) ** 3;
    return m ? -1 : n;
}
```

## Learning

* `Math.pow(n, 3)` is same as `n ** 3`
