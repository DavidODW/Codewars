# Kebabize

## My Solution

```javascript
function kebabize(str) {
    return str
        .replace(/[0-9]+/g, "")
        .split(/(?=[A-Z]+)/)
        .map(ch => ch.toLowerCase())
        .join("-");
}
```

## Most upvoted solution

```javascript
function kebabize(str) {
    return str
        .replace(/[^a-z]/gi, "")
        .replace(/^[A-Z]/, c => c.toLowerCase())
        .replace(/[A-Z]/g, c => `-${c.toLowerCase()}`);
}
```

## Learning

* Use `positive lookahead` so that the regular expression asserts that the special character exists, but does not actually match it.
* Using an inline function that modifies the matched characters.
