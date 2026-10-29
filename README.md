# FilterBranchMap Demonstration

This repository contains the Python implementation and demonstration of **FilterBranchMap**, an interactive visual artifact for tracing and reflecting on filtering steps in exploratory process mining.

FilterBranchMap represents successive filtering steps as a binary tree, preserving both included and excluded event log subsets. It supports comparing subsets using aggregate measures and exploring how alternative filtering orders affect intermediate subsets and their relationships.

This repository accompanies an **extended journal paper currently under review**, building on our [previous conference paper](https://doi.org/10.1007/978-3-032-28274-3_5).

## Project Structure

```text
.
├── Demonstration.ipynb       # Main demonstration notebook
├── evaluation_setup.py       # Data preparation and evaluation metrics
├── filterbranchmap.py        # Interactive FilterBranchMap visualization
├── lineage_core.py           # Query-lineage utilities
├── queries.py                # LogView query definitions
├── utils.py                  # Shared helpers
├── Model.png                 # Data-model image
├── logview/                  # Local LogView implementation
├── dataset/                  # Dataset directory
└── requirements.txt          # Python dependencies
```

## Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/lauradidden/FilterBranchMap-Demonstration.git
cd FilterBranchMap-Demonstration
python -m pip install -r requirements.txt
```

Install or upgrade the Jupyter widget packages to ensure compatibility with the interactive visualization:

```bash
python -m pip install -U ipywidgets jupyterlab_widgets widgetsnbextension
```

## Dataset

The demonstration uses the **Road Traffic Fine Management (RTFM)** event log.

Due to its size, the dataset is not included in this repository. Download it [[here](https://doi.org/10.4121/uuid:270fd440-1057-4fb9-89a9-b699b47990f5)] and place it at:

```text
dataset/Road_Traffic_Fine_Management_Process.csv
```

## Running the Demonstration

Start JupyterLab:

```bash
jupyter lab
```

Open `Demonstration.ipynb` and run the cells in order.

The notebook demonstrates how FilterBranchMap can be used to revisit filtering decisions, compare previously excluded subsets using aggregate measures, and explore alternative filtering orders in a recorded exploratory process mining analysis.

## Related Publications

- **Conference paper:** [*Visually Retracing and Comparing Filter Steps in Exploratory Process Mining*](https://doi.org/10.1007/978-3-032-28274-3_5).
- **Journal extension:** Currently under review.