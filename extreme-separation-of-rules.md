# extreme separation of business rules

Often the business rules and the boilerplate get mixed up. When you review a PR, is it obvious whether the core business logic has changed, or whether it's just a re-jigging of the implementation?

If we could separate the two completely it would make these diffs stand out clearly.

## Proposal

- `src/rules/` is a place for "business modules"
- where possible, modules should export constants and algorithms that describe the expected behaviour. Also use a lot of comments that explain the reasons behind these things, and how different parts of the system relate to each other.
- keep these values & functions as implementation-agnostic as possible.
- if you're using flowtype, this is also a good location for type definitions
- sometimes it's just not possible / practical to express a business rule as a function independent from boilerplate. In that case pseudocode is fine.

If all goes well, when it comes time to write your implementation code you should find that it is mainly declarative, with most (if not all) of the decision-making happening inside the business modules.
