# Do I get a bonus?

## My Solution

```javascript
function bonusTime(salary, bonus) {
    return bonus ? `£${salary * 10}` : `£${salary}`;
}
```

## Most upvoted solution

```javascript
function bonusTime(salary, bonus) {
    return bonus ? `£${10 * salary}` : `£${salary}`;
}
```
