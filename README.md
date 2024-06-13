# ai-experiments

Just a weird collection of stuff

## Jupyter Notebooks

### Getting started

Just start the docker container.

```
docker compose up
```

Fetch the URL from the console, align the port 8888 to 10000 and open the jupytherLab in your broweser.

```
http://127.0.0.1:10000/lab?token=__YOUR_TOKEN____
```

Enter the "work" folder and start with the 00_installation notebook.

* https://github.com/jupyter/docker-stacks

#### Cleanup Notebooks

To avoid commiting of notebook outputs, just run the following command from launcher -> Terminal

```
jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace *.ipynb
```

There is a more elegant way of using pre-commit hooks, described [here](https://zhauniarovich.com/post/2020/2020-06-clearing-jupyter-output/).

### Projects

* [Neuronm explanation](./notebooks/01_neuron_explanation/README.md)
* [fashionMNIS single output](./notebooks/02_fashionMNIST_single_output/README.md)
* 