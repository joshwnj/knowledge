# Extreme separation of business rules

Often the business rules and the boilerplate of an application get mixed & intertwined.

**Litmus test:** When you review a PR, is it obvious whether the core business logic has changed, or whether it's just a re-jigging of the implementation?

If we could separate the two completely it would make these diffs stand out clearly.

## Proposal

Store all business rules in "business modules".

For example, make a directory like `src/rules/` that contains modules describing different parts of the system (I'm using nodejs as the example platform).

These modules are kind of like documentation, but where possible we should be describing business rules in well-commented code.

### Q. What kinds of things can these business modules export?

- **constants**: this is the easiest place to start. Most of the time we do this anyway, via a config file.
- **algorithms**: export a function that encapsulates a certain business rule. Eg. If you have different shipping rates in months beginning with "J", wrap that up in a function.
- **types**: if you're using flowtype this is a good location for type definitions.
- **pseudocode**: sometimes it's just not possible / practical to express a business rule as a function independent from boilerplate. In that case pseudocode is fine.

Keep these values & functions as implementation-agnostic as possible. You don't want implementation-specific stuff leaking into your business rules. A little bit is ok but avoid it where practical.

Also a good idea to use a lot of comments that explain the reasons behind these things, and how different parts of the system relate to each other. This makes it feel like a hybrid betweeen code & docs. If you're into literate programming this is probably a good use case.

If all goes well, your implementation code should have an overall declarative / boilerplatey flavour to it, with most (if not all) of the decision-making happening inside the business modules.
