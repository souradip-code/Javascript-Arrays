# Javascript-Arrays



1. Write a JavaScript function to check whether an `input` is an array or not

*******************************************************************************

function checkArray(arr) {
  if (Array.isArray(arr)) {
    return "array";
  }
  else return "not an array";

}
checkArray([1, 2, 3, 4, 5])

2.Write a JavaScript function to clone an array

************************************************

function cloneArray(arr) {
  var newarr =[]
  return newarr.concat(arr)
}
var arr1 =[1, 2, 3, 4, 5]
var arr2=cloneArray(arr1)
arr1.pop()
console.log(arr1)
console.log(arr2)


3.Write a JavaScript function to get the first element of an array. Passing a parameter 'n' will return the first 'n' elements of the array

*************************************************************************************************************************************

function getFirstElements(arr, n) {
  var newarr = []
  for (let i = 0; i < n; i++) {
    if (arr[i] !== undefined) {
      newarr.push(arr[i])
    }
  }
  return newarr
}
console.log(getFirstElements([1, 2, 3, 4, 5], 3))
console.log(getFirstElements([7, 9, 0, -2]));
console.log(getFirstElements([], 3));
console.log(getFirstElements([7, 9, 0, -2], 3));
console.log(getFirstElements([7, 9, 0, -2], 6));
console.log(getFirstElements([7, 9, 0, -2], -3));


4.Write a JavaScript function to get the last element of an array. Passing a parameter 'n' will return the last 'n' elements of the array

**********************************************************************************

function getLastElements(arr, n) {
  return arr.reverse().slice(0, n).reverse()
}
console.log(getLastElements([1, 2, 3, 4, 5], 3))
console.log(getLastElements([7, 9, 0, -2]));
console.log(getLastElements([], 3));
console.log(getLastElements([7, 9, 0, -2], 3));
console.log(getLastElements([7, 9, 0, -2], 6));
console.log(getLastElements([7, 9, 0, -2], -3));


5.Write a simple JavaScript program to join all elements of the following array into a string.

********************************************************************************************

function join_string(arr){

  return arr.join(",")
}
myColor = ["Red", "Green", "White", "Black"];
join_string(myColor)


6.Write a JavaScript program which accept a number as input and insert dashes (-) between each two even numbers. For example if you accept 025468 the output should be 0-254-6-8.

***********************************************************************************************************************************

function withDash(num) {
  var withdash = ''

  for (let i = 0; i < num.length; i++){
    if(num[i]%2===0 && num[i+1]%2===0){
      withdash += `${num[i]}-` 
    }
    else{
      withdash += num[i]
    }
  }
  return withdash

}
withDash('02546')



7. Write a JavaScript program to sort the items of an array.

************************************************************

function sortArray(arr){
  return arr.sort(function(a,b){
    return a-b;
  })
}
sortArray([ -3, 8, 7, 6, 5, -4, 3, 2, 1 ])

**********************************************************************************
8.Write a JavaScript program to find the most frequent item of an array (Important)

**********************************************************************************

function mostFrequent(arr) {
  let valores = {}
  arr.sort().forEach(item => {
    valores[item] = (valores[item] ? valores[item] + 1 : 1)
  });

  const values = Object.values(valores)
  const maxvalues = Math.max(...values)
  const findindex = values.findIndex(function(e1){ return e1===maxvalues})
  console.log(findindex)
    
  return Object.entries(valores)[findindex]

}

mostFrequent([3, 'a', 'a', 'a', 2, 3, 'a', 3, 'a', 2, 4, 9, 3])




9. Write a JavaScript program which accept a string as input and swap the case of each character. For example if you input 'The Quick Brown Fox' the output should be 'tHE qUICK bROWN fOX'

***************************************************************************************************************************************
function swapFirst(str) {
  var arr = str.split(' ')
  var newarr = []
  for (let i = 0; i < arr.length;i++) {
    newarr.push(arr[i].charAt(0).toLowerCase()+arr[i].toUpperCase().slice(1))
  }
  return newarr.join(' ')


}
swapFirst('The Quick Brown Fox')


10. Write a JavaScript program which prints the elements of the following array.

**********************************************************************************
function showList(arr) {
  for (let i = 0; i < arr.length; i++) {
    console.log('row', i)
    for (let j = 0; j < arr[i].length; j++) {
      console.log(arr[i][j])
    }

  }
}


var a = [[1, 2, 1, 24], [8, 11, 9, 4], [7, 0, 7, 27], [7, 4, 28, 14], [3, 10, 26, 7]]
showList(a)

