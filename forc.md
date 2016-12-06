# FORC

_"Fear of Removing CSS"_

- Q. why is it often difficult to delete css code?
  - global scope
  - cross-module cascading

- "how easy will this be to remove?" is a helpful question to ask when considering technical debt

- It's vastly easier to add complexity than it is to remove it
  - [Joe Armstrong: "the mess we're in"](https://vimeo.com/97408239)

- golden rule: **you can remove code easily if you know where all of the dependencies are**, and can confirm that nothing depends on it.

- what kinds of things can make it easier?
  - you can remove code easily if you know precisely where all of the dependencies are, and can confirm that nothing depends on it.
  - we already have a dependency tree of js modules, so if we consider css modules as part of this tree it's easy to prove the existence or absence of dependencies
  - avoid cascading from one module to another. Separate concerns so that we put display-logic in js, leaving css for pure styles
  - think about "hidden dependencies". When an html adds something to its `class` attribute, it depends on the css being there. When you write a cascade rule in css, there's a dependency, possibly between multiple css files.
