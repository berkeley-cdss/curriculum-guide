# Shared Conda Environment

We are excited to announce that, beginning in Fall 2025, we will introduce the ability to create a shared Conda environment for instructors in selected hubs. This feature will allow instructors to create a custom kernel, install the desired packages, and have those changes automatically reflected in the student kernel. This streamlined process provides autonomy to instructors in making quick changes to the instructional environment.

If you are interested in piloting the shared Conda environment in your hub, we encourage you to contact the DataHub team via [GitHub](https://github.com/berkeley-dsep-infra/datahub/issues/new?template=featurerequest.md] for more information and to express your interest.


## Steps for Creating and Registering a Shared Conda Environment in Jupyter

### Tips

- Conda dependency resolution can be memory-intensive, especially when installing multiple or complex packages. We recommend temporarily increasing memory resources for instructor or TA pods when setting up shared environments.


- After instructors or TAs install new packages and register the environment as a Jupyter kernel, students may need to restart their notebook servers to see the updated kernel appear in the kernel selection menu.


### Step-by-Step Guide

- Open a terminal from Jupyterlab, run 

```{bash}
conda init
```

If you see the “No action taken” error, run the following

```{bash}
source ~/.bashrc
```

- Create a new Conda environment (Create a conda environment from scratch)

```{note}
You can check if notebook exists by running conda env list
```

```{bash}
conda list --explicit --prefix /srv/conda/envs/notebook > base-env.txt
conda create --prefix /srv/conda/envs/shared_conda --file base-env.txt
```

Create a conda environment from the ‘base’ conda environment

```{bash}
conda list --explicit --prefix /srv/conda > base-env.txt
conda create --prefix /srv/conda/envs/shared_conda --file base-env.txt
```

- Activate the new environment
```{bash}
conda activate /srv/conda/envs/shared_conda
```

- Install extra packages you need

```{bash}
conda install numpy pandas -y
```

You may install any additional packages needed for the course.

- Install ipykernel if not already exists  to enable Jupyter integration

```{bash}
conda install ipykernel -y
```

- Register the environment as a Jupyter kernel. This step allows the environment to show up in the Jupyter Notebook interface:

```{bash}
python -m ipykernel install \
--name shared_conda \
--display-name "Python (<bcourse_id or whatever you want>)" \
--prefix /srv/conda/envs/shared_conda
```

```{note}
--name is the internal kernel identifier, and --display-name is what users will see in the Jupyter UI.
```

- Validate that the kernel was successfully registered

```{bash}
jupyter kernelspec list
```

This will display all available Jupyter kernels. 

- Deactivate the environment. Once setup is complete

```{bash}
conda deactivate
```

## Steps for Removing a Conda Environment

In case you want to remove the conda environment, run the following

```{bash}
conda env remove --prefix /srv/conda/envs/shared_conda
```
