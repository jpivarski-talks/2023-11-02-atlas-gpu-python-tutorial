# 2023-11-02-atlas-gpu-python-tutorial

Thursday, November 2, 2023. This is the Python part of the [ATLAS GPU Training](https://indico.cern.ch/event/1331139/overview).

## Working on instructions

1. Launch your DLI Jupyter.
2. Click the blue `+` button and black `$_` terminal button.
3. In the terminal, install Miniforge:

```bash
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh
bash Miniforge3-Linux-x86_64.sh -b
~/mambaforge/bin/mamba init bash
```

4. **Close this terminal and open a new one.**
5. In the **new** the terminal, install this git repo:

```bash
git clone https://github.com/jpivarski-talks/2023-11-02-atlas-gpu-python-tutorial.git
cd 2023-11-02-atlas-gpu-python-tutorial
```

5. Install all the Python packages in an environment and activate it:

```bash
echo y | mamba env create -f environment.yml   # or environment.lock.yml
mamba activate 2023-11-02-atlas-gpu-python-tutorial
```

6. Install the environment as a new kernel in the already-running Jupyter:

```bash
python -m ipykernel install --prefix=/usr/local/ --name 2023-11-02-atlas-gpu-python-tutorial
```

7. Click the blue `+` button and "2023-11-02-atlas-gpu-python-tutorial" should be available as an alternate kernel. Notebooks created with this kernel will have all of the Python packages, as will any notebooks in which you "Change kernel..." ("Kernel" menu) to this kernel.

The notebooks for this tutorial are in the 2023-11-02-atlas-gpu-python-tutorial folder (see the file browser in the left panel).
