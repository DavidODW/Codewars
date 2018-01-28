# Cat years, Dog years

## My Solution

```javascript
var humanYearsCatYearsDogYears = function(humanYears) {
    let catYears = 15 + (humanYears >= 2 ? 9 : 0) + (humanYears >= 3 ? (humanYears - 2) * 4 : 0);
    let dogYears = 15 + (humanYears >= 2 ? 9 : 0) + (humanYears >= 3 ? (humanYears - 2) * 5 : 0);

    return [humanYears, catYears, dogYears];
};
```

## Most upvoted solution

```javascript
const humanYearsCatYearsDogYears = humanYears => [
    humanYears,
    (humanYears - 1 ? 16 : 11) + 4 * humanYears,
    (humanYears - 1 ? 14 : 10) + 5 * humanYears
];
```
