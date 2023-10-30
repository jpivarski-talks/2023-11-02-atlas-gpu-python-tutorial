# 2023-11-02-atlas-gpu-python-tutorial

Thursday, November 2, 2023. This is the Python part of the [ATLAS GPU Training](https://indico.cern.ch/event/1331139/overview).

## Draft instructions

1. Launch your DLI Jupyter.
2. Click the blue `+` button and black `$_` terminal button.
3. In the terminal, install Miniforge:

```bash
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh
bash Miniforge3-Linux-x86_64.sh -b
/root/miniforge3/bin/mamba init bash
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

## Draft schedule

* **0:00** (30 min) Introduce the Python tools
* **0:30** (20 min) Compute the Z mass in CUDA with Numba
* **0:50** (20 min) Introduce tree-reduction
* **1:10** (20 min) Students work on Project 1: parallel histogram filling
* **1:30** (5 min) _break_
* **1:35** (20 min) Review Project 1 solutions
* **1:55** (20 min) Introduce random seeding of parallel algorithms
* **2:15** (20 min) Students work on Project 2: compute area by random sampling
* **2:35** (5 min) _break_
* **2:40** (20 min) Review Project 2 solutions
* **3:00** _end_
