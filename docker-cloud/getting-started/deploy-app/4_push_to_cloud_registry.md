---
description: Push the Docker image to Docker Cloud's Registry
keywords: image, Docker, cloud
redirect_from:
- /docker-cloud/getting-started/python/4_push_to_cloud_registry/
- /docker-cloud/getting-started/golang/4_push_to_cloud_registry/
title: Push the image to Docker Cloud's registry
---

*Skip this step if you don't have Docker Engine installed locally.*

In this step you will take the image that you built in the previous step, and push it to Docker Cloud.

In step 2, you set your Docker Cloud username as an environment variable called **DOCKER_ID_USER**. If you skipped this step, change the `$DOCKER_ID_USER` to your Docker ID username before running this command.

First tag the image. Tags in this case denote different builds of an image.

**Python quickstart**

```bash
$ docker tag quickstart-python $DOCKER_ID_USER/quickstart-python
```

**Go quickstart**

```bash
$ docker tag quickstart-go $DOCKER_ID_USER/quickstart-go
```

Next, push the tagged image to the repository.

**Python quickstart**

```
$ docker push $DOCKER_ID_USER/quickstart-python
```

**Go quickstart**

```
$ docker push $DOCKER_ID_USER/quickstart-go
```

## Verify the image location

After the push command completes, verify that the image is now in Docker Cloud's
registry. Do this by logging in to [Docker Cloud](https://cloud.docker.com) and
clicking  **Repositories** in the left navigation. Your image should appear in
the repository list.

Next: [Deploy the app as a Docker Cloud service](5_deploy_the_app_as_a_service.md).
