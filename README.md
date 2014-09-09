---
tags: readme
language: ruby
resources: 0
track: web development
unit: ruby
lesson: interpolation
---

# String Interpolation

## Introduction

You're a party planner for Beyonce's 34th birthday and you're using Ruby to help you out with the arrangments. There is a variable called `num_of_attendees` and since she's very popular, this variable points to the integer 547. You try and print the value of `num_of_attendees` to the screen with the code below:

```ruby
puts "There are num_of_attendees people coming to Beyonce's birthday party"
```

You expect this to print "There are 237 coming to Beyonce's birthday party" but instead it prints "There are num_of_attendees people coming to Beyonce's birthday party". Why is this?

Well, that's because variables need to be interpolated to get their value, and not just their name, to print to the screen. To interporate, you wrap the variable like #{this}. You try again:

```ruby
puts "There are #{num_of_attendees} people coming to Beyonce's birthday party"
```

This prints "There are 547 people coming to Beyonce's birthday party". Yay!

## Example 2

Let's say have this question on your biology test:

```text
puts "A group of flamingos is called a #{answer}"
```

You make `answer` a variable, and assign it to the word "flamboyance", above the interpolation:

```text
answer = "flamboyance"
puts "A group of flamingos is called a #{answer}"
```

This prints "A group of flamingos is called a flamboyance" to the screen.

Note that here you're declaring the variable `answer` before calling `puts`. You need to do it in this order, because our program is read by the computer sequentially. When your computer gets to `#{answer}`, it won't know what that is if answer isn't known yet.

Some Rubyists write this another way, like this:

```ruby
answer = "Flamboyance"
puts "A group of flamingos is called a " + answer
```

There's debate about the best practice but most people at Flatiron think the first way looks nicer and is easier for your fellow programmers to read.
