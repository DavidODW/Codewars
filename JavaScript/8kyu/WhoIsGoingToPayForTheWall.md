# Who is going to pay for the wall?

## My Solution

```javascript
function whoIsPaying(name) {
    let shortName = name
        .split("")
        .splice(0, 2)
        .join("");

    return shortName === name ? [name] : [name, shortName];
}
```

## Most upvoted solution

```javascript
function whoIsPaying(name) {
    return name.length > 2 ? [name, name.substr(0, 2)] : [name];
}
```
