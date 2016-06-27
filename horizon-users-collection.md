# horizon users collection

It's pretty common to create a table called `users` in your database. But probably don't add stuff to the `users` collection in [horizon](https://horizon.io), think of a different name.

Reason: the `users` collection is managed internally by horizon.  When you start horizon with an empty db it populates the `users` collection with:

```
[
  { groups: [ 'admin' ], id: 'admin' }
]
```
