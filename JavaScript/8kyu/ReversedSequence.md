# Reversed sequence

## My Solution

```javascript
const reverseSeq = n => {
    return Array.from({ length: n }, (v, k) => n - k);
};
```
