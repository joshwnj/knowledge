# docker

## volumes in docker-compose.yml

- when you specify a `volumes` field it creates a mapping between a directory on the host, and a counterpart directory in the container
- 2-way sync: any changes to files are reflected in both places, regardless of where they originated

## npm3 issue

[Using Node with Docker](http://blog.cloud66.com/using-node-with-docker)

Has a solution for the `EXDEV: cross-device link not permitted` error that you might see from an `npm install`

## what's the `version: '2'` bit I sometimes see at the top of a `docker-compose.yml`?

At first I was confused by this. Is "version 2" an upgrade, or a downgrade, from where I am now??

Answer: version 3 is the latest, and is the default if you don't specify a version. So don't worry about version 2.

Ref: <https://docs.docker.com/compose/compose-file/#/versioning>
