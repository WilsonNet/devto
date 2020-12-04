# Interest ways to use Array Reduce

Generally when I see reduce tutorials it goes something like this:

```javascript
  const numbers = [1, 10, 15, 20];
  const reducer = (accumulator, currentValue) => accumulator + currentValue)
  const result = numbers.reduce(reducer)
  console.log(result) // 46
``` 
If it's not a simple sum, it's something like an

```javascript
  //Calculate the average
  const numbers = [1, 10, 15, 20];
  const reducer = (accumulator, currentValue) => (accumulator + currentValue)/2)
  const result = numbers.reduce(reducer)
  console.log(result) // 46
``` 

But there are actually more interesting ways to use reduce.

Let's suppose we got a list of studnts

```javascript
  //Calculate the average
  const students = [
    {
      name: 'John Desta',
      grade: 10
    },
    {
      name: 'John Desta',
      grade: 10
    },
    {
      name: 'John Desta',
      grade: 10
    },
    {
      name: 'John Desta',
      grade: 10
    },
  ]
``` 
