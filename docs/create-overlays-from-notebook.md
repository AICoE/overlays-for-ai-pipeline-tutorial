# Create overlays from notebooks

For the purpose of this tutorial, the notebooks have been created already. They all contain dependencies information in their metadata thanks to [jupyterlab-requirements][1] library that allow for reproducibility.

Dependency management is one of the most important requirements for reproducibility. Having dependencies clearly stated allows portability of notebooks, so they can be shared safely with others, reused in other projects or simply reproduced. If you want to know more about this issue in the data science domain, have a look at this [article](https://developers.redhat.com/blog/2021/03/19/managing-python-dependencies-with-the-thoth-jupyterlab-extension/) or this [video](https://www.youtube.com/watch?v=ifyQ2oSxjnU).
If you are interested in a tutorial on managing dependencies, you can have a look at this [tutorial](https://github.com/AICoE/manage-dependencies-tutorial).

The notebooks that will be used in this tutorial are:

1. [explore_dataset.ipynb](../notebooks/explore_dataset.ipynb) for exploring the dataset from HuggingFace from GLUE Benchmark.

2. [preprocess_dataset.ipynb](../notebooks/preprocess_dataset.ipynb) for processing the dataset from HuggingFace from GLUE Benchmark.

3. [fine_tune_model.ipynb](../notebooks/fine_tune_model.ipynb) for to download a pre-trained model and fine tune it.

NOTE: _These notebooks have been derived from [HuggingFace material](https://github.com/huggingface/notebooks/blob/master/examples/text_classification.ipynb)._

In this step we want to create overlays with software stacks for the three notebooks/steps we want to have in the AI Pipeline


# Extract software stacks and runtime environments

1. Open one of the jupyter notebook in `notebooks` folder.

2. Run `%horus extract --use-overlay --pipfile --pipfile-lock --store-files-path ..` to extract software stack and runtime environment from

3. Repeat this process for each notebook.


At this point you will have an overlays folder with the following structure:

```
overlays/
    download-dataset/
        Pipfile
        Pipfile.lock
    fine-tune-model/
        Pipfile
        Pipfile.lock
    preprocess-dataset/
        Pipfile
        Pipfile.lock
```

As you can see we have specific software stacks for each of the notebooks/steps we have created.


## Next Step

[Push changes to GitHub](./push-changes.md)


## References

* [jupyterlab-requirements][1]

[1]: https://github.com/thoth-station/jupyterlab-requirements
