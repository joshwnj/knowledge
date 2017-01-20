# docker

## volumes in docker-compose.yml

- when you specify a `volumes` field it creates a mapping between a directory on the host, and a counterpart directory in the container
- 2-way sync: any changes to files are reflected in both places, regardless of where they originated

## npm3 issue

[Using Node with Docker](http://blog.cloud66.com/using-node-with-docker)

Has a solution for the `EXDEV: cross-device link not permitted` error that you might see from an `npm install`
