Here's a JavaScript function that takes an array of numbers and a target number, and returns the index of the target number in the array. It does not use indexOf.

```
function findIndexOfNumber(arr, target) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === target) {
      return i;
    }
  }
  return -1; // If the target number is not found in the array
}
```

```
// Example usage:
const numbers = [1, 2, 3, 4, 5];
const targetNumber = 3;
const index = findIndexOfNumber(numbers, targetNumber);
console.log(index); // Output: 2
```

The findIndexOfNumber function iterates through the input array and checks if each element is equal to the target number. If it finds the target number, it returns the index. If it doesn't find the target number after iterating through the entire array, it returns -1 to indicate that the target number is not present in the array.

---

Here's the refactored code using a forEach loop:

```
function findIndexOfNumber(arr, target) {
  let result = -1;
  arr.forEach((num, index) => {
    if (num === target && result === -1) {
      result = index;
    }
  });
  return result;
}
```

---

And here's the refactored code using a map method:

```
function findIndexOfNumber(arr, target) {
  const resultArr = arr.map((num, index) => {
    if (num === target) {
      return index;
    } else {
      return -1;
    }
  });
  return resultArr.indexOf(target);
}
```

Both of these refactored versions accomplish the same task as the original for loop, but with more concise and readable code.
