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
    disabled: props.isSubmitting || props.isButtonDisabled,
    value: props.isSubmitting ? 'Checking...' : 'Submit'
  }

  const button = (
    <input
      className={styles.button}
      type="button"
      onclick={props.handleClick}
      {...buttonProps} />
  )
```

Now it's easy to see the common props and the props that change.

A variation on this would be to separate the normal case from the edge case, and move towards a slightly more declarative form. That can make the conditional parts stand out even a little more:

```js
  const submittingProps = props.isSubmitting ? {
    disabled: true,
    value: 'Checking...'
  } : {}

  const button = (
    <input
      className={styles.button}
      type="button"
      onclick={props.handleClick}
      disabled={props.isButtonDisabled}
      value="Submit"
      {...submittingProps} />
  )
```

Here we can easily see the default state in `button`, and see what changes when it is submitting.
