# Managing-Environment-Using-Anaconda
This tutorial is going through what you need to manage python environments by yourself using Anaconda. This is just a summary that I think this is needed for beginners or any people want to use Anaconda prompt to handle python environment comfortably

**Note:** all the in thing the square bracket [] is your choice

---
## Install Anaconda
- [Install latest version of Anaconda suitable for your computers (64-bit or 32-bit: Almost computer nowadays is 64-bit)](https://www.anaconda.com/products/individual)
- Open Anaconda Command Prompt and flow the tutorial

---
## Creating and removing an environment

1. **Create an environment do not using file**
   1. To create an environment
    ``conda create --name [name]``
   2. To create an environment with specific version of Python
    ``conda create -n [name] python=3.6``
   3. To create an environment with specific package
    ``conda create -n [name] scipy=0.15.0``
    4. If you do not tell what version this will install the latest release
    ``conda create -n [name] python``
    5. To install python and multiple package
    ``conda create -n [name] python=3.6 scipy=0.15.0 astroid babel``

2. **Create an environment from .yml file**:
    1. Create an environment from the example.yml file
    ``conda env create -f example.yml``
    2. Save current environment to the file
    ``conda env export > example.yml``

3. **Remove an environment**
    1. In many case that some envs you do not remember those name. You can see all the envs by the command:
    ``conda info --envs``
    2. To remove specific environment
    ``conda remove -n [name] --all``

---
## Activate and Deactivate the environment:
1. For using or activating specific environment in anaconda you can use
    ``conda activate [name]``
2. For quitting or deactivate environment
    ``conda deactivate``

---

## Install packages for your environment

**\[name]** in here is your environment that you just have create in first part

1. **When you do not activate environment**
   ``conda install -n [name] scipy numpy jupyterlab matplotlib=3.1``

2. **You have activate your environment**
   - Once you have install python in your environment. After activate you can using pip to install any package that you want.
      ``pip install scipy numpy jupyterlab matplotlib=3.1``
      Or you can using:
        ``conda install [package]`` and ``conda uninstall [package]`` to handle your environment
    - You can see what package that you have install
      ``conda list``
    - Update specific package:
      ``conda update scipy ``
    - Updata all package:
      ``conda update --all``



## Reference
\[1]: https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

\[2]: https://stackoverflow.com/questions/38972052/anaconda-update-all-possible-packages
