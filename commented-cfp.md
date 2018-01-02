    Abstract Title:

    Extensible Input Validation with PureScript

I don't really know what "Extensible Input Validation" means. If I knew a thing or two, I would guess "input validation using extensible effects." But you don't want attendees to have to guess. Don't be so technical here. Be practical and illustrative. For example, "Form Validation in PureScript: Simpler, Better, Faster" or whatever. That is, think about what you want attendees to accomplish, or what using this coding style will accomplish for them, and then you can get into technical details in your summary (or the talk itself). I'm not entirely sure you're talking specifically about "extensible effects" per se here, either.

    Hop Workshop (2h):

    This session could be applicable for a Hop Workshop that begins with an introduction to purescript-validation's Data.Validation.Semigroup module and covers validating the input to a product type and tagging the failures with errors from a closed Sum type.

    This knowledge could be expanded to cover validating input to Sums-of-Products with Data.Validation.Semiring (where the Sum branches represent alternative input constructions) using the same manner of closed Sum type for error tagging.

    The session would conclude with an introduction to using purescript-variant to tag errors with a Variant type, which essentially captures the idea of an open Sum-type using PureScript's row-polymorphism.

    The attendees would walk through an example where one of the previous validators is converted to use a Variant. This would demonstrate how validation functions can be broken up into modules that cover specific primitive forms of validation, but can be used together to form complex validation pipelines with well-typed error messages.

    Some time could also be dedicated to showing how Variant's JavaScript runtime representation makes it amenable to these validation functions being defined in PureScript, but directly called from JavaScript. However, this may be beyond the scope of such a presentation.

I think a 2 hour workshop just covering how to do functional validations in PureScript would be salutary. I would focus on "how validation functions can be broken up into modules that cover specific primitive forms of validation, but can be used together to form complex validation pipelines with well-typed error messages." Why? Because:

    Nobody uses PureScript. Show them a reason why they should. Give them evidence to bring back to their companies.
    This is functional programming. One of the super powers of FP is composition. You're showing how useful that is for an extremely common scenario.
    This is typed functional programming. You're showing how the use of ADTs makes this problem simpler, not more complex, and how the libraries really do most of the heavy lifting for you. Teach the patterns.

This will easily take 2 hours. You can include the Variant stuff as a bonus, if you think it's necessary, but you'll probably get plenty of mileage out of just Semigroup and Semiring. But I would advise that you focus on the practical benefits and not present your talk as if you're going to focus on those concepts, per se. Also, since this is a workshop, make it clear what the hands-on part will be. Don't get ambitious. Two hours flies by like nothing. Believe me.

    Educational Session (50m)

    Alternatively, this session could be reduced in scope so that only a brief introduction to the concept of Data.Validation's Semigroup and Semiring modules would be given. The main focus being on how purescript-variant's row types allow one to build up very modular, extensible validation pipelines.

    Like the Hop Workshop above, some time could be dedicated to showing how these validation functions might be called from JavaScript.

No, don't do this. You'll get halfway through Semigroup and have to deal with a bunch of questions and won't end up showing anything or feeling like you did anything useful. Do a workshop, not a talk. We need more long form PureScript content, and you're on the front lines.

    Content Relevancy

    This session aims to provide attendees of both beginner and intermediate skill levels with some new insight into how statically typed, functional languages can help tackle the problem of complex input validation.

This is fine, but switch the order of emphasis. "Complex input validation is a problem that software engineers face over and over again. We're going to learn how to make solving it with statically typed, functional programming so clear, straightforward, and expressive that it's actually fun. Put composition to work for you and stop writing boilerplate." Or whatever.

Your bullet lists are probably going to be overkill for the application itself, but they can help inform your thinking about it. Here are yours:

        How Product types can be used to represent form input
        How Sum types can be used to represent validation error states
        How Semigroup can be used to accumulate errors over the failing branch of a validation
        How Applicative can be used to chain together successive validation functions and emit either successfully validated output, or a collection of well-typed error messages
        How complex forms with alternative means of construction can be represented as Sums of Products

    For intermediate attendees:

        Why it's necessary that Validation has the "weaker" Applicative instance without a Monad instance
        Why it's useful that Validation only requires Semigroup and not Monoid
        How PureScript's row polymorphism allows for much more modular validation functions through the "open sum types" provided by purescript-variant

I would edit down to:

    How basic algebraic data types help you clearly and reliably represent your data before and after validation
    How to flexibly compose simple validations together into more complex functions depending on your needs
    How the Applicative type class gives you the power to apply your complex validations to form data for free, with parallelizable code thrown in as a bonus.
    How PureScript's row polymorphism allows for much more modular validation functions through the "open sum types" provided by purescript-variant

Skip the pedantry about applicative/monad and semigroup/monoid. The bit about row polymorphism is fine, though I don't know anything about it. Sounds intriguing, though.

Next step: actually produce a rough draft. Avoid passive voice. Avoid abuse of the word "this".
