# Allen Database Notebooks

A collection of Jupyter notebooks for analyzing neuroscience data from the Allen Institute.

## Setup Instructions

### Prerequisites
- Python 3.11 (recommended but any should do)
- Anaconda or Miniconda for environment management

### Installation

1. Create a Python environment:
   ```bash
   conda create -n allen-notebooks python=3.11
   conda activate allen-notebooks
   ```

2. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. Install additional packages from GitHub (with fixes for Allen Institute compatibility):
   ```bash
   git clone https://github.com/GregGlickert/neuroanalysis
   cd neuroanalysis
   python setup.py develop
   cd ..
    ```
    
   ```bash
   git clone https://github.com/GregGlickert/aisynphys
   cd aisynphys
   python setup.py develop
   cd ..
   ```

### Usage

This repository contains two main Jupyter notebooks for analyzing neuroscience data:

#### `Synapses/in_vivo_synapses.ipynb`
Analyzes synaptic connectivity and properties between different cell types in mouse visual cortex. The notebook:
- Loads synapse data from the Allen Institute's synaptic physiology database
- Defines cell classes (ET, IT, PV, SST neurons)
- Extracts excitatory and inhibitory synapse parameters
- Fits stochastic release models to characterize synaptic transmission

#### `Cells/in_vivo_cell_properties.ipynb`
Examines electrophysiological properties of individual neurons from the Allen Cell Types Database. The notebook:
- Filters cells by species, brain region (Layer 5 visual cortex), and transgenic lines
- Extracts key electrophysiological features (input resistance, membrane time constant, etc.)
- Generates visualizations of cell type-specific characteristics such as FI curve and current clamps

