
1. Remove Duplicate characters from String
```js
function removeDuplicateCharacters() {
  var string='priya riya supriya'
  let result= string.split('').filter((item, index, arr)=> {
               return arr.indexOf(item) == index;
               }).join('');
  return result;
}
console.log(removeDuplicateCharacters());
```


2. Remove Duplicate characters from array of element and find the count of an elements using set object
```js
var arr = [55, 44, 55,67,67,67,67,8,8,8,8,8,65,1,2,3,3,34,5];
var unique = [...new Set(arr)]
console.log(unique) //output: [55, 44, 67, 8, 65, 1, 2, 3, 34, 5]
console.log(unique.length) //output: 10
```


3. Write a program to remove duplicate element from an array in different ways.
```js
const numbers = [1, 3, 2, 3, 3, 4, 5];
// 1
function removeDuplicates(arr) {
    let res = []
    for (let i = 0; i < arr.length; i++) {
        if (res.indexOf(arr[i]) == -1) {
            res.push(arr[i])
        }
    }
    return res;
}
// console.log(removeDuplicates(numbers));
```


4. let arr= [1,2,3,4,4,2,5,6]

```js
// using for loop
let newArr= []
for(let i=0; i<arr.length; i++){
    if(!newArr.includes(arr[i])){
        newArr.push(arr[i])
    }
}
console.log(newArr)
```


5. Write a JavaScript program to find duplicate number from an array.
```js
function findDuplicates(arr) {
    let res = {};
    let duplicate=[];
    for (let i = 0; i < arr.length; i++) {
        if(!res[arr[i]]){
            res[arr[i]] = 1;
        }else{
            res[arr[i]]++;
        }
    }
    for(let data in res){
        if(res[data]>1){
            duplicate.push(parseInt(data));
        }
    }

    return duplicate
}

console.log(findDuplicates([1, 2, 3, 3, 4, 5, 5, 6, 7, 8, 8, 9, 9])); // [3, 5, 8, 9]
```


6. Write a function to identify duplicates in an array and return them as a new array.
```js

let arr5= [1,2,3,1,3,4,2,5];
function findDuplicate(arr){
    let res=[];
    for(let i=0; i<arr.length; i++){
        for(let j=i+1; j<arr.length; j++){
            if(arr[i]===arr[j]){
                res.push(arr[i]);
            }
        }
    }
    return res;
}
// console.log( findDuplicate(arr5));
```
