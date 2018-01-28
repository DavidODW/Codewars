# String matchup

## My Solution

```javascript
function solve(a, b) {
    let hashMap = {};
    a.forEach(el => (hashMap[el] = hashMap[el] + 1 || 1));
    return b.map(el => hashMap[el] || 0);
}
```

## Most upvoted solution

```javascript
const solve = (a, b) => b.map(x => a.filter(n => n === x).length);
```
