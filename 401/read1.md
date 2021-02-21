# Node Ecosystem, TDD, CI/CD

1. Describe (in plain English) what Array.map() does
### The map() method creates a new array with the results of calling a function for every array element. The map() method calls the provided function once for each element in an array, in order. Note: map() does not execute the function for array elements without values.

2. Describe (in plain English) what Array.reduce() does
### The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in single output value.

3. Provide code snippets showing how to use superagent() to fetch data from a URL and log the result

## Normal Promise Syntax
### superagent.get(`some API url`)
  .then(data => {
    console.log(data.body)
  })
  .catch(err => console.error(err)

## Async / Await Syntax
### async function someName() {
  try {
    let data = await superagent.get(`some API url`)
    console.log(data.body)
    
  } catch(error) {
     console.error(error)
  }
}

3. Explain promises as though you were mentoring a Code 301 level student

### basically you send out your call to what your doing a promise it will eather finsih what you were trying to do or get rejected and obviously it gets alot more complicated then that

4. Are all callback functions considered to be Asynchronous? Why or Why Not?

### from my understanding no. but in the world of coding you can make anything do anything. so i guess it would be situational and what you needed done.
