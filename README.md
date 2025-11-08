# swe-sr-1-3

## Setup

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/how-tos/working-with-assignments#how-to-work-on-assignments).

Here are some useful commands to remember.

```sh
npm i                   # install dependencies
git checkout -b draft   # switch to the draft branch before starting

git add -A              # add a changed file to the staging area
git commit -m 'message' # create a commit with the changes
git push                # push the new commit to the remote repo
```
## Question 1

Read the documentation for `findIndex` and `indexOf` on MDN:
- [findIndex](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
- [indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf). 

Explain the difference between the methods and explain when you would choose one over the other. Provide examples to enhance your response.

### findIndex()
The `findIndex()` method returns the first index in an **array** that satisfies the argument given. Otherwise, the method returns `-1`. 
```js
const array = [1, 5, 105, 67, 8];
const memeNum = (element) => element > 67;
console.log(array.findIndex(memeNum));
// output: 2
```

### indexOf()
The `indexOf()` method returns the index in an **array** that matches the element given. Otherwise the method returns `-1`. You can also enter another **parameter**, determining where you want the method to start iterating from.
```js
const array = [1, 5, 105, 67, 8];
console.log(indexOf(67));
// output: 3
console.log(indexOf(67, 4));
// output: 4
```

### When would I use one over the other?
I would use `findIndex()` over `indexOf()` when I am trying to base the index location on an argument. In the example for `findIndex()`, I want to find the first number that is larger than **67** and it was **105** found in the index of `2`. If I just want to find the number `67` in the given array, `indexOf()` is a more simpler method because the method will iterate through the array and spit out the index location of the number `67`.