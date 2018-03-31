## Kitty's First Programming Challenge

We recently started doing some programming challenges on the slack channel with my friends and the challenge was simple yet, very difficult! 

```
Challenge 1: 

Write FizzBuzz in a language you have never used before, OR in the MOST creative way possible! 

For those who do not know these are the rules of FizzBuzz: 
---------------------------------------------------------------------- 
If a number is divisible by 3, print "Fizz", 
If a number is divisible by 5, print "Buzz", 
If a number is divisible by both 3 and 5 print "FizzBuzz", 
If a number is NOT divisible by 3 or 5 print the number
```

I think this was an interesting take on the challenge we got submissions in [lolcode](http://lolcode.org/), [Scratch](https://scratch.mit.edu/), [Obfuscated C#](https://vignette1.wikia.nocookie.net/fantendo/images/c/c0/Ohgodwhy.png/revision/latest?cb=20120405044625), [EmojiCode](http://www.emojicode.org/), and my submission in [KittenLang](kittenlang.org). 

For those who don't know about KittenLang (like me about a week ago) it is a stack based programming language. This means the compiler takes input and pushes that onto the stack so to add and multiplywould be like this: 

```
$ 2
> 2
$ 2
> 2
> 2
$ +
> 4
$ 3
> 3
> 4
$ *
> 12
``` 

So this was an interesting challenge because of the way you have to loop over the range of numbers. To keep the challenge simple a CSV was provided and I wrote the code with 0..100 included in the source :). 

Then I was able to define a function that took an `Int32` as input and spit a `List<Char>` to `stdout` for the user. Below is my code: 

```
#KITTEN LANG

define fizzbuzz (Int32 -> +IO +Fail) -> x: if ( x % 15 = 0 ) { "FizzBuzz" say } elif ( x % 5 = 0 ) { "Buzz" say }  elif ( x % 3 = 0 ) { "Fizz" say } else { x say }

[0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100] \fizzbuzz each
```

You can see how to define the function pretty plainly but calling it with the `\\` preceeding it means that I am calling the entire function on the input,rather than evaluating the expression given incase I definted a function with the same name as a keyword or if the letters themselved were past variables or keywords on the stack. The `each` keyword means that I am running the function on _each_ item of the array. At first I was using the `map` function, which I still believe should work, but that in the langague wiki page (which is imcomplete :(), says that it maps each result to an array I believe since I am returning to `stdout` that was casuing a program and with the way the language was handling strings I could not quite figure out how to utilize the `map` keyword properly for this langauge. 

That was it! A fun little challenge that introduced me into a new langauge and an entirely differnt style of programming. 

