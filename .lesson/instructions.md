# JavaScript Loops 
It is often necessary to have your code repeat itself. For example if you wanted to `log` every letter in the word `Hello` individually you could do it like this

```javascript
console.log("H")
console.log("e")
console.log("l")
console.log("l")
console.log("o")
```

However this is very redundant and the code is only useful for the specific case of `Hello`. Instead we have something called the `while loop`.

Before you get to that you need to understand a few new things.
## Task 1
1.Declare a variable `candy` and assign it `Skittles`

2.Use your log to see what candy.length does

3.Use your log to see what `candy[0]`, `candy[1]`, `candy[2]`
#

You should now know that `length` gives you the amount of letters in the word and `candy[2]` gives you the letter in the `third` position. You read that right, the `third` position. In computer science counting usually starts with 0. So a 2 is actually the third position as you have `0, 1, 2`. As opposed to every other part of your life when you start with 1 and would count `1,2`.

Now that you have that information lets setup your first `while loop`
```javascript
let word = "Hello"//declare and assign variable
let i = 0//starting out our counter
let length = word.length//this will save 5 in i as there is 5 letters in "Hello"
while (i < length) {//if i < length then then run the code in the while block
  console.log(word[i]);//log the 1 letter
  i++//increase i by 1 and save
}
```

The `while loop` first checks to see if i < length. On the first run it is because i = 0 and length = 5. Since it is `true` it will log the letter in the 0(first) position and then increase i by one. It is important to understand that `i++` is the same as `i = i + 1`

The code then starts the loop over at the `conditional statement`. Now i = 1 and length = 5. The condition is still `true` so it runs the code in the block. Logging the letter in the 1(second) position and incrementing i by 1.

The code then starts the loop over again at the `conditional statement`. Now i = 2 and length = 5. The condition is `true` so it runs the code in the block.... and again and again.

Eventually i = 5 and length = 5. The `conditional statement` reads (5 < 5). This is `false`, so the `while loop` exits. In your case the code is complete but if there were more code below it would run that.

## Task 2
Create a `while loop` for your variable `candy`. Log each letter in the word one at a time.
#

You now know how to loop or `iterate` over each letter in a list of letters(word). You also need to know how to `iterate` over a list of the following:

cars, people, sales, test scores, animals, ..., `objects`

In our normal life we call them `lists` but in JS we call them `arrays`. You can think of an array as an accordian folder.

![](assets/folder.jpg)

The tab names are 0,1,2,3,4,...and they can hold all kinds of things inside. On the folder you call them tab names but in JS you call it the `index`

```javascript
let cars = ["Saab", "Volvo", "BMW"];//declare variable and assign it an array
console.log(cars[0])//prints "Saab"
```

You may have noticed that we view the items inside the array in the same way we do for a string `[0]`. You can also assign new things to any position in the array like so

```javascript
let cars = ["Saab", "Volvo", "BMW"];
console.log(cars[0])//->"Saab"
cars[0] = "Toyota"
console.log(cars[0])//->"Toyota"
```

## Task 3 
1.Declare a variable `movies` and assign the movies, Avatar, Matrix, Terminator, Hackers. 

2.Log the third movie

3.Re-assign the third move to "Office Space"

4.Log the third movie
#

If you wanted to you could log all 4 with the `while loop` code you made before. However, you need to learn about the most popular type of loop, the `for loop`.

```javascript
let word = "Hello"//declare and assign variable
for (let i = 0; i < word.length; i++) {
  console.log(word[i])
}
```

As you can see a `for loop` takes the form for(counter; condition; increment). The example above will loop as long as i < cars.length. In many sitautions the `for` and `while` are interchangable. As a general rule you use a `for` when you know how many loops will occur. So this example of `Hello` is really best with a `for loop`. A `while loop` would be best when you don't know how many loops will occur. An example would be if you asked a user what is 5+2 and you keep asking the question until they respond correctly. Exactly how many guesses it will take is unknown and that is why it is better with a `while`. 

## Task 4
Take the `movies` array that you created in task 3 and log each item in a `for loop`
#

## Task 5
Create a while loop that `prompts` the user for the answer of 5+2 and will loop until the answer is correct. If it is incorrect, log `Incorrect, try again`. If it is correct, log `Correct!`

## Task 6
Create a for loop that logs the odd positioned(not odd `indexed`) letters in the word `California` 

Hint: Your going to want to check out the modulus operator
https://www.w3schools.com/js/js_arithmetic.asp
https://www.w3schools.com/js/tryit.asp?filename=tryjs_oper_mod
#