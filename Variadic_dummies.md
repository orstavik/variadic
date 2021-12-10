## Variadic functions for dummies

### What is a function?

A function is like a little box with a machine inside. Into this box you can put a couple of things and then the machine inside goes *crank, crank* and out pops something or nothing.

`plus` is a good example of a function. `plus` can take two numbers as input, then *crank, crank*, and then out comes another number: the sum of the two inputs. The actual numbers that we pass to the `plus` we call "arguments", and the number that comes out we call the "return" value.

### What is a variadic function?

A variadic function is just like any other function in most respects. It is a box with a machine inside that take some input and then spit out some result. The difference between variadic functions and other functions that are not variadic is only that the number of things that you can put into the box at the same time is unspecified. The same box can crank up and process 2 things, or 2000 things. The number of input is "variable", and therefore the function is called "variadic".

`plus` happens to be a good example of a variadic function. You can pass `plus` two numbers `1` and `2` and it will spit out `3`. But, you can also pass `plus` the 5 numbers `1,2,3,4,5` and it will spit out `15`. And this is not difficult at all! We all know `plus`. Easy. And we all know that `1 + 2 + 3 = 6`. Easy again. And so we all therefore know the simple truth about variadic functions: they are a little box with a machine inside that can take in 2 or 2000 inputs.

### How do kids write variadic functions in school?

In first grade kids learn that `1 + 2 + 3 = 6` is a good, normal way to write `plus` equations. The `plus` function is written as a `+` placed in between the numbers. This `+` is called an "operator", and by writing a list of numbers seperated by the `+` operator, the first-graders write and use the variadic `plus` function. All day long. With ease.

Slightly older kids face bigger numbers: `123 + 456 + 789 = ??`. These numbers are hard to calculate in the head only. So the kids start writing the list of numbers vertically, not horisontally. The vertical alignment enable them to better perform parts of the inner machinery of the `plus` function on the paper too:

```
   123
   456
+  789
-------
= 1368				 
=======
```

> Tip: In your peripheral vision you might have registered that the list of `+` is now only a single `+` at the bottom of the list. That is a good observation!

In school, with pen on squared paper, writing the variadic `+` function vertically is fine. But, in high-school "kids gotta code". The kids start writing the `plus` functions in programming languages, and that is not done with pen on squared paper. Instead, the kids need to write `plus` as "lines of code". We are back to the horisontal format again. And in programming, the `plus` equations can be written in two ways: using the `+` operator or with a `plus` function.

```javascript
var sum1 = 1 + 2 + 3;     // the operator way
var sum2 = plus(1,2,3);   // the function way
```

At first glance, the kids appear to be back where they started: horisontal listing of arguments. But that is not 100% true. One invisible lesson has been gleaned from vertical listing of numbers on squared paper: the input of the `plus` function can be listed without *reusing* the `plus` symbol itself, ie. in the vertical-squared-paper approach each vertical line represents an argument to the `plus` function. And when the kids go back to horisontal they do a similar maneuver, but instead of using the invisible line, they use the visible parenthesis and comma `(` 1 `,` 2 `,` 3 `)` to separate the three arguments.

The "infinite comma" has arrived. It illustrates how we can write the variadic `plus` function *both* using a variadic operator `+` specific for `plus`, but also using a more generic syntax with a function name `plus` with an infinite comma-separated list.

### What is the infinite comma?

The math teacher is however not so clever as we now might think. Because he hasn't conjured the infinite comma out of thin air. In fact, the math teacher knows that the kids already know roughly how the infinite comma works. They are quite good at it actually. 'Cause they have already learned it in a different subject... `English`(!)

In `English` (and most other languages using some version of the latin alphabet) the `,` is used to "list things". We can write `John has a car, a house, a wife, two kids, a dog, and some other problems`. The `,` is infinite. With comma we can give `John` *aaaall* the problems in the world. If we want. And, even though the English teacher is seriously annoyed when the mischievous high-school kid that writes a whole essay as a single sentence with one loooong comma-separated list, she has to concede to the prankster that he has not broken any *syntactic* rule.

> While on this detour into the English classroom, we see again in our peripheral vision that there are *more* variadic operators lying around here. `;` obviously. But what about `.`? Doesn't that list sentences *indefinitely*. And *space* `' '` (and parenthesis `()` (which are a little strange (being recursive (which really is a thing (strange)))). Wow. Ok, we must look into that later. Let's do that when we look at how variadic structures list arguments in time and space and both.

### What did you learn in school today, dear little boy of mine?

