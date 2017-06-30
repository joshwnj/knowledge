# sitespeed

https://github.com/sitespeedio/sitespeed.io

Using docker it's really easy to create a sitespeed report:

```
docker run --privileged --shm-size=1g --rm -v "$(pwd)":/sitespeed.io sitespeedio/sitespeed.io --video --speedIndex https://www.sitespeed.io/
```
