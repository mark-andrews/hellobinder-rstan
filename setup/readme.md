The `base_image_dockerfile` is the `Dockerfile` to create the base image for the `Dockerfile` used for this binder based project (in parent dir).
Once the image is built, it needs to be pushed to DockerHub or some such, and then the `Dockerfile` in the parent dir needs to be based on it.

Here is how to build it locally and then run the container locally. This can be used to verify it is working as intended.
```
docker build -t hellobinder_with_rstan_test -f base_image_dockerfile
docker run -p 8888:8888 hellobinder_with_rstan_test:latest
```
