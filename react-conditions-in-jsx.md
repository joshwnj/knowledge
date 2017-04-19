# react: conditions in jsx

Let's say we have a submit button. It normally displays _"Submit"_, and if the form is currently being submitted the label changes to _"Checking..."_.

We could do it like this:

```js
  const button = props.isSubmitting ?
    <input
      className={styles.button}
      type="button"
      disabled={true}
      value={'Checking...'} /> :
    <input
      className={styles.button}
      type="button"
      disabled={props.isButtonDisabled}
      value={'Submit'}
      onClick={props.handleClick} />
  }
```

But there's a lot of duplication there. In abstract, the code says _"depending on Condition, render 1 Element or another"_.

We could rewrite it to say _"Render an Element, with varying props based on Condition"_:

```js
  const buttonProps = {
    className: styles.button,
    type: 'button',
    onclick: props.handleClick,
    disabled: props.isSubmitting || props.isButtonDisabled,
    value: props.isSubmitting ?
      'Checking...' :
      `Submit`
  }

  const button = <input {...buttonProps} />
```

Another approach would be to separate the normal case from the edge case. That can make the conditional parts stand out even a little more:

```js
  const buttonProps = {
    className: styles.button,
    type: 'button',
    value: 'Submit',
    onclick: props.handleClick,
    disabled: props.isButtonDisabled
  }

  if (props.isSubmitting) {
    buttonProps.disabled = true
    buttonProps.value = 'Checking...'
  }

  const button = <input {...buttonProps} />
```
