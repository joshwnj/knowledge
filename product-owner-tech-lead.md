# Product Owner / Tech Lead interactions

I recently set out to scope some new features for a project. As I was hoping to delegate the majority of coding I wanted to remain within a "product owner" role, and leave technical decisions to a tech lead. So I created some "UX stories" to describe a user's goals and how the system operates from their point of view, without going into detail of how I thought it should be implemented. I wrote each scenario as a github issue, and added them all to a new milestone so they could be read as a group.

Here's what I'm finding: in a dev's mind there is often a 1:1 mapping of issue:task. We think _"I will write some code and close that issue"_. But that doesn't work when we're talking about UX stories, because multiple stories might all reference the same feature.

## Proposed workflow

(PO is "product owner", TL is "tech lead")

Here's the kind of workflow I'm trying to get to:

- PO writes Stories
- TL writes as many Tasks as necessary to complete the Stories.
- At this point, there's a discussion between PO and TL. We need to agree that the Tasks adequately describe a journey from A to B (from where we are now, to where we are ready to ship).
- Upon agreement the Tasks can be moved from Backlog to Ready queue for the team to work on

When it comes to prioritizing, there is also a clear split:

- PO determines priority for Stories, with a goal of maximising business value
- TL determines priority for Tasks, with a goal of maximising dev efficiency
