# principles of css modules

## unique names

- it doesn't matter what the name is, as long as it's guaranteed to be unique
- unique names mean that we always know what a name means. A name never has 2 meanings, or a meaning which is different depending on context.
- css modules achieves this by namespacing each classname (based on the module file path)

## think in components

- css modules is to traditional css as functional composition is to object-oriented inheritance
- composition & inheritance are both ways to define reusable components
- the big difference is that with inheritance we are "extending" the meaning of something, and overriding parts of it. With functional composition we define immutable atoms and group them together to create the meaning we want.

## css modules approach is a mix of traditional css and inline styles

- traditional css approach:
  - define the css style guide as a bunch of classes
  - write your dom elements, and decorate them with css

- inline styles approach:
  - write your dom elements
  - apply whatever styles are neccesary to make it look right

- css modules approach:
  - every element in a component has a name
  - apply styles, or style-guide classes, to those elements


## style child-components by setting props, not adding classes

Instead of:

```
.ParentComponent .ChildComponent {
  /* overrides for color / layout / etc */
}
```

Prefer:

```
<div>
  <ChildComponent color={...} layout={...} />
</div>
```

That way it's up to `ChildComponent` to provide an API that determines how it can be customized.
