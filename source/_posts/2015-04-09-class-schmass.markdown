---
layout: post
title: "Class Schmass"
date: 2015-04-09 19:43:38 -0400
comments: true
categories: flatiron, ruby, classes
---

Nine days into my programming education, I am realizing 1. I know jack shit and 2. I am certainly not as clever as I thought. So an approporiate first post would be on a topic which has been challenging me lately: Ruby classes. Let's dive right in shall we?

When you strip Ruby down to its bare bones, I find that it consists simply of two things: objects and methods. Everything in ruby is an object (the number 1, the word "hello") and methods are what you can do to those objects.

For example, you can tell ruby to reverse your name (your name being the object and reverse being the method). It would look something like this:

``` ruby
"Summer".reverse
=> "remmuS" 
```

See? my name in reverse! Cool, huh? But you're asking, "Summer, I thought we were going to talk about classes? GIVE ME CLASSES."

Alright, alright, no need to get all frothy-mouthed. I'm getting there.

Every object in ruby belongs to a specific class. You can check what class it is by simply calling ".class" on an object, like this:

``` ruby
"Summer".class
=> String 

1.class
=> Fixnum 
```

Man, ruby is so smart. It knows that my name in quotes is a string and the number 1 is a number. So why is this important? Well, what class an object is determines what methods you can call on it. Take a look here:

``` ruby
1234.reverse
NoMethodError: undefined method `length' for 1234:Fixnum

"1234".reverse
=> "4321" 
```

When you try to run reverse on a number, ruby doesn't know what you're talking about. If you really wanted to get 4321, you could turn that number into a string by adding quotes around it. So quick recap: classes determine what methods you can use. Strings have their own set of methods, numbers have their own set, arrays have their own set, etc etc. Alright, take a deep breath, you with me? Just one more thing and we're done.

You can make your own class and define the methods which the class can use. With these custom classes, you can do some pretty powerful stuff, what kind of stuff? We'll leave that for another post. Here, I'll provide a very simple example. Let's make a cat class. 

``` ruby
class Cat

  def initialize(name)
    @name = name
  end

  def meow
    puts "meow meow"
  end

end
```

To make an instance of this class (aka, an object), you do this:

``` ruby
newcat = Cat.new("Olivia")

newcat.meow
meow meow
```

Here we also pass this new cat object a name variable containing the name of the cat, Olivia. We can make Olivia meow by simply saying newcat.meow (which will print out "meow meow" to the screen) since we defined this meow method for the cat class.

And that's it for today folks. Back to the grind, and hopefully I'll have much more to share with you soon.


