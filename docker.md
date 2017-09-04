# docker

- [builder pattern](_notes/2017-06/30-012.md)
- [docker npm3 issue](_notes/2017-06/30-013.md)
- [docker-compose volumes and syncing](_notes/2017-06/30-014.md)
- [docker-compose version 2](_notes/2017-06/30-015.md)
- [notes on caching](_notes/2017-07/26-015.md)
- [connect to mysql](_notes/2017-09/04-011.md)

## env vars

I usually have a file that sets the env vars of a container, using `env_file`: https://docs.docker.com/compose/environment-variables/

Sometimes it's helpful to also be able to [export these vars in the host](_notes/2017-08/14-012.md)