11. Write a JavaScript program to find the sum of squares of a numeric vector

**********************************************************************************

function sumOfSquares(arr){
var sum= 0
  for(let i of arr){
    sum += i*i

  }
  return sum
}
sumOfSquares([1,2,3])


12.Write a JavaScript program to compute the sum and product of an array of integers

**********************************************************************************

function sumOfSquares(arr){
var sum= 0
var mul =1
  for(let i of arr){
    sum += i
    mul *= i

  }
  return console.log(sum,mul)
}
sumOfSquares([1,2,3,4])


13. Write a JavaScript program to add items in an blank array and display the items

**********************************************************************************



















14.Write a JavaScript program to remove duplicate items from an array
 
**********************************************************************************

function removeDuplicates(arr) {
  var newarr = []
  for (let x of arr) {
    if (!newarr.includes(x)) {
      newarr.push(x)
    }
  }
  return newarr
}
removeDuplicates([1, 2, 3, 4, 2, 4, 3, 1, 6, 7, 8, 2, 2, 2, 2])

**********************************************************************************
15. We have the following arrays : Go to the editor
color = ["Blue ", "Green", "Red", "Orange", "Violet", "Indigo", "Yellow "];
o = ["th","st","nd","rd"]
Write a JavaScript program to display the colors in the following way :
"1st choice is Blue ."
"2nd choice is Green."
"3rd choice is Red."

**********************************************************************************
var color = ["Blue", "Green", "Red", "Orange", "Violet", "Indigo", "Yellow"];
var ordinal = ["th","st","nd","rd"];
var output = "";
for (var i = 0; i < color.length; i++) {
	switch(i){
		case 0: output += "1" + ordinal[1] + " choice is " + color[i]+'\n'; break; // you need to fix < b r > codes here.
		case 1: output += "2" + ordinal[2] + " choice is " + color[i]+'\n'; break;
		case 2: output += "3" + ordinal[3] + " choice is " + color[i]+'\n';
    break;
		default: output += i+1 + ordinal[0] + " choice is " + color[i]+'\n'; break;
	}
}
console.log(output)



16. Find the leap years in a given range of years.

**********************************************************************************
function range(startY, endY){
for(let i = startY; i <= endY; i++){
if((i % 4 === 0 && i % 100 !== 0) || (i % 100 === 0 && i % 400 === 0)){
console.log(i)
}
}
}
range(2000,4000)

17. Write a JavaScript program to shuffle an array

**************************************************

function shuffle(arr) {
  for (let i = 0; i < arr.length; i++) {
    var temp;
    let rnd = Math.floor(Math.random() * arr.length)
    temp = arr[i];
    arr[i] = arr[rnd]
    arr[rnd] = temp

  }
  return arr
}
shuffle([1, 2, 3, 4, 5])

18. Write a JavaScript program to perform a binary search
**********************************************************
function binarySearch(arr, n) {
  var min = 0
  var max = arr.length - 1
  while (min <= max) {
    var mid = Math.floor((min + max) / 2)
    if (arr[mid] < n) {
      console.log('if1')
      min = mid + 1
    }
    else if (arr[mid] > n) {
      console.log('if2')
      max = mid - 1
    }
    else if (arr[mid] == n) {
      console.log('if3')
      return mid;
    }
  }
  return `The value doen't exist in the array`;
}

var items = [1, 2, 3, 4, 5, 6, 7, 8]
binarySearch(items, 7)


19.There are two arrays with individual values, write a JavaScript program to compute the sum of each individual index value from the given arrays

**************************************************************************************************************************************



function sumOfArrays(arr1, arr2) {

  var newarr = []
  if (arr1.length > arr2.length) {
    for (let i = 0; i < arr1.length; i++) {
      if (arr2[i] === undefined) {
        arr2[i] = 0
      }

      newarr.push(arr1[i] + arr2[i] + '')
    }
  }
  else if (arr1.length < arr2.length) {

    for (let i = 0; i < arr2.length; i++) {
      if (arr1[i] === undefined) {
        arr1[i] = 0
      }
      newarr.push(arr1[i] + arr2[i] + '')
    }
  }
  else {
    for (let i = 0; i < arr2.length; i++) {
      newarr.push(arr1[i] + arr2[i])
    }
  }



  return newarr
}


array1 = [1, 0, 2, 3, 4];
array2 = [3, 5, 6, 7];
sumOfArrays(array1, array2)







20. Write a JavaScript program to find duplicate values in a JavaScript array

