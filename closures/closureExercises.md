##Closure exercises

1. Write a function, `nonsense` that takes an input `string`. This function contains another function, `blab` which alerts `string` and is immediately called inside the function `nonsense`. `blab` should look like this inside of the `nonsense` function:

	```javascript
	 var blab = function(){
	   alert(string);
	 };
	 ```

1. In your function, `nonsense`, change the immediate call to a setTimeout so that the call to `blab` comes after 2 seconds. The `blab` function itself should stay the same as before.

1. Now, instead of calling `blab` inside of `nonsense`, return `blab` (without invoking it). Call `nonsense` with some string and store the returned value (the `blab` function) in a variable called `blabLater`. Call `nonsense` again with a different string and store the returned value in a variable called `blabAgainLater`.

1. Inspect `blabLater` and `blabAgainLater` in your console. Call them (they are functions!) and see what happens!


1. Write a function with a closure. The first function should only take one argument, someone's first name, and the inner function should take one more argument, someone's last name. The inner function should console.log both the first name and the last name.
	```javascript
	var lastNameTrier = function(firstName){
	   //does stuff
	
	    var innerFunction = function() { 
	        //does stuff
	    };
	    //maybe returns something here
	};
	var firstNameFarmer = lastNameTrier('Farmer'); //logs nothing
	firstNameFarmer('Brown'); //logs 'Farmer Brown' 
	```      
	This function is useful in case you want to try on different last names. For example, I could use firstName again with another last name:

	```javascript
	firstNameFarmer('Jane'); //logs 'Farmer Jane'
	firstNameFarmer('Lynne'); //logs 'Farmer Lynne'
	```       
       

1. Create a `storyWriter` function that returns an object with two methods. One method, `addWords` adds a word to your story and returns the story while the other one, `erase`, resets the story back to an empty string. Here is an implementation:
	```javascript
	var farmLoveStory = storyWriter();
	farmLoveStory.addWords('There was once a lonely cow.'); // 'There was once a lonely cow.'
	farmLoveStory.addWords('It saw a friendly face.'); //'There was once a lonely cow. It saw a friendly face.'
	
	var storyOfMyLife = storyWriter();
	storyOfMyLife.addWords('My code broke.'); // 'My code broke.'
	storyOfMyLife.addWords('I ate some ice cream.'); //'My code broke. I ate some ice cream.'
	storyOfMyLife.erase(); // ''
	
	```  

1. Using the module pattern, design a toaster. Use your creativity here and think about what you want your users to be able to access on the outside of your toaster vs what you don't want them to be able to touch.
		
	```javascript
	var Toaster = function(){
	    //some private methods and properties
	    
	    return {
	      //some public methods and properties, etc
	    };
	};
	```


1. [EXTRA CREDIT] Use the module pattern to design a character in a Super Mario game. Think about what actions you can control in the game and other aspects you can't control directly (example:  you can only affect your health indirectly by eating a mushroom). If you are not familiar with Super Mario, choose another simple game for this example.

1. [EXTRA CREDIT] Why doesn't the code below work? This is a function that should return an array of functions that console.log() each person's name as a string when invoked. Fiddle with this function and inspect how it works, then try to fix it using a closure. Be prepared to explain to a partner how it worked before, and how it works now with a closure. 

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

1. [EXTRA CREDIT] Write a function that takes another function\* as an argument and creates a version of the function that can only be called one time. Repeated calls to the modified function will have no effect, returning the value from the original call. How could you do this without using a closure? Is it even possible? How could you do this with a closure? \*Note: This original input function should *not* have any parameters.
