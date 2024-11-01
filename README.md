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
```

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
```

### 3. **Reverse a String (Easy)**

**Problem**: Write a function that reverses a string.

```javascript
function reverseString(str) {
  return str.split("").reverse().join("");
}
```

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
```

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
```

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
```

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
```

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
```

### 9. **Check for Even Number (Easy)**

**Problem**: Given an integer `num`, check if it is even.

```javascript
function isEven(num) {
  return num % 2 === 0;
}
```

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
```

These tasks are designed to be manageable for beginners while helping build problem-solving skills. Let me know if you'd like more similar problems!
