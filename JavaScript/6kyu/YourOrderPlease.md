# Array Helpers

## My Solution

```javascript
function order(words) {
    if (!words) return "";

    let orderWords = [];
    words.split(" ").map(word => (orderWords[word.match(/\d+/)[0]] = word));

    return orderWords.join(" ").trim();
}
```

## Most upvoted solution

```javascript
function order(words) {
    return words
        .split(" ")
        .sort(function(a, b) {
            return a.match(/\d/) - b.match(/\d/);
        })
        .join(" ");
}
```

## Learning

* Extract first number in string by using `string.match(/\d+)[0]`.
