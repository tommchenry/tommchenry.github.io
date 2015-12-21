---
layout: post
title: Classes Versus Constructors
---

#Classes Versus Constructors

##Ruby classes vs. JavaScript constructor functions

###December 6, 2015

In both Ruby and Javascript, once you get beyond a certain point of complexity, you'll probably want the abilty to produce many instances of the same kind of object. Last week I talked about how Ruby classes are a lot like blueprints for a house or the template for a comics page and how having this plan to work off of means that we can make more and more of the same general object instances with new kinds of specific values. Javascript can kind of do the same thing (but not exactly) by using constructor functions.

The terminology constructor function is easier to remember than "class" because the name tells you what you can expect the function to do: construct an object. When you write a constructor function, you're telling Javascript how to build that object's default instance. You can then interact with and update individual instances without necessarily updating all the instances of that same object. Again, this is all very much like a class in Ruby.

####Syntax

#####Ruby Class

{% highlight ruby %}
class myObjects
  def initialize(instance_variable)
    @instance_variable = instance_variable
  end
{% endhighlight %}

#####Javascript Constructor Function

{% highlight javascript %}
function myObjects(instanceVariable){
  this.instanceVariable = instanceVariable;
}
{% endhighlight %}
Notice the many similarities between these two. After the first line in the Ruby example specifically declares a class of myObjects, the two can be laid next to each other and compared easily. The Ruby def is used to define a method, much how the Javascript function is used to define a function in Javascript. Both are then passed instance_variable as an argument in Ruby or a parameter in Javascript. We then set this value equal to a property that each instance of our object will have. In Ruby we declare a special variable, an instance variable with @instance_variable. In Javascript, we also declare a special kind of variable but the syntax is slightly different: this tells Javascript that this particular value of the property will belong to this particular instance of the object. Imagine telling your constructor function "This time the value of the property will be what's passed in as a parameter.

####Differences

Even though I took pains to lay out how classes in Ruby are used to produce objects, weirdly enough, classes are themselves also objects. Because Ruby classes are objects that are so widely used, Ruby provides a whole bunch of built-in methods and properties for these special class objects.

However, Javascript constructors aren't these robust special objects. They're just functions like other functions, they just happen to produce instances of objects. At our level, the similarities overwhelm the differences, but these Javascript constructor functions wind up being a much more basic version of Ruby classes until you flesh them out with additional properties and methods.