#Callback Exercises

1. Write a function, `funcCaller`, that takes a func (a function) and an arg (any data type). The function returns the func called with arg(as an argument).

1. Write a function, `firstVal`, that takes an array, `arr`, and a function, `func`, and calls `func` with the first index of the `arr`, the index # and the whole array.

1. Change `firstVal` to work not only with arrays but also objects. Since objects are not ordered, you can use any key-value pair on the object.

1. [Extra Credit] Write a function, `once`, (see: http://underscorejs.org/#once) that returns a version of the function which can only be called once. 
  ```javascript
    var chargeCreditCard = function(num, price){
      //charges credit card for a certain price
    };
    var processPaymentOnce = once(chargeCreditCard);
    processPaymentOnce(123456789012, 200);
  ```
