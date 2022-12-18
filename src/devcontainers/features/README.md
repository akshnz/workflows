# devcontainer features

A devcontainer feature is a self-contained unit of installation code, container
configuration, and/or settings and extensions designed to enable new development
capabilities in a devcontainer. It is a way to easily add new tools or
capabilities to a devcontainer, which is a container that provides a complete
coding environment with the tools that a project needs. devcontainer features
can be stored as OCI Artifacts in any supporting container registry and
referenced using the same types of identifiers that are used to reference a
container image. They can be added to a devcontainer by including a reference to
them in the devcontainer.json file. devcontainer features are intended to make
it easier to add new tools or capabilities to a devcontainer, ensuring that
anyone accessing the code will have a consistent experience with all the added
tools.

To use a devcontainer feature with your project, you will need to have a
devcontainer set up using an image, Dockerfile, or Docker Compose file and a
devcontainer.json file. The devcontainer.json file is used to define the
metadata and configuration for your devcontainer.

To add a devcontainer feature to your devcontainer, you will need to include a
reference to the feature in the devcontainer.json file. You can do this by
adding a "features" property to your devcontainer.json file and specifying the
devcontainer feature that you want to include.

Here is an example of how you might add a devcontainer feature to your
devcontainer.json file:

```json
{
  "name": "my-project-devcontainer",
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainers/features/go:1": {
      "version": "1.18"
    },
    "ghcr.io/devcontainers/features/docker-in-docker:1": {
      "version": "latest",
      "moby": true
    }
  }
}
```

In this example, the devcontainer includes two features: "go" and
"docker-in-docker". The "go" feature installs the Go programming language, and
the "docker-in-docker" feature enables Docker support within the devcontainer.

To use the devcontainer with your project, you will need to build the
devcontainer using the devcontainer.json file and then start it up. Once the
devcontainer is running, you can use it to develop your project with the added
tools and capabilities provided by the devcontainer features.
