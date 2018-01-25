# Find the stray number

## My Solution

```javascript
function maxRot(n) {
    function stray(numbers) {
        return numbers.find((i, index) => numbers.lastIndexOf(i) == numbers.indexOf(i));
    }
}
```

## Most upvoted solution

```javascript
function stray(numbers) {
    for (var i in numbers) {
        if (numbers.indexOf(numbers[i]) === numbers.lastIndexOf(numbers[i])) {
            return numbers[i];
        }
    }
}
```