A generic format to write variadic functions. As the `plus` function travels through the mind of the kids as they journey through school, from math to English to computer programming, from the `+` operator to the infinite `,`, the concept of both writing and reading variadic structures becomes second nature. To all of us. The comma is *easy*. The `+` is *easy*. And once thought and practiced, so the `plus(1,2,3)` becomes natural, easy, and second nature as well.

The variadic function is tacit knowing. We all know how it works. We read and write simple variadic structures such as `,` and `+` with the utmost ease. But, if put on the spot, we can't put it into words and explain it. So, your kids will learn it. But if you ask them what they learned in school today, they will never say "infinite comma" nor "variadic functions". So. When you ask your kid "what did you learn in school today, dear little boy of mine"? And he answers "nothing..". Then don't be angry, but instead take comfort in that he probably practiced his tacit knowing of variadic syntax.


## Part two: different variadic functions

### `plus` and `minus`. And `multiply` and `divide`.

Ok. `plus` is variadic. But is `minus` also a variadic function?

For example, if we look at an equation like `52-4-3-2-1 = 42`, there seems to be no end in sight for how many numbers we can throw into a `minus` function at the same time. And in fact, `minus` is a variadic function.

And `minus` is also slightly different from `plus`. We can sense it. But what is it? Well, with `plus` all the arguments are the same, they are "terms": `plus(term1, term2, term3, ...)`. With `minus`, the first argument is different than the rest of the arguments. The first argument is called the "minuend" while all the rest of the arguments are called "subtrahend"s: `minus(minuend, subtrahend1, subtrahend2, subtrahend3, ....)`.

In simple terms, the minuend number has a positive "+" value, all the "subtrahend" numbers have a negative "-" value. And so the inner mechanics of the `minus` machine-in-the-box-function is to take the special first input and cut off the equivalent of each of the other arguments coming in:
```
+ 52    legged centipede (minuend)
-  4    cut off 4 legs   (subtrahend)
-  3    cut off 3 legs   (subtrahend)
-  2    cut off 2 legs   (subtrahend)
-  1    cut off 1 leg    (subtrahend)
-------------------------------------
= 42   legged centipede  (remains of the minuend)
```

And. Same goes for `multiply` (`*`) and `divide` (`/`). The machinery inside these four mathematical operations are of course different. But in terms of their variadic structure, `multiply` behaves *exactly* as `plus`: "the order of factors does not alter the product", and neither does the order of terms. And `divide` also treats its arguments the *exact* same way as `minus`: the "dividend" is the "minuend" equivalent. Yes. It is that simple. Yes, *that is exactly the thing that you have **felt** your entire life, but never really knew how to put into words*.

### The most important one: `append`

Now, for the school kids, these basic arithmetic operations are the most important variadic structures in their life. Next to the infinite commas and periods in plain English. But. For computer programmers there is *one* variadic function that rain supreme and trump all its arithmetic brethren: `append` to list.

Now, for those of us not intimately familiar with the practice of programming, this might come as a bit of a surprise. And so I would need to explain a little why the `append` to list is such an important operation that it trumps even basic arithmetic in value and precedence. Computer programming can in many ways be considered the art of list-making. Some programmers even think that programmers *only* should think about what they do as operations on lists. But the basic concept is that computer programs enable us humans to make small virtual robots that can move things around in a memory space. The things they move around can be anything, numbers, letters, pixels, sound, motion, smell, stars, and atoms. If you can think it, we can make a model of it in a memory. And the core model for such a memory space is, yes you guessed it, a list. And the most important operation we do on that list, yes you guessed it again, `append`. Furthermore, most modern programming environments automatically remove unused lists, so-called garbage-collection. This means that you can write long, complex, really good apps by *only* `append`ing and *never* `remove`ing elements from lists (many developers, myself included, actually consider such an approach better than having developers write code that tries (and often fails) to clean up after itself). And that is why *lists* and *`append` to lists* plays such a unique role in programming. Phu..

So. `append`. We have a list, and then we are going to `append` and an element at the end of that list. And then we are going to `append` a second element. And then we are going to `append` elements three, four, and five. Somehow, this reminds us of `plus`ing. Except that there is not really that much machinery going on. When we are `append`ing elements on a list, the function-is-a-box-with-a-machine is more like the function-is-just-a-box. We have a box, ie. the list, and then we put a thing inside it. That's all. No machinery really, just a box.

Let's look at an example of what this looks like in JavaScript. First, we need to know that in JS we can write lists using square brackets and commas: `[ x , y , z ]`. Second, in JS the `append` function is called `push`. And finally, the `push` function is variadic.

