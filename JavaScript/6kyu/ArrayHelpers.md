# Array Helpers

## Solution

```javascript
Array.prototype.square = function() {
    return this.map(i => i ** 2);
};

Array.prototype.cube = function() {
    return this.map(i => i ** 3);
};

Array.prototype.sum = function() {
    return this.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
};

Array.prototype.average = function() {
    return this.sum() / this.length;
};

Array.prototype.even = function() {
    return this.filter(i => i % 2 == 0);
};

Array.prototype.odd = function() {
    return this.filter(i => i % 2 != 0);
};
```

## Most upvoted solution

```javascript
Array.prototype.square = function() {
    return this.map(function(n) {
        return n * n;
    });
};
Array.prototype.cube = function() {
    return this.map(function(n) {
        return n * n * n;
    });
};
Array.prototype.average = function() {
    return this.sum() / this.length;
};
Array.prototype.sum = function() {
    return this.reduce(function(a, b) {
        return a + b;
    }, 0);
};
Array.prototype.even = function() {
    return this.filter(function(item) {
        return 0 == item % 2;
    });
};
Array.prototype.odd = function() {
    return this.filter(function(item) {
        return 0 != item % 2;
    });
};
```
