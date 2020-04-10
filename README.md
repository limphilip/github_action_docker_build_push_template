# [Template] GitHub action: Build and push Docker image on new tag
Template project containing the `yml` file defining a workflow that builds
and pushes the Docker image of the project to GitHub packages and DockerHub
everytime a new tag is pushed. The workflow pushes both an image with the tag
pushed, as well as an update of the `latest` version.

The images are pushed to DockerHub, because there seem to have a 
bug that requires authentification when executing `docker pull` of public
GitHub Docker images (https://github.community/t5/GitHub-Actions/docker-pull-from-public-GitHub-Package-Registry-fail-with-quot/td-p/32782/page/4).


# Repository setup
The following secrets need to be defined in the repository:
* `APP_NAME`: name of the application
* `DH_TOKEN`: token used for DockerHub authentication
* `DH_USERNAME`: username used for DockerHub registry authentication
* `GH_USERNAME`: username used for GitHub registry authentication

