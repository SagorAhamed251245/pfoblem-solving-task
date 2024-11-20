### 1. **Two Sum (Easy)**

**Problem**: Given an array of integers `nums` and an integer `target`, find two numbers such that they add up to `target`. Return their indices.

```javascript
function twoSum(nums, target) {
  for (let i = 0; i < nums.length; i++) {
    for (let j = i + 1; j < nums.length; j++) {
      if (nums[i] + nums[j] === target) {
        return [i, j];
      }
    }
  }
  return null;
}

// Example
console.log(twoSum([2, 7, 11, 15], 9)); // Output: [0, 1]
```

---

### 2. **Maximum Number in an Array (Easy)**

**Problem**: Given an array `nums`, find and return the largest number.

```javascript
function findMax(nums) {
  let max = nums[0];
  for (let i = 1; i < nums.length; i++) {
    if (nums[i] > max) {
      max = nums[i];
    }
  }
  return max;
}

// Example
console.log(findMax([3, 5, 7, 2, 8])); // Output: 8
```

---

### 3. **Reverse a String (Easy)**

**Problem**: Write a function that reverses a string.

```javascript
function reverseString(str) {
  return str.split("").reverse().join("");
}

// Example
console.log(reverseString("hello")); // Output: "olleh"
```

---

### 4. **Find the Index of an Element (Easy)**

**Problem**: Given an array `nums` and an integer `target`, return the index of the first occurrence of `target` in `nums`, or `-1` if it is not present.

```javascript
function findIndex(nums, target) {
  for (let i = 0; i < nums.length; i++) {
    if (nums[i] === target) {
      return i;
    }
  }
  return -1;
}

// Example
console.log(findIndex([10, 20, 30, 40, 50], 30)); // Output: 2
console.log(findIndex([10, 20, 30, 40, 50], 60)); // Output: -1
```

---

### 5. **Count the Vowels in a String (Easy)**

**Problem**: Write a function to count the number of vowels in a given string.

```javascript
function countVowels(str) {
  let count = 0;
  const vowels = "aeiouAEIOU";
  for (let char of str) {
    if (vowels.includes(char)) {
      count++;
    }
  }
  return count;
}

// Example
console.log(countVowels("Hello World")); // Output: 3
```

---

### 6. **Remove Duplicates from an Array (Easy)**

**Problem**: Write a function that removes duplicates from a sorted array `nums` in place, returning the length of the unique elements.

```javascript
function removeDuplicates(nums) {
  let uniqueIndex = 0;
  for (let i = 1; i < nums.length; i++) {
    if (nums[i] !== nums[uniqueIndex]) {
      uniqueIndex++;
      nums[uniqueIndex] = nums[i];
    }
  }
  return uniqueIndex + 1;
}

// Example
const nums = [1, 1, 2, 3, 3];
console.log(removeDuplicates(nums)); // Output: 3
console.log(nums.slice(0, 3)); // Output: [1, 2, 3]
```

---

### 7. **Merge Two Sorted Arrays (Easy)**

**Problem**: Given two sorted arrays, merge them into a single sorted array.

```javascript
function mergeArrays(arr1, arr2) {
  let i = 0,
    j = 0;
  const result = [];
  while (i < arr1.length && j < arr2.length) {
    if (arr1[i] < arr2[j]) {
      result.push(arr1[i]);
      i++;
    } else {
      result.push(arr2[j]);
      j++;
    }
  }
  return result.concat(arr1.slice(i)).concat(arr2.slice(j));
}

// Example
console.log(mergeArrays([1, 3, 5], [2, 4, 6])); // Output: [1, 2, 3, 4, 5, 6]
```

---

### 8. **Sum of Array Elements (Easy)**

**Problem**: Write a function that returns the sum of all elements in an array.

```javascript
function sumArray(nums) {
  let sum = 0;
  for (let num of nums) {
    sum += num;
  }
  return sum;
}

// Example
console.log(sumArray([1, 2, 3, 4, 5])); // Output: 15
```

---

### 9. **Check for Even Number (Easy)**

**Problem**: Given an integer `num`, check if it is even.

```javascript
function isEven(num) {
  return num % 2 === 0;
}

// Example
console.log(isEven(4)); // Output: true
console.log(isEven(5)); // Output: false
```

---

### 10. **Find the Smallest Number in an Array (Easy)**

**Problem**: Write a function to find and return the smallest number in an array.

```javascript
function findMin(nums) {
  let min = nums[0];
  for (let i = 1; i < nums.length; i++) {
    if (nums[i] < min) {
      min = nums[i];
    }
  }
  return min;
}

// Example
console.log(findMin([5, 2, 9, 1, 7])); // Output: 1
``` 

Each example demonstrates how to use the function along with its expected output for clarity.