```javascript
var list = [1,2,3];  //list is [1,2,3]
list.push(4);        //list is [1,2,3,4]
list.push(5);        //list is [1,2,3,4,5]
list.push(6, 7);     //list is [1,2,3,4,5,6,7]
```

In the example above, we:
1. start by making a little `list` with the numbers `1`, `2`, and `3`,
2. then we append the number `4` at the end of the list (ie. `list.push(4)`),
3. then we append the number `5`, and
4. finally we append the numbers `6` and `7` in one go.
5. The result is a list `[1,2,3,4,5,6,7]`.

> For those of you that feel uncomfortable with the above example, I can only say that I have been there and felt that too. When some random foreign guy presents you with something alien, and then simply expects you to intuit it, and then internalize it, well that is rarely a precursor to a pleasant experience. And I am that guy. But. Don't worry too much about remembering the syntax and understanding every detail. Just look at it for say 10-15 seconds, try to follow the flow, and then things should be ok in the end.

### `append` as operations in space

As the above example progress, we can literally see the list expand. First, the list is three elements long, then four, then five, and then seven. It is like the game "snake" where the little worm slowly grows as it gobbles up element after element while trying to avoid colliding with its own tail.

The `append` is a function that alters *things in space*: `4` is moved into the `list`. And `append` changes space: first `list` has three slots, second it has four, then five, then seven. It is like a `plusOne` function, a function that can only add the number one for each operation.


## Part 3: variadic functions behavior in time

### when time and space move linearly

Ok. We have now come to the part of this "for dummies" article where we are going to explain how "time and space are really one and the same" and how the human mind with somewhat ease can conflate and switch between the two. Nothing out of the ordinary.

First, we start with a variadic `plus` function example. We are going to do `1+2+3+4+5`. Now, we can do that in one operation with 5 arguments, or five operations with one new argument:
```javascript
var sum1 = plus(1,2,3,4,5);  //one operation, 5 arguments
//or
var sum2 = 0;
sum2 = plus(sum2,1);         //five operations, 1 new argument each
sum2 = plus(sum2,2);
sum2 = plus(sum2,3);
sum2 = plus(sum2,4);
sum2 = plus(sum2,5);
```

Both `sum1` and `sum2` end up as `15`. In fact, we can see that it doesn't really matter how many operations we segment the `plus` operations into, the output is always the same. And again, this we already *know*. Nothing new to see here.

So, we move on and look at the `push`. Now, `push` is a little different than `plus` in that the order of the arguments matters. If we do `list.push(7,6)` instead of `list.push(6,7)`, or `list.push(5); list.push(4);` instead of `list.push(4); list.push(5);`, then the resulting list would look different.

But, as with `plus`, it doesn't matter how many individual steps we divide the `push` function into. We make the same list in a single declarative statement, or using only *one* `push` operation, or in seven consecutive `push` operations. In the end `list` is always `[1,2,3,4,5,6,7]`:

```javascript
var list = [1,2,3,4,5,6,7];
//or
var list = [];
list.push(1,2,3,4,5,6,7);  // list = [1,2,3,4,5,6,7]
//or 
var list = [];
list.push(1);
list.push(2);
list.push(3);
list.push(4);
list.push(5);
list.push(6);
list.push(7);              // list = [1,2,3,4,5,6,7]
``` 

Again, this is nothing new. Even with zero programming experience you might be able to intuit this behavior from the examples above. It's like berries on a straw, if your fingers are nimble enough it doesn't matter if you thread the straw one or seven berries at the time. We can say that the space and time move linearly with each other, no matter the length of each step the outcome is the same at each point.

### The time-space-continuum, continued

When time and space follow each other in this way, the human mind quite quickly jumps to conclusions. If a hungry caveman sees four squirrels run down the tree once every ten seconds, you can bet your backside he will try to catch the fifth squirrel in 10,9,8,7,6,... . That's just thinking ahead.

Similarly, when the hungry caveman sees a pack of four squirrels hordes down the tree, he intuits that he can single them out, throw a stone at one of them, and kill it. The mass of four squirrels is not a squirrel river into which stones just sink seamlessly. That's just basic, caveman analysis.

Now, technically, the caveman can be wrong. Squirrel #5 might come early or not at all. Or squirrel #5 might instead be a snake chasing the four squirrels. Similarly, in fictional literature four squirrel river and mega-transformers might exist. For programmers, this is a common problem usually referred to as "a bug" and "not my fault". So, just because the human mind is prone to see such "patterns of time-space-linearity" and "jump" to conclusions in a time-space-continuum, this doesn't mean that the world *must* or *will* conform to such a pattern. Sometimes *thinking ahead* and *basic analysis* will fail you.

