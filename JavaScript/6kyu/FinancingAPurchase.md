# Financing a purchase

## My Solution

```javascript
function amort(rate, bal, term, num_payments) {
    let r = rate / 100 / 12;

    let n = r * bal;
    let d = 1 - Math.pow(1 + r, -term);
    let c = n / d;

    let newBalance = bal;
    let princ = 0;

    let int = 0;

    for (let i = 1; i <= num_payments; i++) {
        int = r * newBalance;
        princ = c - int;

        newBalance = newBalance - princ;
    }

    return `num_payment ${num_payments} c ${c.toFixed(0)} princ ${princ.toFixed(
        0
    )} int ${int.toFixed(0)} balance ${newBalance.toFixed(0)}`;
}
```
