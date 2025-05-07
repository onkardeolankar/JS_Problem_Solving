## Count of Occurance of each letter in a input string

- Using map

```js
function countOccurance(str){

  const countValue = new Map();

  for (const char of str) {

    if(countValue.has(char)){
      countValue.set(char, countValue.get(char)+1)
    }else{
      countValue.set(char,1)
    }
    
  }


  countValue.forEach((count,char)=>{
    console.log(`${char}:${count}`);
  })


}

console.log(countOccurance("aabbcc")); //a:2 ,b:2, c:2
```


- Using dictionalry

```js
function countCharacters(input) {
    const counts = {}; // Initialize an empty object to store character counts

    for (let char of input) {
        if (counts[char]) {
            counts[char]++; // Increment the count if the character is already in the object
        } else {
            counts[char] = 1; // Initialize the count for new characters
        }
    }

    // To print the counts in the desired format:
    for (let char in counts) {
        console.log(`${char}: ${counts[char]}`);
    }
}

// Example usage:
const inputString = "abbcccd";
countCharacters(inputString);
```
```js
count the character in string
// input: malyalam
// outout : m:2, a:3, l:2, y:1

function countString(str) {
    let obj = {};
    for (let x of str) {
        if (obj[x]) {
            obj[x] = obj[x] + 1;
        } else {
            obj[x] = 1;
        }
    }
    return obj;
}

// console.log(countString("malyalam"));
```
