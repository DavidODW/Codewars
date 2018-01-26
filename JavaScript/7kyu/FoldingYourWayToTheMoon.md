# Folding your way to the moon

## My Solution

```javascript
function foldTo(distance) {
    if (distance <= 0) return null;
    if (distance <= 0.0001) return 0;

    return 1 + foldTo(distance / 2);
}
```

## Most upvoted solution

```javascript
function foldTo(n) {
    return n > 0 ? Math.max(0, Math.ceil(Math.log2(1e4 * n))) : null;
}
```
