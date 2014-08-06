##Day 3: Callback exercises

1. Use _.each to loop through an array and console.log() all the values. Now use it to console.log() the indices. How would this be different if you were looping through and object?

2. Write a function that searches an array for a value. It takes an array and a value and returns true if the value exists in the array.

		var helloArr = ['bonjour', 'hello', 'hola'];
		
		var checkValue = function(arr, val) {
		  //checks if the val is in arr
		}
		
3. Rewrite checkValue using _.each. Make sure that you have underscore.js included where you are running your code.

3. Write a loop that pushes all the values in an object to an array.

		input: {two: 2, four: 4, three: 3, twelve: 12}
		output: [2, 4, 3, 12]

3. Use _.map to mimic the previous behavior. 

		input: {two: 2, four: 4, three: 3, twelve: 12}
		output: [2, 4, 3, 12]
4. use _.map to return all the even numbers in an array.

		input: [9,8,7,6,5,2]
		output: [8,6,2]
		
