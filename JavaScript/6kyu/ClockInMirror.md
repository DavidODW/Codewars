# Build a pile of Cubes

## My Solution

```javascript
function WhatIsTheTime(timeInMirror) {
    let [hour, minute] = timeInMirror.split(":");

    hour = parseInt(hour);
    minute = parseInt(minute);

    if (hour % 6 == 0 && minute == 0) {
        return timeInMirror;
    }

    let mirrorMinute = minute == 0 ? minute : 60 - minute;
    let mirrorHour = 12 - hour || hour;

    if (parseInt(minute) > 30 && parseInt(minute) <= 59) {
        mirrorHour -= 1;
    } else if (mirrorMinute > 30 && mirrorMinute <= 59) {
        mirrorHour -= 1;
    }

    if (mirrorHour == 0) mirrorHour = 12;

    return `${formatNumber(mirrorHour)}:${formatNumber(mirrorMinute)}`;
}

function formatNumber(number) {
    return ("0" + number).slice(-2);
}
```

## Most upvoted solution

```javascript
Number.prototype.mod = function(n) {
    return (this % n + n) % n;
};

function whatIsTheTime(mirrored) {
    const [mh, mm] = mirrored.split(":").map(Number);
    const m = (-mm).mod(60);
    const h = (-mh - (m && 1)).mod(12) || 12;
    return [h, m].map(n => ("0" + n).slice(-2)).join(":");
}

const WhatIsTheTime = whatIsTheTime;
```

## Learning

* Format number into two digit number by using `("0" + number).slice(-2)`.
* Convert element in the array to number by using `array.map(Number)`.
* `mod` function that used for negative number.
