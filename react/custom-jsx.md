# custom elements in react

To make a custom jsx element, one easy way is to wrap it as a single-function component:

```js
const React = require('react')
      
const MyTag = function (props) {
  return React.createElement(props.inline ? 'span' : 'div', props)
}

// then we can use it in jsx:

<div>
  <MyTag>This is rendered as a div</MyTag>
  <MyTag inline>This is rendererd as a span</MyTag>
</div>
```
