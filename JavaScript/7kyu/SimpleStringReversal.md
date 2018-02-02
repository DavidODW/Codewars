# Simple string reversal

## My Solution

```javascript
function solve(str) {
    let reverse = str
        .replace(/\s/g, "")
        .split("")
        .reverse()
        .join("");

    return str
        .split(" ")
        .map(str => {
            let word = reverse.substring(0, str.length);
            reverse = reverse.slice(str.length);
            return word;
        })
        .join(" ");
}
```

## Most upvoted solution

```javascript
function solve(str) {
    var result = str
        .split(" ")
        .join("")
        .split("")
        .reverse();
    str.split("").map((c, index) => {
        if (c === " ") result.splice(index, 0, " ");
    });
    return result.join("");
}
```
