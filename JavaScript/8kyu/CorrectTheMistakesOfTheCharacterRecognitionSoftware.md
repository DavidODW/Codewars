# Correct the mistakes of the character recognition software

## My Solution

```javascript
function correct(string) {
    return string
        .replace(/5/g, "S")
        .replace(/0/g, "O")
        .replace(/1/g, "I");
}
```
