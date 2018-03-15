# Create Phone Number

## My Solution

```javascript
function createPhoneNumber(numbers) {
    return `(${numbers.slice(0, 3).join("")}) ${numbers.slice(3, 6).join("")}-${numbers
        .slice(6)
        .join("")}`;
}
```

## Most upvoted solution

```javascript
function createPhoneNumber(numbers) {
    return numbers.join("").replace(/(...)(...)(.*)/, "($1) $2-$3");
}
```

## Learning

*   Use regex to extract string in certain format, and indicate the correspending matching as `$1`-`$9`.
