### Abstract Title

Extensible Input Validation with PureScript

### Session Topics
- Languages
- Libraries
- Concepts

### Abstract Summary

TODO - Fill this section out

### Session Type

This session could potentially be either a Hop Workshop or an Educational 
Session, depending on how interactive or in-depth it ends up becoming.

#### Hop Workshop (2h)
This session could be applicable for a Hop Workshop that begins with an 
introduction to `purescript-validation`'s `Data.Validation.Semigroup` module and
covers validating the input to a product type and tagging the failures with
errors from a closed Sum type. 

This knowledge could be expanded to cover validating input to Sums-of-Products 
with `Data.Validation.Semiring` (where the Sum branches represent alternative 
input constructions) using the same manner of closed Sum type for error tagging.

The session would conclude with an introduction to using `purescript-variant` to
tag errors with a `Variant` type, which essentially captures the idea of an
open Sum-type using PureScript's row-polymorphism. 

The attendees would walk through an example where one of the previous validators
is converted to use a `Variant`. This would demonstrate how validation functions 
can be broken up into modules that cover specific primitive forms of validation, 
but can be used together to form complex validation pipelines with well-typed
error messages.

Some time could also be dedicated to showing how `Variant`'s JavaScript runtime
representation makes it amenable to these validation functions being defined in
PureScript, but directly called from JavaScript. However, this may be beyond the
scope of such a presentation.

#### Educational Session (50m)
Alternatively, this session could be reduced in scope so that only a brief
introduction to the concept of `Data.Validation`'s `Semigroup` and `Semiring`
modules would be given. The main focus being on how `purescript-variant`'s
row types allow one to build up very modular, extensible validation pipelines.

Like the Hop Workshop above, some time could be dedicated to showing how these
validation functions might be called from JavaScript.

### Content Relevancy
This session aims to provide attendees of both beginner and intermediate skill 
levels with some new insight into how statically typed, functional languages 
can help tackle the problem of complex input validation.

For beginner attendees:
- How Product types can be used to represent form input
- How Sum types can be used to represent validation error states
- How `Semigroup` can be used to accumulate errors over the failing branch of a
validation
- How `Applicative` can be used to chain together successive validation 
functions and emit either successfully validated output, or a collection of
well-typed error messages
- How complex forms with alternative means of construction can be represented as
Sums of Products

For intermediate attendees:
- Why it's necessary that `Validation` has the "weaker" `Applicative` instance 
without a `Monad` instance
- Why it's useful that `Validation` only requires `Semigroup` and not `Monoid`
- How PureScript's row polymorphism allows for much more modular validation
functions through the "open sum types" provided by `purescript-variant`
