# css-modulesify with postcss-copy-assets

Goal: combine [css-modulesify](https://github.com/css-modules/css-modulesify/) with [postcss-copy-assets](https://github.com/shutterstock/postcss-copy-assets) so that any assets (like svg, images, fonts) referenced from css files can be automatically copied to the output directory.

After a quick trial it looks like this will work, but we need to update `loader-core` to set a proper `from` and `to` when running the postcss chain (these are necessary to rewrite asset urls).

## other things to check

- [ ] interop with watchify (updating an asset should trigger a re-copy)