> If you are a programmer, especially a programmer developing library functions, this point should catch your interest. How do we make variadic functions that do not confuse our caveman minds and that do not function as snakes or mega-transformer-squirrels in our developers code? If this is your thing, read my article about good and bad design-patterns for variadic functions.

## Part 4: `Homer Simpson giftwraps ...donums.`

No "for dummies" article would be complete without a section on Latin grammar. And how Latin and English grammar can create hybrid words. And how these hybrid words can help us understand some complex programming language syntax such as the `...` spread operator. And so, just to check that box, the final chapter of this article will be to look at **a single word in a single sentence**: `presents` in `Homer Simpson giftwraps presents`.

## Plural and singular in pidgin-Latin

`Homer Simpson giftwraps presents`. Yet again Homer Simpson is being a selfless giftwrapper. And Homer is being generous: it is not just one, singular `present`, but `presents` plural. In English, we signal "more than one" from "just one" by adding an `s` at the end of the noun.

In Latin, the word for `present` is `don-` as in `donate` and `donation`. But Latin distinguishes between singular and plural form of nouns such as `don-` with different endings for *both* the singular and the plural case: `donum` means "just one present" while `dona` means "two or more presents". `-um` signals singular, `-a` signals plural.

However, when Latin words are picked up in English, English morphology must morph with Latin morphology. Sometimes, Latin words are imported in one case, and then English adds its own morphology on top of that. For example: the Latin words such as "museum" originally meant *one* place to "muse". Thus, in Latin, several such places would be "musea". English imported "museum" as a the word stem, and added its own morphology to it. Thus, the English word "museums" is in essence a hybrid of the Latin word "muse-" in its Latin singular case "-um" with the English plural case "-s": "muse-um-s".

For most English speakers, this is no problem. "Museums" is fine. No cognitive conflict. However, for English speakers sensitive to Latin grammar, the contradictory meaning of Latin singular `-um` and English plural `-s` can cause more mental tension. And some English words such as "millenium"/"millenia" have their Latin morphology intact. English-pidgin-latin can be tricky. Singular+plural-case...

## The need for plural+singular

But. plural+singular *could* be useful. When we say `Homer Simpson giftwraps presents`, we do not know if he will put all the presents in one wrapping or wrap each present individually. And, poor Homer, we must here confess that this is a common problem in most households. When the wife tells the husband to "giftwrap the presents to her sister", then far too often the discussion afterwards becomes:
```
husband: "What are you yelling at me for?! If you wanted me to giftwrap them individually, then you should have told me so! You told me 'giftwrap the presents', and that is exactly what I have done!". 
wife: "Why?! Why do I have to tell you everything?! Even my daughter knows that you don't giftwrap the wine inside knitted sweaters!" 
husband: "Why not?! That is perfect, then the bottle is protected by the soft clothes!! But why?! Why are you saying *your* daughter?! Are you saying she is not mine?!"

The altercation turns physical as the curtain lowers, and the audience is left with a sense of impending doom. Then, in front of the curtain, in walks a little girl, carefree and happy.   
```

In English the difference here is signaled by adverbs such as `one by one`, `indvidually`, or `as one`: `Homer Simpson giftwraps presents individually`. But in JavaScript there is a syntactic/morphological mechanism to signal "plural-singular" in just this instance.

## Variadic + spread

In JS, we could write `HomerSimpson.giftWrap(presents)`, given a `HomerSimpson` object that can execute a `giftWrap` function. We imagine the `presents` referring to a list of individual `present` objects.

The problem with the above method is its duality of meaning: if the `presents` is a list, then should the `giftWrap` function extract the elements from this list and put a bow on each element in that list, or should the `giftWrap` function put paper and a bow around all the elements in the list as a whole?

If the `giftWrap` function is made variadic, then this duality disappears. Once variadic, the `giftWrap` method signals that each argument should be interpreted "as one"/atomically, and the function instead rely on the use of the `...` spread operator to signal that a list should be "deconstructed"/interpreted as `one by one`. The result is:
* `HomerSimpson.giftWrap(...presents)` means `Homer Simpson giftWraps presents one by one`.
* `HomerSimpson.giftWrap(presents)` means `Homer Simpson giftWraps presents as one`.

## What?

1. Are verbs variadic?
2. Are there any natural languages that have a similar plural+singular case as JavaScript?

## References

1. [Latin plurals: nouns ending in -um](https://oikofuge.com/latin-plurals-nouns-ending-in-um/)