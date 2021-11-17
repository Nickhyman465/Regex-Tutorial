# Regex Tutorial: Hex Values

This gist-page will teach you all about using a regualar expression to match a hex value.

## Summary

We are going to be discussing regular expressions that can be used for Hex values. On example of one would look like this: `#fddfd2`. Our goal is to have a regular expression that would isolate these kinds of values. The regular express code we have to do this looks something like this:
 `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)


## Regex Components

### Anchors
`^` and `$` are 2 of the anchors we use in of regex for finding a hex value. The `^` anchor will match any line or string that begins with what comes after it. For example: `^bat` will match any string bat in it. Meanwhile, `$` will do the same thing but will match at the end. For example: `abc$` will match any string that ends with abc.

### Quantifiers
The two main quantifiers we will need for the hex value express above are `?` and `{n}`.

The `?` acts like a conditional where the proceding character can only match 0 or 1 times. In our expression above, `/^#?` this part of it makes it so that we can only match the `#` character up to one time.

The `{n}` seeks to match the proceding character `n` times. An example from our example above would look like this: `[a-f0-9]{6}`. The expression will match if there are 6 characters that are between lowercase `a-f` and/or between the numbers `0` and `9`.

### Grouping Constructs
Our grouping constructs are simply binding our statements together so that we can achieve a more unique match. The `()` coupled with the OR operator `|` help us achieve this.

### Character Classes
In our regex example, we have one character class that is used twice: `[a-f0-9]`. A character class matches any character enclosed in brackets.

### The OR Operator
As I mentioned in the grouping section, our regex is contained in a grouping operator, divided by an OR operator `|`. In the group `([a-f0-9]{6}|[a-f0-9]{3})` we have two expresions: `[a-f0-9]{6}` and `[a-f0-9]{3}`. This means that our regex will match either of those two expresions.


## Author
Nicholas Hyman
[GitHub](https://github.com/Nickhyman465)
[Portfolio](https://nick-hyman-portfolio.herokuapp.com/)

