# Shared Conda Environments

Shared conda environments let instructors and TAs install custom packages and
register new Jupyter kernels for their courses, without needing GitHub pull
requests or waiting for the new software to be deployed. This is useful for
quickly adding or updating software needed for teaching or assignments,
providing autonomy to instructors in making quick changes to the instructional
environment.

Creating additional conda environments also helps avoid dependency problems: you
can install software into a secondary environment that might otherwise break the
base environment, keeping your course setup stable and isolated.

:::{warning}
Creating or modifying environments in `/srv/conda/envs/` may require elevated
permissions or specific hub configuration. If you encounter permission errors,
contact the DataHub team.
:::

If you are interested in piloting this feature in your hub, we encourage you to
[contact the DataHub
team](https://github.com/berkeley-dsep-infra/datahub/issues/new?template=featurerequest.md)
for more information and to express your interest.

## Technical Details

The software is deployed on the shared cloud file server, not within the hub's
singleuser docker image, so changes to secondary conda environments do not
require that the docker image be rebuilt and deployed. Students might only need
to restart their notebook servers to see newly installed kernels, and package
updates would require that students restart running kernels.

## Create a Conda Environment

1. Open a terminal from Jupyterlab and run:

   ```bash
   conda init
   ```

   If you see the “No action taken” error, run:

   ```bash
   source ~/.bashrc
   ```

1. Create a conda environment from scratch

   ```bash
   conda create --prefix /srv/conda/envs/shared_conda python=3.11 -y
   ```

   You can create a conda environment from the ‘notebook’ conda environment if ‘notebook’ exists. You can check if notebook exists by running conda env list.

   ```bash
   conda list --explicit --prefix /srv/conda/envs/notebook > base-env.txt
   conda create --prefix /srv/conda/envs/shared_conda --file base-env.txt
   ```

   You can also create a conda environment from the `base` conda environment:

   ```bash
   conda list --explicit --prefix /srv/conda > base-env.txt
   conda create --prefix /srv/conda/envs/shared_conda --file base-env.txt
   ```
   :::{tip}
   Conda dependency resolution can be memory-intensive, especially when installing multiple or complex packages. We recommend temporarily increasing memory resources for instructor or TA pods when setting up shared environments.
   :::

1. Activate the new environment to start working in it.

   ```bash
   conda activate /srv/conda/envs/shared_conda
   ```

1. Install any additional packages you need for the course.

   ```bash
   mamba install numpy pandas -y
   ```
   If `mamba` is not available, use `conda install ...` instead. `mamba` is a faster drop-in replacement for `conda`.

1. Install `ipykernel` if not already installed.

   ```bash
   mamba install ipykernel -y
   ```

1. Install a kernel that uses your new conda environment.

   ```bash
   python -m ipykernel install \
       --name shared_conda \
       --display-name "Python (<bcourse_id or whatever you want>)" \
       --prefix /srv/conda/envs/shared_conda
   ```

   ```{note}
   Registering a kernel makes it available in the Jupyter interface for you and your students. `--name` is the internal kernel identifier, and `--display-name` is what users will see in the Jupyter UI.
   ```

1. Validate that the kernel was successfully registered.

   ```bash
   jupyter kernelspec list
   ```

   This will display all available Jupyter kernels.

1. Optionally deactivate the environment once setup is complete. This is only necessary if you want your running terminal to have access to the original environment.

   ```bash
   conda deactivate
   ```

:::{tip}
If your new kernel does not appear in the Jupyter interface, try restarting your notebook server. Students may also need to restart their servers to see new kernels.
:::

## Remove a Conda Environment

To remove the conda environment, run:

```bash
conda env remove --prefix /srv/conda/envs/shared_conda
```

This frees up disk space on the shared file server.
