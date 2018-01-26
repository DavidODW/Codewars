# If you can read this...

## My Solution

```javascript
function to_nato(words) {
    return words
        .replace(/(\s)+/gi, "")
        .split("")
        .map(ch => convertToPhoneticAlphabet(ch))
        .join(" ");
}

function convertToPhoneticAlphabet(ch) {
    switch (ch.toLowerCase()) {
        case "a":
            return "Alfa";
        case "b":
            return "Bravo";
        case "c":
            return "Charlie";
        case "d":
            return "Delta";
        case "e":
            return "Echo";
        case "f":
            return "Foxtrot";
        case "g":
            return "Golf";
        case "h":
            return "Hotel";
        case "i":
            return "India";
        case "j":
            return "Juliett";
        case "k":
            return "Kilo";
        case "l":
            return "Lima";
        case "m":
            return "Mike";
        case "n":
            return "November";
        case "o":
            return "Oscar";
        case "p":
            return "Papa";
        case "q":
            return "Quebec";
        case "r":
            return "Romeo";
        case "s":
            return "Sierra";
        case "t":
            return "Tango";
        case "u":
            return "Uniform";
        case "v":
            return "Victor";
        case "w":
            return "Whiskey";
        case "x":
            return "Xray";
        case "y":
            return "Yankee";
        case "z":
            return "Zulu";
    }
    return ch;
}
```

## Most upvoted solution

```javascript
let table = {
    A: "Alfa",
    B: "Bravo",
    C: "Charlie",
    D: "Delta",
    E: "Echo",
    F: "Foxtrot",
    G: "Golf",
    H: "Hotel",
    I: "India",
    J: "Juliett",
    K: "Kilo",
    L: "Lima",
    M: "Mike",
    N: "November",
    O: "Oscar",
    P: "Papa",
    Q: "Quebec",
    R: "Romeo",
    S: "Sierra",
    T: "Tango",
    U: "Uniform",
    V: "Victor",
    W: "Whiskey",
    X: "Xray",
    Y: "Yankee",
    Z: "Zulu"
};

function to_nato(words) {
    return words
        .split("")
        .filter(c => c !== " ")
        .map(c => table[c.toUpperCase()] || c)
        .join(" ");
}
```

## Learning

* Use regex `/(\s)+/gi` to replace all the empty string.
