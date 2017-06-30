# computed fields in javascript

Situation: we are fetching documents from a database, operating on them, making changes and storing them back in the database.

Let's say we have a document like this:

```
const doc = {
  tastesLikeBacon: true,
  usesArtificialFlavours: false
}
```

And we have a definition of "delicious" that means:

- it tastes like bacon
- it doesn't use artifical flavours

Rather than duplicating information and adding an `isDelicious` field, we want to calculate the value from the other 2 fields.

## Option 1. create a class

```
const a = new Food(doc)
a.isDelicious() ? ... : ...
```

- pros: familiar pattern for a lot of developers
- cons: now we have to keep track of whether we have a class instance or a plain js object, and handling the marshalling for db reads & writes

### Option 2. just use functions

```
foodFuncs.isDelicious(doc) ? ... : ...
```

- pros: no temptation to form an inheritance hierarchy
- con: ?
