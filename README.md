# Demonstration FilterBranchMap

## Project structure

```text
.
├── Demonstration.ipynb       # Main evaluation notebook
├── evaluation_setup.py       # Data preparation and evaluation metrics
├── filterbranchmap.py        # FilterBranchMap visualization
├── lineage_core.py           # Query-lineage utilities
├── queries.py                # Reusable LogView query definitions
├── utils.py                  # Shared metric and query helpers
├── Model.png                 # Data-model image used by the notebook
├── logview/                  # Local LogView implementation
├── dataset/                  # Create this folder locally
│   └── Road_Traffic_Fine_Management_Process.csv
└── requirements.txt
```

## Dataset

The event-log dataset is not included in this repository because the file is too large to upload.

Before running the notebook, create a folder named `dataset` in the project root and place the following file inside it:

```text
Road_Traffic_Fine_Management_Process.csv
```
