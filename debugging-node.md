# debugging node

Recent node versions (eg. v7.9.0) have some great debugging tools built in: https://nodejs.org/api/debugger.html

You can run `node --inspect=9222 my-script.js` and use the interactive debugger in chrome devtools.

You can also use the `--inspect-brk` flag which sets a breakpoint on the first line. For example, if you want to debug a monobrow build:

```
node --inspect-brk=9222 node_modules/.bin/monobrow
```

Once you have the devtools open, you can search the source and set new breakpoints, inspect values, etc. Really helpful way to see what is happening under the hood.
