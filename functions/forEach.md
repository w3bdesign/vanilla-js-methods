Here's a basic implementation of the forEach() method in JavaScript:

```
function myForEach(arr, callback) {
  for (let i = 0; i < arr.length; i++) {
    callback(arr[i], i, arr);
  }
}
```
