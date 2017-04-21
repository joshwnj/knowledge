# working with github pull requests locally

Useful if someone submits a PR on your github project, and you want to try it out locally. Append this line to the `[remote "origin"]` section in your `.git/config` file:

```
	fetch = +refs/pull/*/head:refs/remotes/origin/pr/*
```

So the whole section will now look something like this:

```
[remote "origin"]
	url = git@github.com:joshwnj/monobrow.git
	fetch = +refs/heads/*:refs/remotes/origin/*
	fetch = +refs/pull/*/head:refs/remotes/origin/pr/*
```

Now when you `git pull`, you'll see a bunch of "pr" branches. You can switch to a PR branch with it's ID, like this:

```
git checkout pr/9
```
