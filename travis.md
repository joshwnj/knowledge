# travis ci

<https://travis-ci.org/>

## detecting the travis environment

`process.env.TRAVIS` is a handy way to tell whether your code is running on travis

## running karma tests in chrome

Previously I only knew how to run karma tests in phantomjs, when using travis. This is fine for some things but falls apart when you need a more realistic browser environment.

Turns out there's a way to use chrome in travis.

- First you need to [add a `before_install` section in the `.travis.yml` config](https://github.com/joshwnj/react-visibility-sensor/pull/54/files#diff-354f30a63fb0907d4ad57269548329e3R7)
- [Tell karma to use chrome when running on the travis environment](https://github.com/joshwnj/react-visibility-sensor/pull/54/files#diff-a2a3b7b0c9c3b4b93b4aebf4e3ec3cfbR52)
- [Configure the `Chrome_travis_ci` browser](https://github.com/joshwnj/react-visibility-sensor/pull/54/files#diff-a2a3b7b0c9c3b4b93b4aebf4e3ec3cfbR55)

Thanks to <https://github.com/eek> for introducing me to this!
