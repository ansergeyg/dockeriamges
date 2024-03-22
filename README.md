# Docker images

Docker images for local development

To build an image run:

Now you need to use buildx:

```
sudo apt install docker-buildx
```

and then:

```
docker buildx build -t myimage --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g) php

```

Note: build time arguments are mandatory. Otherwise image will not build.

---

Should I Use apt or apt-get?

The apt-get command isn’t updated often, and that’s a good thing. It has to maintain backward compatibility. Backward compatibility isn’t such a concern for apt. It is considered and treated as a user-facing command.

For day-to-day use, use apt.

If you script anything to do with package installation, use apt-get. That gives you the greatest chance of portability and compatibility in your scripts.


source: https://linuxhint.com/diff_apt_vs_aptget/

---

Docker image building issues (resolved):
1) https://github.com/docker-library/php/issues/61

2) https://vsupalov.com/docker-shared-permissions/
 1) https://stackoverflow.com/questions/27701930/how-to-add-users-to-docker-container
