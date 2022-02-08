# Open container's CLI in Docker

Run `docker ps` to show all running/active containers. The thing which we need in this stage is ID.

Then run command below:

```bash
docker exec -it CONTAINER_ID /bin/bash
```

It'll open up directory of the container. In my case it was helpful to run seed file, but there are many different use cases for sure.

Special thanks for [Alisher](https://t.me/naturalBornHunter) (деп рекламный вставкалар толып кетты дейсын гой). Appreciate your time spent on explanation
