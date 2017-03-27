# wireframing

The purpose of a wireframe is not so much to tell us how something will look, but to give an idea of:

- what data will be present
- how the data is grouped and prioritized

So obviously the visual aspect is an important one (grouping and prioritizing is achieved visually) but we can still express a lot of this with text.

## Example

If we wanted to describe a `Tweet` (subcomponent of a `TwitterTimeline`) we might start by listing the data we need to display:

```
- Author avatar
- Author name
- Author handle
- Time
- Body
- Number of replies
- Number of retweets
- Number of likes
```

Next we might split into primary / secondary, to show which fields should be given visual prominance. The split between primary / secondary is dependent on use-case, and we might need to cater for a few of these at once. In this case let's say our user is browsing a timeline, so the "primary" fields should be those which help to scan for interest:

```
primary:

- Author avatar
- Author name
- Body

secondary:

- Author handle
- Time
- Number of replies
- Number of retweets
- Number of likes
```
