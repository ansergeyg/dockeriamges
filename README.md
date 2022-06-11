# Docker images

Docker images for local development

To build an image run:

```
docker build -t image_name_here:version_here php
```
---

Should I Use apt or apt-get?

The apt-get command isn’t updated often, and that’s a good thing. It has to maintain backward compatibility. Backward compatibility isn’t such a concern for apt. It is considered and treated as a user-facing command.

For day-to-day use, use apt.

If you script anything to do with package installation, use apt-get. That gives you the greatest chance of portability and compatibility in your scripts.


source: https://linuxhint.com/diff_apt_vs_aptget/

---

Docker image building issues (resolved):

1) https://github.com/docker-library/php/issues/61