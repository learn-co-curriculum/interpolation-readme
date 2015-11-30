# String Interpolation

## Overview

We'll cover when and how to use string interpolation. 

## Objectives

1. Interpolate variables into strings 


## When to Use String Interpolation 

You're a party planner for Beyonce's 35th birthday and you're using Ruby to help you out with the arrangements. There is a variable called `num_of_attendees` and since she's very popular, this variable points to the integer 547. You try and print the value of `num_of_attendees` to the screen with the code below:

```ruby
puts "There are num_of_attendees people coming to Beyonce's birthday party."
```

You expect this to print "There are 547 people coming to Beyonce's birthday party" but instead it prints "There are num_of_attendees people coming to Beyonce's birthday party." Why is this?

Well, that's because variables need to be **interpolated** inside a string to get their value, and not just referenced by their name, to print to the screen. 

## How You Interpolate Variables into Strings

To interpolate, you wrap the variable like `#{this}`. 

Let's try again:

```ruby
puts "There are #{num_of_attendees} people coming to Beyonce's birthday party."
```

This prints `There are 547 people coming to Beyonce's birthday party.`. Yay!

## Additional Practice

Let's drop into IRB and copy and paste the code from the following example. 

Let's say you have a super hard question on your biology test asking you to identify the technical term for a group of flamingos. 



```ruby
answer = "< fill in your answer here >"
puts "A group of flamingos is called a #{answer}."
```

Now, set the `answer` variable equal to `"flamboyance"` and run the following code in IRB: 

```ruby
answer = "flamboyance"
puts "A group of flamingos is called a #{answer}."
```

This prints `A group of flamingos is called a flamboyance.` to the screen.

Note that here you're declaring the variable `answer` before calling `puts`. You need to do it in this order, because our program is read by the computer sequentially. When your computer gets to `#{answer}`, it won't know what that is if `answer` isn't defined yet.

## Another Way to Interpolate Variables into Strings

Some Rubyists write this another way, like this:

```ruby
answer = "Flamboyance"
puts "A group of flamingos is called a " + answer + "."
```

There's debate about the best practice but most people at Learn think the first way looks nicer and is easier for your fellow programmers to read.
