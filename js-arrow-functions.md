# js arrow functions

TIL: arrow functions have no `arguments`: <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#No_binding_of_arguments>

eg.

```js
const arrowFunc = (a, b) => {
  // this doesn't work!
  console.log(arguments)
}

arrowFunc(1, 2)

// ReferenceError: arguments is not defined
```

However, sometimes you might be tricked into thinking it _does_ exist, if your arrow function is inside a normal function:

```js
function normalFunc (arg1) {
  const arrowFunc = (a, b) => {
    // this does work, but gives arguments of `func1`!
    console.log(arguments)
  }

  arrowFunc(1, 2)
}

normalFunc('yay')
// { '0': 'yay' }
```
