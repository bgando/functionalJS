##Day 2: Closure exercises
1. Write a function with a closure. The first function should only take one argument, someone's first name and the inner function should take one more argument, someone's last name. The inner function should console.log both the first name and the last name.

       var lastNameTrier = function(firstName){
           //does stuff

           var innerFunction() {
              //does stuff
           };
           //maybe returns something here
       };
       var name = lastNameTrier('Bianca'); //logs nothing
       
       name('Gandolfo'); //logs 'Bianca Gandolfo' 
       
       
2. Write a function that has three nested functions, each taking one number as an argument. The inner-most function should return the sum of all three numbers.

3. Write a function that takes another function as an argument and ensures it is only called one time. How could you do this without using a closure? How could you do this with a closure. 

4. Using the module pattern, design toaster. Use your creativity here and think about what you want your users to be able to access on the outside of your toaster vs what you don't want them to be able to touch.
		
		var myToaster = function(){
		    //some private methods and properties
		    
		    //some public methods and properties, etc
		
		
		}
	
5. Use the module pattern to design a character in a Super Mario game. Think about what actions you can control in the game and other aspects you can't control directly (example:  you can only affect your health indirectly by eating a mushroom). If you are not familiar with Super Mario, choose another simple game for this example.

6. Why doesn't the code below work? This is a function that should return an array of functions that console.log() each person's name in a string when invoked. Fiddle with this function and inspect how it works then try to fix it using a closure. Be prepared to explain to a partner tomorrow. 

		var checkAttendanceFunc = function(nameArr){
			var resultArr = [];
			for(var i = 0; i < nameArr.length; i++){
				resultArr.push(function(){ console.log('Is', nameArr[i], 'present?', i)})
			};
			return resultArr;
		};

Here is a hint: http://jsfiddle.net/PuEy6/