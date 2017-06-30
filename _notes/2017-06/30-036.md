# jest snapshot testing

I've tried using jest on 2 separate occasions before, and both times found it was either too weird or buggy. This was a while back.

Seems to be a lot more stable now, so maybe 3rd time's the charm? I'm most interested in incorporating snapshot testing into my workflow.

- https://facebook.github.io/jest/docs/tutorial-react.html
- works with plain functions as well as react components. nice.

- ava also has support for snapshot tests (uses jest-snapshot under the hood): https://github.com/avajs/ava#snapshot-testing
- works well too, although when I tried to compare a snapshot I got an error with no stacktrace: `[TypeError: Cannot read property 'split' of null]`
- worthwhile digging into this more later on. But for now might try jest some more and see where that leads.
