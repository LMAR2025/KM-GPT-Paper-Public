# KM-GPT Paper Public

Public repository for the KM-GPT paper materials. This repository contains:

- notebook-based analyses in `code/`
- public Kaplan-Meier reconstruction datasets in `data/`
- synthetic survival simulation data and model reconstruction outputs in `SimulationData/`

The project appears to focus on evaluating Kaplan-Meier curve reconstruction workflows on both public-study examples and simulated survival datasets.

## Repository Layout

```text
KM-GPT-Paper-Public/
|-- code/
|-- data/
`-- SimulationData/
```

### `code/`

Jupyter notebooks used for simulation, reconstruction review, and evaluation:

- `SurvDatasSimulator.ipynb`
  Generates synthetic survival data and Kaplan-Meier style outputs.
- `Public Data Eval.ipynb`
  Evaluates public-study datasets stored under `data/`.
- `PD-L1 Reconstruction Results.ipynb`
  Examines PD-L1 reconstruction outputs.
- `PD_L1_Meta.ipynb`
  Related PD-L1 notebook workflow.
- `Simulation Data Eval GPT5 Base.ipynb`
  Evaluates GPT-5 base reconstruction results on simulated datasets.
- `Simulation Data Eval Sensitivity.ipynb`
  Sensitivity-style analysis on simulated reconstruction results.

### `data/`

Public-study examples used for reconstruction and comparison, including:

- `LANG0213_PFS`
- `LEO1010_PFS`
- `PD-L1`
- `ZAMAN0715_OS`

These folders include source materials such as PDFs, SVGs, digitized data, risk tables, and reconstructed IPD files.

### `SimulationData/`

Synthetic Kaplan-Meier benchmark assets and outputs, including:

- `figures/`
  Generated Kaplan-Meier plots and risk table images.
- `ipd/`
  Simulated individual patient data.
- `recon_GPT5_base/`
- `recon_GPT5_minimal/`
- `recon_GPT4o_Tat0/`
- `recon_GPT4o_Tat05/`
- `recon_GPT4o_Tat1/`
- `recon_Qwen32B_Tat0/`
- `recon_Qwen32B_Tat1/`
- `simulation_metadata.csv`
  Metadata describing simulated datasets, including patient counts, median survival, censoring level, follow-up horizon, and risk tables.

## Getting Started

This repository is notebook-first, so the easiest way to explore it is through Jupyter.

### Suggested environment

Install Python 3.10+ and create an environment with packages used in the notebooks:

```bash
pip install jupyter numpy pandas matplotlib seaborn pillow lifelines tqdm
```

Depending on the notebook path you follow, you may also need additional packages not listed here.

### Launch notebooks

From the repository root:

```bash
jupyter notebook
```

Then open notebooks in `code/`.

## Workflow Notes

- Many notebooks use relative paths such as `../data/` and `../SimulationData/`.
- For those paths to resolve correctly, open and run the notebooks from the `code/` directory context.
- Large generated outputs are already included in this repository, so cloning may take some time.

## Suggested Entry Points

If you are new to the repository, a practical reading order is:

1. `code/SurvDatasSimulator.ipynb`
2. `code/Public Data Eval.ipynb`
3. `code/Simulation Data Eval GPT5 Base.ipynb`
4. `code/PD-L1 Reconstruction Results.ipynb`

## Status

This README was created from the current repository contents and notebook names. If you want, it can be expanded next with:

- a paper abstract or citation block
- exact reproduction steps for each notebook
- a dependency file such as `requirements.txt`
