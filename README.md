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
```javascript
Here are additional problem-solving examples using an array of objects in JavaScript, where each object represents a person:

---

### Example Array
```javascript
const persons = [
  { id: 1, name: 'Alice', age: 25, occupation: 'Engineer' },
  { id: 2, name: 'Bob', age: 30, occupation: 'Designer' },
  { id: 3, name: 'Charlie', age: 28, occupation: 'Teacher' },
  { id: 4, name: 'David', age: 35, occupation: 'Developer' },
  { id: 5, name: 'Eve', age: 22, occupation: 'Artist' }
];
```

---

Here’s an expanded version of your `persons` array with additional data:

```javascript
const persons = [
  { id: 1, name: 'Alice', age: 25, occupation: 'Engineer' },
  { id: 2, name: 'Bob', age: 30, occupation: 'Designer' },
  { id: 3, name: 'Charlie', age: 28, occupation: 'Teacher' },
  { id: 4, name: 'David', age: 35, occupation: 'Developer' },
  { id: 5, name: 'Eve', age: 22, occupation: 'Artist' },
  { id: 6, name: 'Frank', age: 29, occupation: 'Writer' },
  { id: 7, name: 'Grace', age: 27, occupation: 'Scientist' },
  { id: 8, name: 'Hannah', age: 33, occupation: 'Doctor' },
  { id: 9, name: 'Ian', age: 24, occupation: 'Photographer' },
  { id: 10, name: 'Jack', age: 40, occupation: 'Chef' },
  { id: 11, name: 'Kara', age: 26, occupation: 'Musician' },
  { id: 12, name: 'Liam', age: 31, occupation: 'Architect' },
  { id: 13, name: 'Mona', age: 23, occupation: 'Social Worker' },
  { id: 14, name: 'Nathan', age: 36, occupation: 'Pilot' },
  { id: 15, name: 'Olivia', age: 34, occupation: 'Nurse' },
  { id: 16, name: 'Paul', age: 21, occupation: 'Student' },
  { id: 17, name: 'Quinn', age: 29, occupation: 'Entrepreneur' },
  { id: 18, name: 'Rachel', age: 38, occupation: 'Manager' },
  { id: 19, name: 'Steve', age: 37, occupation: 'Lawyer' },
  { id: 20, name: 'Tina', age: 28, occupation: 'Data Analyst' }
];
``` 

### 2. **Find the Oldest Person**
```javascript
const findOldestPerson = () => persons.reduce((oldest, person) => {
  return person.age > oldest.age ? person : oldest;
}, persons[0]);

console.log(findOldestPerson()); 
// { id: 4, name: 'David', age: 35, occupation: 'Developer' }
```

---

### 3. **Find All Persons Within an Age Range**
```javascript
const findByAgeRange = (minAge, maxAge) => {
  return persons.filter(person => person.age >= minAge && person.age <= maxAge);
};

console.log(findByAgeRange(25, 30));
// [ { id: 1, name: 'Alice', age: 25, occupation: 'Engineer' },
//   { id: 3, name: 'Charlie', age: 28, occupation: 'Teacher' },
//   { id: 2, name: 'Bob', age: 30, occupation: 'Designer' } ]
```

---

### 4. **Count the Number of Persons for Each Occupation**
```javascript
const countByOccupation = () => {
  return persons.reduce((count, person) => {
    count[person.occupation] = (count[person.occupation] || 0) + 1;
    return count;
  }, {});
};

console.log(countByOccupation()); 
// { Engineer: 1, Designer: 1, Teacher: 1, Developer: 1, Artist: 1 }
```

---

### 5. **Update the Age of a Person by ID**
```javascript
const updateAgeById = (id, newAge) => {
  const person = persons.find(person => person.id === id);
  if (person) {
    person.age = newAge;
  }
};

updateAgeById(3, 29);
console.log(persons);
// Updated array where Charlie's age is now 29
```

---

### 6. **Check if All Persons Are Above a Certain Age**
```javascript
const areAllAboveAge = (minAge) => persons.every(person => person.age > minAge);

console.log(areAllAboveAge(18)); // true
console.log(areAllAboveAge(30)); // false
```

---

### 7. **Find the Total Age of All Persons**
```javascript
const totalAge = () => persons.reduce((sum, person) => sum + person.age, 0);

console.log(totalAge()); // 140 (sum of all ages)
```

---

### 8. **Sort by Multiple Criteria (Age, then Name)**
```javascript
const sortByAgeAndName = () => {
  return persons.sort((a, b) => {
    if (a.age === b.age) {
      return a.name.localeCompare(b.name);
    }
    return a.age - b.age;
  });
};

console.log(sortByAgeAndName());
```

---

### 9. **Check if Any Person Matches a Condition**
```javascript
const isAnyoneUnder25 = () => persons.some(person => person.age < 25);

console.log(isAnyoneUnder25()); // true
```

---

### 10. **Create a New Array with Custom Keys**
For example, extract only names and ages.
```javascript
const extractNamesAndAges = () => persons.map(person => ({
  name: person.name,
  age: person.age
}));

console.log(extractNamesAndAges());
// [ { name: 'Alice', age: 25 }, { name: 'Bob', age: 30 }, ... ]
```

---

### 11. **Paginate the Results**
```javascript
const paginate = (page, pageSize) => {
  const start = (page - 1) * pageSize;
  return persons.slice(start, start + pageSize);
};

console.log(paginate(1, 2)); 
// First page with 2 results: [ { id: 1, name: 'Alice', age: 25 }, { id: 2, name: 'Bob', age: 30 } ]
```

---

### 12. **Find Duplicate Names (if any)**
```javascript
const findDuplicates = () => {
  const names = persons.map(person => person.name);
  return names.filter((name, index) => names.indexOf(name) !== index);
};

console.log(findDuplicates()); // Empty array if no duplicates
```

---

### 13. **Get Distinct Occupations**
```javascript
const getDistinctOccupations = () => [...new Set(persons.map(person => person.occupation))];

console.log(getDistinctOccupations()); 
// [ 'Engineer', 'Designer', 'Teacher', 'Developer', 'Artist' ]
```

---

 


Each example demonstrates how to use the function along with its expected output for clarity.
