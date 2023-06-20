
/* 1. Write a javascript function named is_integer which checks if the passed argument is an integer. You can use any mathematical operator or functions defined in the Math object.*/
   function is_integer(value) {
    return Number.isInteger(value);
  }
  console.log(is_integer(5)); 
  console.log(is_integer(24));
  console.log(is_integer(15)); 
  
  function is_integer(value) {
    return typeof value ==='number' && isFinite(value)&& Math.floor(value)===value;
  }
    console.log(is_integer('15'));
    /* 2. Using the forEach function defined for an array, find the sum of the array of numbers. [function add_all(arr) {...}]*/

    function add_all(arr) {
        let sum = 0;
        arr.forEach(function(num) {
          sum += num;
        });
        return sum;
      }
      
      // Example usage:
      const numbers = [1, 2, 3, 4, 5];
      console.log(add_all(numbers));

  /* 3. Write a JavaScript program to convert temperatures to and from celsius, fahrenheit. [ Use the formula : c/5 = (f-32)/9, where c = temperature in celsius and f = temperature in fahrenheit]*/

function convertFahrenheitToCelsius (celsius) {
    return (celsius* 9/5) +32;
}
function convertCelsiusToFahrenheit (fahrenheit) {

    return (fahrenheit* 9/5) +32;
}
const celsius = 37;
const fahrenheit = convertCelsiusToFahrenheit(celsius);

console.log (fahrenheit);
/*Pounds to kgs*/

function kilogramstopounds (kilograms) {
    return (kilograms* 2.20462);
}
function poundstokilograms (pounds) {
      return (pounds* 0.453592);
}

const kilogram =69;
const pounds = kilogramstopounds(kilogram);
 console.log (pounds);

 function factorial (n){
    if ((n===0) || (n===1)){
        return 1;
    }
    else {
        return (n* factorial(n-1));
    }
 }
    const n = 5;
    answer = factorial(n)
    console.log ("The factorial of " + n + " is " + answer);

function converttocoins (amount) {
    var coins = [25,10,5,2,1];
    var result =[0,0,0,0,0];
    for (var i=0; i<coins.length; i++){
        while (amount>=coins[i]){
            amount -=coins[i];
            result[i]++;

        }
    }
    const amount = 87;
    const result = converttocoins(amount);
    console.log(result);
}

console.log (converttocoins(25));
