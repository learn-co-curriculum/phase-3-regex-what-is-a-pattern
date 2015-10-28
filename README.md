
# RegEx - What Is A Pattern?

## Objectives

- When to use patterns
- Explain a bit of the history of regex, understanding that there are a few different implementations but we use the ruby one, which is based off of perl mostly

## Introduction

Say you're working at your new job as a web developer and your supervisor asks your to build in validation for the email field in the company's signup form. There have recently been a lot of sign-ups with invalid email addresses ("joeflatiron.com", "@helloworld.com", "$%!-adam@gmail.com"). You sit down and come up with a set of rules that any email address should adhere to (stop reading and see how many you can come up with.):

+ Numbers, letters, dashes, and underscores are ok.
+ Uppercase and lowercase letters are ok.
+ `%`, `?`, `$`, `!`, `*` are not valid characters.
+ There must be an `@` separating the local part from the domain part.
+ There must be at least one `.` in the domain (eg. gmail.com)
+ Two dots in a row are not allowed
+ The local (first) part of the email cannot start with a `.`

We now have a **pattern** that we know all email addresses must follow. We use Regular Expressions, or **Regex** to encode these patterns for matching, searching, and substitution. Here's a sample regex for email validation:

```
/[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}/
```

(There are actually a [LOT more rules](https://en.wikipedia.org/wiki/Email_address#Domain_part) to email adresses, but you get the point.)


## About Regex

### History

Regex came about in the 1950's and 1960's in various forms. Among the first appearances of regular expressions in program form was when Ken Thompson built Kleene's notation into the editor QED as a means to match patterns in text files (Wikipedia). Since then, there have been various implementations of Regular Expressions developed. We'll be using Ruby Regular Expressions with is mostly based off the PERL language.

### When to use Regex
Regular expressions are an extremely powerful way to search through strings and blocks of text for specific patterns. They can be used for data validation, searching, mass file renaming, finding records in a database. 