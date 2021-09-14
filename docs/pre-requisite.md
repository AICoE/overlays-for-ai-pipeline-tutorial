# Pre-requisites

In this section, the user can find the requirements needed for the tutorial:

- GitHub account
- GitHub token
- JupyterLab environment with [jupyterlab-requirements][1] library.
- [Elyra][2]
- [Kubeflow Pipeline][3]
- [Tekton][4]

## GitHub account

The project is based on GitHub, if you don't have one just following this [link](https://docs.github.com/en/github/getting-started-with-github/signing-up-for-a-new-github-account).

## GitHub token

If you don't have a GitHub token, you can create one following GitHub docs: [create GitHub token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

## Operate first environment

In [Operate First][2] you can find all components of [Open Data Hub][3], including [JupyterHub][4] to spawn images with [Elyra][2] and [jupyterlab-requirements][1] library, [Kubeflow Pipeline][3] backed by [Tekton][4]. For this tutorial you can select the image called [Experimental Elyra Notebook Image](https://github.com/operate-first/apps/blob/master/kfdefs/base/jupyterhub/notebook-images/experimental-elyra-notebook-imagestream.yaml), which has the library for dependency management already installed.


## References

* [jupyterlab-requirements][1]
* [Operate First][2]
* [Open Data Hub][3]
* [JupyterHub][4]

[1]: https://github.com/thoth-station/jupyterlab-requirements
[2]: https://www.operate-first.cloud/
[3]: https://opendatahub.io/
[4]: https://jupyter.org/hub
