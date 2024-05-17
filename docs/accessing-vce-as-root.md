# Accessing an OU VCE as `root`

In the OU VCE containers, user sessions are run as the `ou` user with limited permissions. (Control of services may be enabled using `sudo` permissions and other `sudo` permissions may be added to the build configuration script if required).

Only `root` privilieges supported by `sudo`ers settings are available in the hosted VCE.

However, if the VCE container is run locally, a user may connect to the running container as root. This is particulalry useful for development and maintenance.

- start a container: `docker run --name=demoVCE VCE_IMAGE`
- enter the running container as `root`: `docker exec --user 0 -it demoVCE /bin/bash`
