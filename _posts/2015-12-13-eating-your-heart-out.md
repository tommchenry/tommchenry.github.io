---
layout: post
title: Eating Your Heart Out
---

#Eating Your Heart Out

##Recursion and You (and Recursion)

####December 13, 2015

#####Base Case

If now you feel you understand the basics of recursion, stop reading.

#####Other Cases

Recursion is the snake swallowing its own tail. It's a video camera filming a screen that's displaying the feed from the video camera. It's a story about a dark and stormy night where a vampire tells a story about a dark and stormy night where a vampire tells a story about a dark and stormy night where -- you get the idea.

See how I had to cut off with that last example, or it could run forever? That's the secret to recursion. Remember when we first learned about while loops and there was the dire warning that you have to have some sort of iterator or break on a while loop or it will run forever?

Recursion essentially harnesses the power of infinite loop errors and uses it for good.

We do this by having a function call itself inside itself. The method will run and at some point call the method within itself which will then call the method within that version of the method. You're probably thinking, "Won't that break everything?" And it will!

The secret of recursion and what keeps it from being an infinite loop is the base case. The base case is the most basic possible return value. If you're recursioning a giant list of numbers, it's probably the zero or one value. The base case of the snake eating its tail is when there's no more snake to eat. The base case of the vampire telling a story about a dark and stormy night is my "--you get the idea" (the point where my patience for retyping the phrase hit zero).

The base case is the first thing you'll want to work out. Then you have to work out the rules that apply to all the other cases before the case calls itself again. If this seems confusing, another way to think of it is that some programming languages don't have for loops and rely on recursion to loop. For a virtual for loop, the base case would be when i = 0 and the final value is returned. The other cases would be to perform any steps you want performed, subtract 1 from i and then call the function again inside itself.

The most difficult prongs of recusion are that you have to take the kinds of loops you normally consider and invert them and you have to work out the syntax to insure that what you will pass up from the many levels deep will be correct.

After you've finished reading this primer on the concept of recursion, check out [this article]().