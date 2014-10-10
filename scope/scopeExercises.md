#[Function Scope Exercises](id:xcredit)


#####It is your mission to go through the function.js file and change all the `'???'` in such a way that all the tests pass true. 

###Let's get started...

 
Run the  file in a browser. This document shows one passed test and a series of failing tests.

The **functions.js** folder holds all the failing tests that are being displayed in **SpecRunner.html**. You will be editing this file and using the **SpecRunner.html** to check your progress on making these tests pass. This is just a javascript file so you can use console.log to help debug and inspect these functions.

A test block starts with an `it` function. The `it` function takes two arguments. The first one is a statement describing the rule addressed by the test. The second is a function that will either evaluate to true or false using the `expect` function. The expect statement (`expect(ACTUAL === 'inner').to.be.true;`) will evaluate if the statement between the parens `ACTUAL === 'inner'` is true. You can almost read it like plain English. The expect statement below "expects that the variable ACTUAL equals the value 'inner' to be true".

####Failing Test Example

      it('a function has access to its own local scope variables', 
     
      function () {
        var fn = function () {
          var name = 'inner';
          ACTUAL = name;
        }; 
        fn();
        expect(ACTUAL === '???').to.be.true; 
        //change '???' to what ACTUAL evaluates to.
      });
      
####Passing Test Example

      it('a function has access to its own local scope variables', 
     
      function () {
        var fn = function () {
          var name = 'inner';
          ACTUAL = name;
        }; 
        fn();
        expect(ACTUAL === 'inner').to.be.true; 
        //changed '???' to 'inner' 
        //(because we assigned ACTUAL, a global variable to name inside fn)
      });
      
### Don't forget..
To read all code to try to understand how the whole testing process works. Welcome to programming :)

---
