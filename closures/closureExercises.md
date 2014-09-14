##Day 2: Closure exercises
i. Write a function with a closure. The first function should only take one argument, someone's first name, and the inner function should take one more argument, someone's last name. The inner function should console.log both the first name and the last name.
```javascript
var lastNameTrier = function(firstName){
   //does stuff

    var innerFunction = function() { 
        //does stuff
    };
    //maybe returns something here
};
var firstNameBianca = lastNameTrier('Bianca'); //logs nothing
firstNameBianca('Gandolfo'); //logs 'Bianca Gandolfo' 
```      
This function is useful in case you want to try on different last names. For example, I could use firstName again with another last name:

```javascript
firstNameBianca('Smith'); //logs 'Bianca Smith'
firstNameBianca('Johnson'); //logs 'Bianca Johnson'
```       
       

ii. Write a function that has three nested functions, each taking one number as an argument. The inner-most function should return the sum of all three numbers.

iii. Write a function that takes another function as an argument and creates a version of the function that can only be called one time. Repeated calls to the modified function will have no effect, returning the value from the original call. How could you do this without using a closure? Is it even possible? How could you do this with a closure? 

iv. Using the module pattern, design toaster. Use your creativity here and think about what you want your users to be able to access on the outside of your toaster vs what you don't want them to be able to touch.
		
```javascript
var myToaster = function(){
    //some private methods and properties
    
    //some public methods and properties, etc


}
```


v. Use the module pattern to design a character in a Super Mario game. Think about what actions you can control in the game and other aspects you can't control directly (example:  you can only affect your health indirectly by eating a mushroom). If you are not familiar with Super Mario, choose another simple game for this example.

vi. [EXTRA CREDIT] Why doesn't the code below work? This is a function that should return an array of functions that console.log() each person's name as a string when invoked. Fiddle with this function and inspect how it works, then try to fix it using a closure. Be prepared to explain to a partner how it worked before, and how it works now with a closure. 

```javascript
var checkAttendanceFunc = function(nameArr){
	var resultArr = [];
	for(var i = 0; i < nameArr.length; i++){
		resultArr.push(function(){ console.log('Is', nameArr[i], 'present?', i)})
	};
	return resultArr;
};
```
Here is a hint: http://jsfiddle.net/PuEy6/
