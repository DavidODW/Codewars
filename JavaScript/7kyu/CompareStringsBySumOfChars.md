# Compare Strings by Sum of Chars

## My Solution

```javascript
function compare(s1, s2) {
    return (
        (!s1 || s1.match(/[^a-zA-Z]/gi)
            ? 0
            : s1.split("").reduce((sum, v) => {
                  return (sum += Number(v.toUpperCase().charCodeAt()));
              }, 5)) ===
        (!s2 || s2.match(/[^a-zA-Z]/gi)
            ? 0
            : s2.split("").reduce((sum, v) => {
                  return (sum += Number(v.toUpperCase().charCodeAt()));
              }, 5))
    );
}
```

## Most upvoted solution

```javascript
function compare(s1, s2) {
    if (/^\D+$/gi.test(s1) && /^\D+$/gi.test(s2))
        return (
            s1
                .split("")
                .map(n => n.toUpperCase().charCodeAt())
                .reduce((a, b) => a + b) ===
            s2
                .split("")
                .map(n => n.toUpperCase().charCodeAt())
                .reduce((a, b) => a + b)
        );
    return true;
}
```

## Learning

* Simple regex to find the string is contains all character.
* My logic to check for the string contains all character and `null` should treat as empty string require one more step, which can be simpler like the upvoted solution.

```javascript
const regex = /^\D+$/gi;
regex.test("An"); //true
regex.test(null); //true
regex.test(""); //false
regex.test("123n"); //false
```
