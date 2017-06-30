# reason noob

^ it me

## modules and functions

Coming from a node background, I'm used to thinking of a module as the basic building block of a program. Reason has modules, but it seems slightly different in concept: https://facebook.github.io/reason/modules.html

From what I can see so far, a good place to start is to just declare functions straight up. I mayb find a need for "reason modules" later, but not there yet :)

Looking at the bucklescript output, this:

```reason
let sayHi name => "hello " ^ name ^ "!";
```

produces this:

```js
function sayHi(name) {
  return "hello " + (name + "!");
}

exports.sayHi = sayHi;
```
