# Give me a Diamond

## My Solution

```javascript
function diamond(n) {
    if (n < 3 || !(n % 2)) return null;

    let array = [];
    for (let i = 1; i <= n; i += 2) {
        array.push(i);
    }

    array = array.concat(array.slice(0, array.length - 1).reverse());

    let diam = "";
    for (let j = 0; j < array.length; j++) {
        diam = diam + " ".repeat((n - array[j]) / 2) + "*".repeat(array[j]) + "\n";
    }

    return diam;
}
```

## Most upvoted solution

```javascript
function diamond(n) {
    if (n % 2 == 0 || n < 1) return null;
    var x = 0,
        add,
        diam = line(x, n);
    while ((x += 2) < n) {
        add = line(x / 2, n - x);
        diam = add + diam + add;
    }
    return diam;
} //z.

function repeat(str, x) {
    return Array(x + 1).join(str);
}
function line(spaces, stars) {
    return repeat(" ", spaces) + repeat("*", stars) + "\n";
}
```

## Learning

* Use `str.repeat(count)` to repeat `str` for `count` times.
* Different logic to construct a diamond.
