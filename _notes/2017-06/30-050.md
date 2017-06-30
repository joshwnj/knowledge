# redux

## atomic actions

- each action represents an atomic change to the state
  - rather than naming by what makes most sense from a user's point of view, name the action according to the atomic change it makes
  - atomic, meaning that the state "makes sense" before and after
  - sometimes atomic also means "smallest possible". In this case I think it's ok to start with bigger atoms and split them later.

## binding action creators

- tip: always bind action creators
- [Idiomatic Redux: Why use action creators?](http://blog.isquaredsoftware.com/2016/10/idiomatic-redux-why-use-action-creators/)

## prefer flat stores

I usually find if I have to nest a lot of stuff in a store, it really belongs in multiple stores
