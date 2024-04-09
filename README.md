[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

**Solution**

This function finds the maximum value in the array which is passed in. Using recursion we check check each element in the array by shrinking it using the slice method. Eventualy this will return the only value in the array which we compare to subsequent calls of mystery(). This effectively reduces the size of the array by one element in each recursive call until it reaches the base case of a single element array.

