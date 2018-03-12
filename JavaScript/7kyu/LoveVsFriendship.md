# Love vs friendship

## My Solution

```javascript
function wordsToMarks(string) {
    return string
        .split("")
        .map(a => a.charCodeAt(0) - 96)
        .reduce((a, b) => a + b, 0);
}
```

## Most upvoted solution

```javascript
const wordsToMarks = s => [...s].reduce((res, c) => (res += c.charCodeAt() - 96), 0);
```

## Learning

*   `[...string]` is the alternative to `string.split("")`. Both of them is to convert string into char array.
