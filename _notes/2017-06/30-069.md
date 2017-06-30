# writing tool comparison

## factors

- **close-at-hand**: can I quickly send a note or a message, without much setup overhead?
- **casual VS official**: is the medium suited to writing causal messages, as well as official announcements / docs?
- **access granularity**: how detailed can we get with access rules, eg. public / invite-only / predefined groups?
- **clear authorship**: when you view a note or message, is it clear to see who wrote each line?
- **scaling / refactoring**: does the medium become unwieldy with larger groups or longer-term threads?

## scenario: write a message to someone

- could be a question, an FYI, etc

### email

- pro: close at hand
- con: you have to know their email address, and they will get yours
- con: bad for formatting (because you can't predict their client)
- con: bad for long threads and large groups

### slack

- pro: close at hand (assuming recipients are in the same slack)
- con: if starting off as a DM, can't easily invite new people to the discussion. And creating a new private channel for every message is not scalable.
- con: bad for long threads
- con: bad for official docs

### google doc

- pro: you can theme it if you want something "official" looking
- pro: access granularity is mostly ok (assuming everyone has a google login)
- con: takes a few more steps to create a doc, a few more to invite people, a few more if you want to theme it

### github issue

- pro: slightly better for long threads than some others (because you can refactor the original message) but still not great
- con: no granular access. It's either public to the world, or public to people who have access

## scenario: contribute to a group discussion

### email

- con: ok for small things, but quickly becomes unusable with scale
- con: there's no way to keep track of where the discussion is at, without regular "stocktake" messages

### slack

- con: as soon as you reach multiple threads, or nested threads, things get buried
- con: same "stocktake" problem as email

### google doc

- pro: everyone can edit the doc to collab. Unstructured, so you can solve threading issues in a variety of ways (subheadings, etc)
- con: "who said what" problem, unless everyone follows a formatting convention
