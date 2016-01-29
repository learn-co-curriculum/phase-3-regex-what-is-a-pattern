
# RegEx - What Is A Pattern?

## Objectives

- Understand the purpose of patterns and regular expressions
- Learn a bit of Regex history
- Understand that the version of Regex we use is one of many implementations.

## Introduction

Say you're working at your new job as a developer and your supervisor asks you to build in validation for the email field in the company's signup form. There have recently been a lot of sign-ups with invalid email addresses ("joeflatiron.com", "@helloworld.com", "$%!-adam@gmail.com"). You sit down and come up with a set of rules that any email address should adhere to (stop reading and see how many you can come up with.):

+ Numbers, letters, dashes, and underscores are ok.
+ Uppercase and lowercase letters are ok.
+ `%`, `?`, `$`, `!`, `*` are not valid characters.
+ There must be an `@` separating the local part from the domain part.
+ There must be at least one `.` in the domain (eg. gmail.com)
+ Two dots in a row are not allowed
+ The local (first) part of the email cannot start with a `.`

We now have a **pattern** that we know all email addresses must follow. We use Regular Expressions, or **Regex** to encode these patterns for matching, searching, and substitution. Here's a sample regex for email validation:

```
/[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}/i
```
If this doesn't make any sense, don't worry. We'll be covering how to write and read regular expressions shortly.

(There are actually a [LOT more rules](https://en.wikipedia.org/wiki/Email_address#Domain_part) to email adresses, but you get the point.)


## About Regex

### History

Regex came about in the 1950's and 1960's in various forms. Among the first appearances of regular expressions in program form was when Ken Thompson built [Stephen Cole Kleen's](https://en.wikipedia.org/wiki/Stephen_Cole_Kleene) notation into the editor QED as a means to match patterns in text files (Wikipedia). Since then, there have been various implementations of Regular Expressions developed. We'll be using Ruby Regular Expressions which is mostly based off the PERL language.

### When to use Regex
Regular expressions are an extremely powerful way to search through strings and blocks of text for specific patterns. They can be used for data validation, searching, mass file renaming, and finding records in a database. Use them carefully - they are like a surgeon's scalpel: Able to do a lot of harm or good, depending on how well it is wielded.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/regex-what-is-a-pattern' title='RegEx - What Is A Pattern?'>RegEx - What Is A Pattern?</a> on Learn.co and start learning to code for free.</p>
