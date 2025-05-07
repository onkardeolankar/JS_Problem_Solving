1. String reverse with reversing of individual words

function withoutReverse(){
   var string ="India is my country"
   let result = string.split('').reverse().join('')
   return result
}
console.log(withoutReverse())
// output = "yrtnuoc ym si aidnI"
-----------------------------------------------------------------------------------------
2. String reverse without using inbult function
function Reverse(){
   var string ="India is my country";
   var result="";
   for( var i=string.length-1; i>=0 ; i-- ) {
      result=result+string[i] }
   return result
}
console.log(Reverse())
// output = "yrtnuoc ym si aidnI"
-----------------------------------------------------------------------------------------
3. String reverse without reversing of individual words (Array of elements can be reverse with reverse() method but for string it is won't possible so required to split 
and then join().
function removeDuplicates(){
   var string ="India is my country"
   let result = string.split('').reverse().join('').split(' ').reverse().join(' ')
   return result
}
console.log(removeDuplicates()) 
// output = "aidnI si ym yrtnuoc"