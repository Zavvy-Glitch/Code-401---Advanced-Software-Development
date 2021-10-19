# Node EcoSystem, TDD, CI/CD

## What does Array.map() do?
 - This method will iterate over each element within a given array, automatically returning it in it's original formatting as a brand new array

## What does Array.reduce() do?
 - This method will iterate over each element within a given array and provides a callback function ie: Accumulator. This accumulator can be set to specific value to signify which position you want it to start(index). As the function that is utilizing this method iterates over the elements in the array, it is modified and returned. Once it completes the cycle with the final element it will return the final accumulator value

## Snippets of how to use superagent() to fetch data from URL and log the result

``` 
superagent.get('http://API URL PLACED HERE')
  .then( data => {
    console.log(data.body);
  })
  .catch(error => console.error(error));
  
```

## With async / await syntax

```
async function someFunctionName() {
  let API = await superagent.get('http://API URL PLACED HERE');
  console.log(API.body);
}
someFunctionName();

```

## Explain promises as though you were mentoring a Code 301 level student
 - Promises are an object that may give you a single value. (Abstraction - this would be in a future case) - Promises will either produce a rejected or resolved value
 - There will only be 3 possible outcomes of a promise IE: Pending, Fulfilled, or Rejected
    - Pending (Conditions have not YET been met)
    - Fulfilled (Conditions have been met)
    - Rejected (Conditions WILL NOT be met)

## Are all callback functions considered to be Asynchronous? Why or Why Not?
 - By default callback functions aren't set to be asynchronous
 - Async callbacks are specific to arguments when a function is called
 - Sync callbacks are returned almost immediately
