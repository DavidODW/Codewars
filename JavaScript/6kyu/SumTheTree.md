# Sum The Tree

## My Solution

```javascript
function sumTheTreeValues(root) {
    if (root == null) {
        return 0;
    }

    return root.value + sumTheTreeValues(root.left) + sumTheTreeValues(root.right);
}
```

## Most upvoted solution

```javascript
function sumTheTreeValues(root) {
    return !root ? 0 : root.value + sumTheTreeValues(root.left) + sumTheTreeValues(root.right);
}
```
