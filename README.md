# Thoth Tutorial - create and use overlays for Elyra AI Pipelines steps.

This tutorial is used to show the concept of overlays, how they are applied to software stacks, what are overlays builds and the use of the built images in AI Pipelines.

`overlays` concept is a way of 'overlaying' common content and selectively change pieces of it for specific configurations. This concept is well established in deployments, for example when you have to deploy in different clusters or you have to deploy different environments in the same cluster (e.g. test, stage). Typically there are some commons base files that can be reused across all overlays and then each overlay will have specific configurations overriding based configurations or adding new pieces to it.

The same concept can be applied during image builds when there are different software stacks or runtime environment to be considered in the same repository. You can have common base piece of codes to be present in images with different software stacks or runtime environment.
The possibility to optimize specific part of your code to perform a specific task is very important nowdays with all the combinations of libraries, operating systems, hardwares.

If we consider some typical steps in Machine Learning lifecycle, for example `downloading dataset`, `processing dataset` or `training a model`, each of this step can be optimized in terms of software stacks and runtime environment. Using overlays concept we can have different software stacks and runtime environment for each of them, we can rely on overlays builds to create specific optimized images for each of these step and use them in an AI pipelines.


## What you will learn with this tutorial?

At the end of this tutorial you will be able to create overlays for your jupyter notebooks, setup [AICoE CI][1] and [Kebechet Bot][2] to automate creation of images for overlays and maintenance of the software stack for each of the overlay. Moreover you will learn how to create and run an AI pipeline using the images created.


## Where you will run this tutorial?

[Operate First][6] is an open infrastructure environment started at Red Hat's Office of the CTO. It has been selected to run this tutorial since it is an open source initiative that fulfills all the requirements stated above. Anyone with a Google account can log in and start developing. To learn more about Operate First, visit the [website](https://www.operate-first.cloud/) or [GitHub community](https://github.com/operate-first).

[Operate First][6] hosts [Open Data Hub][3] with all the tools provided for Data Science projects (e.g. JupyterHub, Elyra, Kubeflow Pipelines, Seldon, Prometheus, Grafana, Superset) running on [Red Hat Openshift][4].


## Why does the tutorial repository have this structure?

The project template used can be found here: [project template][1]. It shows correlation between a data scientist needs (e.g. data, notebooks, models) and that of an AI DevOps engineer (e.g. manifests). Having structure in a project ensures all the pieces required for the ML and DevOps lifecycles are present and easily discoverable.


## Tutorial pre-requisites

0. [Pre-requisites](./docs/source/pre-requisite.md)

## Tutorial Steps

1. [Setup your initial environment](./docs/source/setup-initial-environment.md)

2. [Create overlays from notebooks](./docs/source/create-overlays-from-notebook.md)

3. [Push changes to GitHub](./docs/source/push-changes.md)

4. [Setup bots and pipelines to create releases, build images with overlays and enable automatic dependency management](./docs/source/thoth-aicoe-services.md)

5. [Create an AI Pipeline](./docs/source/create-ai-pipeline.md)

6. [Run and debug AI Pipeline](./docs/source/run-ai-pipeline.md)


## References

* [AICoE CI][1]
* [Kebechet Bot][2]
* [Open Data Hub][3]
* [Red Hat Openshift][4]
* [project template][5]
* [Operate First][6]

[1]: https://github.com/AICoE/aicoe-ci
[2]: https://github.com/marketplace/khebhut
[3]: https://opendatahub.io/
[4]: https://www.openshift.com/
[5]: https://github.com/aicoe-aiops/project-template
[6]: https://www.operate-first.cloud/