******************************************************************************
function test(arr){
var result = [];
for (var i = 0; i < arr.length-1; i++){
for (var j = i+1; j < arr.length; j++){
if (arr[i] == arr[j] && !result.includes(arr[i])){
result.push(arr[i]);
}
}
}
return result;
}
console.log(test([1, 2, -2, 4, 5, 4, 7, 8, 7, 7, 71, 3, 6]));

21. Write a JavaScript program to flatten a nested (any depth) array. If you pass shallow, the array will only be flattened a single level.

******************************************************************************************************************************************
function flatten(arr){

  var arr1 =arr.toString().split(',').map(Number)
  return arr1
}
console.log(flatten([1, [2], [3, [[4]]],[5,6]]));





22. Write a JavaScript program to compute the union of two arrays

**********************************************************************
function union(arr1, arr2) {
  for (let i of arr2) {
    if (!arr1.includes(i)) {
      arr1.push(i)
    }
  }
  return arr1
}
console.log(union([1, 2, 3], [100, 2, 1, 10]));





23. Write a JavaScript function to find the difference of two arrays

**************************************************************************
function difference(arr1, arr2) {
  arr1 = arr1.toString().split(',').map(Number)
  arr2 = arr2.toString().split(',').map(Number)
  var newarr = [];

  for (let i of arr2) {
    if (!arr1.includes(i)) {
      newarr.push(i)
    }
  }
  return newarr
}
console.log(difference([1, 2, 3, 4, 5], [1, [2], [3, [[4]]], [5, 6]]));





24. Write a JavaScript function to remove. 'null', '0', '""', 'false', 'undefined' and 'NaN' values from an array
*
****************************************************************************************************************

function notinclude(arr) {
  let newarr = []
  for (let i of arr) {
    if (i) {
      newarr.push(i)
    }
  }
  return newarr
}
console.log(notinclude([NaN, 0, 15, false, -22, '', undefined, 47, null]));




25. Write a JavaScript function to sort the following array of objects by title value

************************************************************************************
function arryObjectSort(arr) {
  arr.sort(function(a, b) {
    var x = a.title.toLowerCase();
    var y = b.title.toLowerCase();
    if (x < y) { return -1; }
    if (x > y) { return 1; }
    return 0;
  });
  return arr
}
var library = [
  { author: 'Bill Gates', title: 'The Road Ahead', libraryID: 1254 },
  { author: 'Steve Jobs', title: 'Walter Isaacson', libraryID: 4264 },
  { author: 'Suzanne Collins', title: 'Mockingjay: The Final Book of The Hunger Games', libraryID: 3245 }
];

console.log(arryObjectSort(library))




26 .Write a JavaScript program to find a pair of elements (indices of the two numbers) from an given array whose sum equals a specific target number.

*****************************************************************************************************************************************************
function sumOfConsecutives(arr, value) {
  var newarr = []
  for (let i = 0; i < arr.length - 1; i++) {
    if (arr[i] + arr[i + 1] == value) {
      newarr.push(arr[i], arr[i + 1])
    }
  }
  return newarr

}
var numbers = [10, 20, 10, 40, 50, 60, 70]
var target = 50
console.log(sumOfConsecutives(numbers, target))




27.Write a JavaScript function to retrieve the value of a given property from all elements in an array.

*********************************************************************************************************
function notinclude(arr) {
  let newarr = []
  for (let i of arr) {
    if (i) {
      newarr.push(i)
    }
  }
  return newarr
}
console.log(notinclude([NaN, 0, 15, false, -22, '', undefined, 47, null]));



28. Write a JavaScript function to find the longest common starting substring in a set of strings

**************************************************************************************************

function longest_common(arr) {
  let [a, b] = arr;
  let idx = 1;
  let result = null;
  while (idx <= a.length) {
    if (b.startsWith(a.slice(0, idx))) {
      result = a.slice(0, idx);
      idx++;
    }
    else
      break;
  }
  return result;
}
console.log(longest_common(['go', 'google']))


**********************************************************************************************************************
29. Write a JavaScript function to fill an array with values (numeric, string with one character) on supplied bounds.(Important)

**********************************************************************************************************************
function num_string_range(start, end, step) {
  let a = start.charCodeAt(0)
  let b = end.charCodeAt(0)
  let newarr =[]
  newarr = Array.from({ length: (b - a) / step + 1 }, (_, i) => a + (i * step)).map(x => String.fromCharCode(x));
return newarr
}
console.log(num_string_range('a', 'z', 2));



