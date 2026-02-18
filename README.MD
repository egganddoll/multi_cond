## Phase-field simulations of multiphase behavior in fluids with randomly interacting components
This is a readme for the documentation of the phase-field simulation model. Running this code requires 
pre-requisites (below) and  recommended to be run in a separate conda environment

### Installation

If using uv, code can be run with

`` uv run run_pfsim --flag_name flag_params ``

For a simple example, run

`` uv run run_pfsim --i Input/input_params.txt --o Output/ ``

If using pip for package management, first create a new virtual environment. Either use 

```
conda create -n multi_cond
conda activate multi_cond
```

or 

```
python -m venv .venv
source .venv/bin/activate
```

These environments will need to be activated each time the code is used. To install requirements, run

`` pip install -e . ``

Code can then be ran with

`` python run_pfsim --flag_name flag_params ``

#### Required flags

`` --i /path/to/input_params.file ``
Input parameters (example provided along with the code under /Input/input_params.txt)

`` --o /path/to/output_folder/ ``
Path to output folder

#### Optional flags

`` --p /path/to/parameter_sweep.file ``
Values of single parameter to sweep over (example provided along with the code under /Input/params_file.txt)

Note when using this - if only the effect of the parameter is to studied, best to fix a seed instead of using
a random seed. 

`` --pN x``
Run a simulation with param in line (x) from param file

`` --test 0/1``
If 1, runs a test setup - initialization occurs but no phase-field simulation is run and outputs are not generated to be stored.

