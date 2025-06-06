## Find the occurrence in given array in JavaScript

```js
Input:

[5,5,5,2,2,2,2,2,9,4]

Output:

{
  "2":5,
  "4":1,
  "5":3,
  "9":1,
}

```

```js
function countOccurrences(arr) {
  const occurrences = {};

  for (let num of arr) {
    if (!occurrences[num]) {
      occurrences[num] = 1; // If the number hasn't been counted yet, initialize it with 1
    } else {
      occurrences[num]++; // Otherwise, increment the count
    }
  }

  return occurrences;
}

const input = [5, 5, 5, 2, 2, 2, 2, 2, 9, 4];
const output = countOccurrences(input);
console.log(output);
```
Another Approach:

```js
Write a function to count the frequency of each element from given array and return an object with each element and its count.
let arr7 = [1, 2, 3, 1, 3, 4, 2, 5, 5, 4]

function countFrequency(arr){
	let count= {};
  for(let data of arr){
  	if(!count[data]){
    	count[data]=0;
    }
  	count[data]=count[data]+1
  }
  return count;
}

console.log(countFrequency(arr7));
```
Another Approach 2:
```js
Write a JavaScript program to remove all occurrences of a specified character from a given string in JavaScript

function removeAllOccurance_1(str, char) {
    return str.split(char).join("");
}

function removeAllOccurance_2(str, char) {
    const regex = new RegExp(char, 'g');
    return str.replace(regex, '');
}

//    console.log(removeAllOccurance_1("my name is bittu", "i"));  // my name s bttu
//    console.log(removeAllOccurance_2("my name is bittu", "i"));  // my name s bttu
