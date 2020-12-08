- [X] Write the article
- [ ] Test the code
- [ ] Create Github Gist
- [ ] Review the writing
- [ ] Publish to dev.to
- [ ] Post on linkedin


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
  //This is called the "Reducer function"
  const reducer = (accumulator, currentValue) => (accumulator + currentValue)/2)
  const result = numbers.reduce(reducer)
  console.log(result) // 46
``` 

But there are actually more interesting ways to use reduce.

Let's suppose we got a list of students

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

There is one interesting thing about the reduce method, is that you can use a second parameter besides after the "reducer function". The starting value of the accumulator. 

```javascript
  const startingAccumulator = {
    awarded: [],
    average: [],
    failed: []
  }

  const sortedStudents = students.reduce(reducer, startingAccumulator)
``` 
But how the reducer function will look like? I suggest you to try it by yourself before reading my answer.

But it will be something like this.

```javascript
  //Calculate top students
  const reducer = (accumulator, student) => {
   if (student.grade >= 9) { 
     accumulator.awarded.push(student)
   } else if (student.grade >= 6) {
     accumulator.average.push(student)
   } else {
     accumulator.failed.push(student)
   }
   return accumulator    
  } 

  console.log(sortedStudents)
```

As you can see, there are more ways to use Array.reduce then just `numbers.reduce((a, b)=> return a + b)).



