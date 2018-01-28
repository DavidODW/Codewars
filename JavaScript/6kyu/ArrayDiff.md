# Array.diff

## My Solution

```javascript
function array_diff(a, b) {
    return a.filter(el => b.indexOf(el));
}
```

## Most upvoted solution

```javascript
function array_diff(a, b) {
    return a.filter(function(x) {
        return b.indexOf(x) == -1;
    });
}
```
