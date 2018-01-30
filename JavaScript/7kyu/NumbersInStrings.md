# Numbers in strings

## My Solution

```javascript
function solve(s) {
    return s
        .match(/\d+/gi)
        .map(Number)
        .sort((a, b) => b - a)[0];
}
```

## Most upvoted solution

```javascript
solve = s => Math.max(...s.match(/\d+|$/g));
```

## Learning

* Use `Math.max()` to find the largerst number in the arguments.
* Use `...` to spread all element array into zero or more arguments.
