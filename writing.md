# writing

I've recently set a goal to do more writing as part of my day-job. Not because it's a natural thing for me, but because I want to get better at it. Not only because writing stuff down forces me to articulate what I think about it, but it's also a way I can share that journey with others.

## format

I think a blog format is most suitable for this (more than a wiki / knowledgebase format) because it lends itself more to ongoing discovery, and figuring things out on the go.

## tools

What simple tools will make it easier?

- quickly create a post file. Shouldn't have to look around for where to put it. Just write.
- quickly link to other posts, and quote them.
- lint markdown for broken links, so we can safely refactor if we need to.

So far I'm leaning towards this:

- every post file follows a pattern of `posts/YYYY/MM/DD/{name}.md`
- sometimes a post will reference a previous post. Editor shortcut is good for creating links.
- can be useful to also have `topics/{name}.md` for a long-running topic summary. Kind of link an anchor, and easy to link to.
- here's a simple bash script to start: you give it a name, it creates the file and opens in your favourite editor: https://gist.github.com/joshwnj/58e3cdac8b7ccf4c41fcff2b3ad3189e
