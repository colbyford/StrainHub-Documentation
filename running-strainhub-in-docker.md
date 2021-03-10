# Running StrainHub in Docker



### Pull the StrainHub Image from Docker

The StrainHub Docker image is hosted on DockerHub: [hub.docker.com/r/cford38/strainhub](https://hub.docker.com/repository/docker/cford38/strainhub).

Simply run the following from your command prompt:

```text
docker pull cford38/strainhub:latest
docker run --name strainhub --rm -p 3838:3838 cford38/strainhub:latest
```

Then, In your browser, navigate to `localhost:3838`.

### Rebuild the StrainHub Docker Image Locally

To build StrainHub's Docker image locally \(which is unnecessary unless you want to make edits to the Docker image\), clone the GitHub repository and navigate to its directory in your command prompt/terminal window, then run the following:

```text
docker build -t strainhub .
docker run --name strainhub --rm -p 3838:3838 strainhub
```

