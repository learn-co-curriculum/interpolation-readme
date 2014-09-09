# Global Substitution and String Interpolation

### .gsub

The `.gsub` method is a handy ruby tool that allows you to `globally substitute` one or more words, or letter for another. Let's take a look at how that works.

We have a fact about a bug assigned to a variable `wrong_fact`:

```ruby
wrong_fact = "Ladybugs can taste with their feet."
```

But wait, that's not a fact about ladybugs, but butterflies! Let's swap out the word "Ladybugs" for "Butterflies" using .gsub. The method `.gsub` takes two `parameters`, the first one the word you want to replace, and the second one is the word you want to replace it with:

```ruby
right_fact = wrong_fact.gsub("Ladybugs", "Butterflies")
```

The `return value` (aka, what this action produces when it's called) will be "Butterflies can taste with their feet." Then, if we type `right_fact` into our console, we'll see the fact correctly printed.

### Chaining .gsubs

What if you have a sentence that you want to substitute more than one word in? We can do that by calling `.gsub` more than once on the same line, through a process called `method chaining`. Take a look:

```ruby
wrong_fact = "Cats fail to recover about 50 percent of the nuts they bury."
true_fact = wrong_fact.gsub("Cats", "Squirrels").gsub("50", "74")

```

### String Interpolation

`.gsub` is great, but there's another super flexible way to do this (you'll see why in our exercise later). We do this by knowing the word we want to interpolate in our sentence already. We wrap that word like #{this}.

Let's say have this question on your biology test:

"A group of flamingos is called a #{answer}."

Then you make `answer` a variable, and assign it to the answer:

`answer = "Flamboyance"`


Note that here we're declaring the variable `answer` before we call `puts`. We need to do it in this order, because our program is read by the computer sequentially. When our computer gets to `#{answer}`, it won't know what that is if answer isn't known yet.

Some Rubyists write this another way, like this:

```ruby
answer = "Flamboyance"
puts "A group of flamingos is called a " + answer
```

But personally, we think the first way looks nicer and is easier for your fellow programmers to read.