30. Write a JavaScript function to merge two arrays and removes all duplicates elements.

********************************************************************************************



function merge_array(arr1,arr2){
  for(let i of arr1){
    if(!arr2.includes(i)){
      arr2.push(i)
    }
  }
  return arr2
}
var array1 = [1, 2, 3]; 
var array2 = [2, 30, 1]; 
console.log(merge_array(array1, array2));

31. Write a JavaScript function to remove a specific element from an array.

**********************************************************************************

function remove_array_element(arr, n) {
  var newarr = []
  for (let i of arr) {
    if (i !== n) {
      newarr.push(i)
    }
  }
  return newarr
}
console.log(remove_array_element([2, 5, 9, 6], 5));



32. Write a JavaScript function to find an array contains a specific element

*****************************************************************************


function contains(arr, n) {
  var newarr = []
  for (let i of arr) {
    if (i == n) {
      return true
    }
  }
  return false
}
arr = [2, 5, 9, 6];
console.log(contains(arr, 5));



33. Write a JavaScript script to empty an array keeping the original

********************************************************************

var arr = [1, 3, 6, 3, -5];
console.log(arr);
arr.length = 0;
console.log(arr);



34.Write a JavaScript function to get nth largest element from an unsorted array

*******************************************************************************


function nthHighest(numbers, n) {
    var sorted = numbers.sort(function (a, b) {
        return a-b;
    });
 
    return sorted[n - 1];
}

console.log(nthHighest([43, 56, 23, 89, 88, 90, 99, 652], 1));




35. Write a JavaScript function to get a random item from an array.

*******************************************************************

function randomitem(arr) {
  let rnd = Math.floor(Math.random() * arr.length)
  return arr[rnd]
}
console.log(randomitem([1, 4, 6, 9, 12, 43, 76, 98]))



36. Write a JavaScript function to create a specified number of elements with pre-filled numeric value array

***********************************************************************************************************

function array_filled(num1, n) {

  let array = new Array(num1).fill(n)
  return array;
}
console.log(array_filled(6, 0));
console.log(array_filled(4, 11));




37. Write a JavaScript function to create a specified number of elements with pre-filled string value array

**********************************************************************************************************

function array_filled(num1, n) {

  let array = new Array(num1).fill(n)
  return array;
}
console.log(array_filled(4, 'password'));


38. Write a JavaScript function to move an array element from one position to another.

*************************************************************************************

function move(arr, from, to) {
    var elem = arr.splice(from, 1)[0];
    if (to < 0) to += 1;
    arr.splice(to, 0, elem);
    return arr;
}
console.log(move([10, 20, 30, 40, 50], 0, 2));
//[20, 30, 10, 40, 50]






39. Write a JavaScript function to filter false, null, 0 and blank values from an array

*******************************************************************************

function notinclude(arr) {
  let newarr = []
  for (let i of arr) {
    if (i) {
      newarr.push(i)
    }
  }
  return newarr
}
console.log(notinclude([NaN, 0, 15, false, -22, '', undefined, 47, null]));





40. Write a JavaScript function to generate an array of specified length, filled with integer numbers, increase by one from starting position

*********************************************************************************************************************************************

function array_range(start, len) 
     {
		var arr = new Array(len);
		for (var i = 0; i < len; i++, start++) 
        {
			arr[i] = start;
		}
      		return arr;
}
console.log(array_range(1, 4)); 





41. Write a JavaScript function to generate an array between two integers of 1 step length.

******************************************************************************************
function array_generate(start, end, step) {
  
  const length = Math.floor((end-start)/step)+1
  if(start>end){
    step = -step
  }
  return Array.from(Array(length), (_, i) => start + step * i)
}
console.log(array_generate(1, 10, 2))
console.log(array_generate(-6, 7,2));



42. Write a JavaScript function to find the unique elements from two arrays.

*******************************************************************************

function findUnique(arr1,arr2){
  arr1 = arr1.toString().split(',').map(Number)
  arr2 = arr2.toString().split(',').map(Number)

  let newarr = []

  for(let i = 0;i<arr1.length;i++){
    if(!newarr.includes(arr1[i])){
      newarr.push(arr1[i])
    }
  }
  for(let i = 0;i<arr2.length;i++){
    if(!newarr.includes(arr2[i])){
      newarr.push(arr2[i])
    }
  }
return newarr

}

console.log(findUnique([1, 2, 3], [100, 2, 1, 10]));
console.log(findUnique([1, 2, 3, 4, 5], [1, [2], [3, [[4]]],[5,6]]));

