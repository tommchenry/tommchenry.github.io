---
layout: post
title: Hashing It Out
---

#Hashing It Out

##Hashes and Arrays in Ruby

###November 11, 2015

Hashes and arrays are both very similar concepts. Both are container objects -- literally objects to contain other objects (other stuff) -- and both are indexed, which means that they have a quick and easy way for you to access the stuff contained within them. Both can also grow or shrink in size as you need them to, which makes them very useful for all kinds of situations. In fact, both arrays and hashes are so similar, that Ruby has lots of built in ways to help you pass the collection of stuff contained within one to another and vice-versa because in practice both wind up being used fairly often and the ability to convert information from one to another became essential.

That said, they are distinct types of object, which means they aren't so similar as to be the same thing. There are situations where an array is more useful than a hash just as there are situations where a hash is more useful than an array. To see why, let's look at each one specifically

**Arrays**

Arrays are container objects where the objects are kept in a particular order. Each object, when added to the array, is given a place in a kind of line. If you're new to programming languages this part might be kind of confusing, but the first object in line is number 0, the second is number 1, the third is number 2 and so on all the way to the end of the line and the end of the array.

Now, at any time if you need a specific object from the line, you only need to request it by this number, its index. Unless you do something to alter the ordering or the objects in the array, you'll always be able to use an object by calling on this index. Say you had an array of the days of the week from Sunday to Saturday. Monday is always going to be the day with the index 1, and you can probably know that without opening up the program and looking at the array in detail. This is the sort of situation where having an array excels: it's a super efficient way to grab an object when you're sure if its place in line.

But the index is limited to only integers. It's like if you had access to the library, but only by the Dewey Decimal number and no way to look up by subject, title, or author. Sure, an experienced librarian might know offhand that the novels are all in the 800s somewhere, but probably not the exact number for a certain novel. This hypothetical library has limited usability for the first-time user and isn't super readable.

**Hashes**

Hashes are container objects where the objects aren't kept in a strict order. Instead, each object when added to the hash is given a key. This key works almost exactly like an array's index, except that a key can have any sort of value from an integer (like an array index) to whole strings or any other object type. This allows you to set an explicit relationship between this key object and the value object.

Now at any time, if you need a specific object from the hash, you only need to ask for it by its key. Even if additional keys and values are added, you can always reach the value again by calling on its key. Say we wanted to represent me as a hash. They key "name" could be given the value "Tom" and now whenever we needed to use my name, we'd only have to ask for my hash's name key and the hash would hand us back "Tom."

Contrast this to an array where we'd have to remember which index number we stashed my name under: Was that index 0 or 1? Has anything happened in the program that shifted any of the key values in the array? So using hash keys becomes much more powerful for certain kinds of problems. You can even set default values that will return if your hash hasn't been fully fleshed out with all the correct values for each key yet -- maybe the example me hash is incomplete so asking for the key "age" would return the value "No age given" until I get around to adding an actual value later.

This is all very powerful and may make plain old arrays seem kinda flimsy in comparison, but there's still a lot of value to be had in arrays. Remember the example of using an array of all the days of the week from Sunday to Saturday? There are always going to be seven days in a week, always in a certain order and we all know them in that order from a very young age. The more robust unordered container of a hash doesn't give us much more value for the added complexity. You'd need to declare keys for each day's value, but in an array the numbered index is given upon creation of the array.

Hash keys are also limited by uniqueness. You can only have one key by a given value in a hash. I have two cats, so the me hash can't have a "cat" key, or I'll be leaving one of them out, which is a good way to get hissed at. Sure, we can make a cat-1 key and a cat-2 key, but you can probably see how this sort of thing can get out of hand very quickly.