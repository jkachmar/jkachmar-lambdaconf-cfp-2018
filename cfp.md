### Abstract Title

Input Validation in PureScript: Simpler, Safer, and Stronger

### Session Topics
- Languages
- Libraries
- Concepts

### Abstract Summary

#### TODO: This needs to be more better

I've often found myself asking the following questions while writing software:

- How can I write functions that take untyped, unvalidated input and turn it
into something my program can use safely?
- How can I write these functions in such a way that common validation patterns
can be reused in different scenarios?

I propose that strong, statically typed, functional programming provides a very
compelling answer to these questions.  

What this session will cover:

- How basic Algebraic Data Types help you clearly, and reliably, represent your
data before and after validation
- How to build basic validations that can be composed with each other to create
functions that are as simple or as complex as you need them to be
- How the Applicative typeclass gives you the power to apply these complex
validations to form data
- How PureScript's row polymorphism allows us to create extremely modular
validation functions, all while retaining safety of strong, static typing

### Content Relevancy
Complex input validation is a problem that software engineers repeatedly face
in the course of their work. We're going to see how functional programming can
help solve it in a way that's so straightforward, expressive, and reusable that
it's actually fun.
