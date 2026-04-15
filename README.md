# 2025.Arif_Doran_etal_IschemicHeartDisease

Code and data for:

**Arif M, Doran S, Clausen M, Wikström J, Bohlooly-Y M, Björnson E, Davidsson L, Jeppsson A, Levin M, Mardinoglu A, Boren J.**  
**Integrative Analysis of Left Ventricle and Epicardial Adipose Tissue Identifies SDHA and OGDH as Candidate Targets for Ischemic Heart Disease**  
*bioRxiv* (preprint), 2025.  
DOI: `10.1101/2025.09.17.676232`

---

## Overview

This repository contains the code and supporting data used for the transcriptomics and systems-level analysis of ischemic heart disease (IHD) across two cardiac tissue subtypes:

- **Left ventricle (LV)**
- **Epicardial adipose tissue (EAT)**

The study compares healthy controls with ischemic heart disease subjects, including both:

- **non-diabetic ischemic (ND-I)**
- **diabetic ischemic (D-I)**

The analysis includes differential expression, pathway enrichment, co-expression network analysis, reporter metabolite analysis, transcription factor analysis, and validation in independent public datasets.

---

## Repository contents

- `FinalCode.ipynb`  
  Main notebook for the analysis and figure generation.

- `env.yml`  
  Conda environment file required to reproduce the computational setup.

- `Data/`  
  Contains repository-provided input data, including:

  - `Data S1.xlsx`

- `Library/`  
  Reference and auxiliary files used by the workflow.

- `Results_Paper/`  
  Output files, intermediate results, and figure-related materials.

---

## Data availability and reproducibility

This repository uses both **local project data** and **public external datasets**.

### Repository-provided data
The following data are included in this repository:

- `Data/Data S1.xlsx`

This file contains the processed transcriptomics data, along with clinical and demographic data used in the manuscript.

### Public external data
In addition to `Data S1`, the full analysis also uses public datasets, including:

- **GTEx** heart left ventricle data
- Public human single-cell / spatial transcriptomics data from **PMID: 35948637**

To fully reproduce all analyses, make sure these public datasets are downloaded separately from their original sources and made available to the notebook/workflow as expected.

### Notes on reproducibility
Reproducing the complete study therefore requires:

1. the repository data in `Data/Data S1.xlsx`
2. the required public datasets
3. the conda environment defined in `env.yml`

---

## Environment setup

This project uses a conda-based Python environment defined in `env.yml`.

### 1. Clone the repository

```bash
git clone https://github.com/muharif/2025.Arif_Doran_etal_IschemicHeartDisease.git
cd 2025.Arif_Doran_etal_IschemicHeartDisease
```

### 2. Create the conda environment

```bash
conda env create -f env.yml
```

### 3. Activate the environment

```bash
conda activate IHD_project
```

### 4. Add the environment to Jupyter

```bash
python -m ipykernel install --user --name IHD_project --display-name "Python (IHD_project)"
```

## Tested environment

This workflow was tested on **Dardel HPC** at **PDC Center for High Performance Computing, KTH Royal Institute of Technology**.

### System information

- **Platform:** Dardel HPC (PDC/KTH)
- **Operating system:** SUSE Linux Enterprise Server 15 SP5
- **OS version:** SLES 15.5
- **Kernel:** `5.14.21-150500.55.65_13.0.73-cray_shasta_c`
- **Architecture:** `x86_64`
- **CPU:** AMD EPYC 7742 64-Core Processor
- **Available CPUs on test node:** 256

### Software information

- **Python:** 3.10.16
- **Conda:** 24.11.3
- **IPython:** 8.32.0
- **ipykernel:** 6.29.5
- **jupyter_client:** 8.6.3
- **jupyter_core:** 5.7.2
- **jupyter_server:** 2.15.0
- **jupyterlab:** 4.3.5
- **notebook:** 7.3.2
- **nbclient:** 0.10.2
- **nbconvert:** 7.16.6
- **nbformat:** 5.10.4
- **ipywidgets:** 8.1.5
- **traitlets:** 5.14.3

The software environment used for the analysis is defined in `env.yml`. Exact reproducibility may still depend on local HPC module configuration, package resolution, and access to the required input datasets.

---

## Launch Jupyter

Start Jupyter Notebook with:

```bash
jupyter notebook
```

Then open:

```text
FinalCode.ipynb
```

and select the kernel:

```text
Python (IHD_project)
```

---

## Execution

To run the analysis:

1. Open `FinalCode.ipynb`
2. Make sure all required input files are available
3. Ensure any required public datasets have been downloaded and paths are updated if needed
4. Select the correct Jupyter kernel
5. Run the notebook cells **in order**, from top to bottom

---

## Expected analyses in this repository

The notebook/workflow includes analyses such as:

- clinical and demographic comparisons
- transcriptomics analysis of LV and EAT
- differential expression analysis
- pathway enrichment analysis
- co-expression network construction
- Leiden clustering / community detection
- reporter metabolite analysis
- reporter transcription factor analysis
- validation using GTEx and public myocardial infarction datasets
- figure generation for the manuscript

---

## Public datasets referenced in this study

The revised manuscript indicates use of the following public datasets/resources:

- **GTEx**  
  Used for validation using heart left ventricle expression data.

- **PMID: 35948637**  
  Public single-cell and spatial transcriptomics dataset used for validation.

- Additional public transcriptomic datasets are also described in the manuscript methods and supplementary data.

---

## Manuscript

Current preprint version:

**Integrative Analysis of Left Ventricle and Epicardial Adipose Tissue Identifies SDHA and OGDH as Candidate Targets for Ischemic Heart Disease**  
bioRxiv, 2025  
DOI: `10.1101/2025.09.17.676232`

This README reflects the **current manuscript version** and can be updated after journal acceptance.

---

## Citation

If you use this repository, please cite the current preprint:

```text
Arif M, Doran S, Clausen M, Wikström J, Bohlooly-Y M, Björnson E, Davidsson L, Jeppsson A, Levin M, Mardinoglu A, Boren J.
Integrative Analysis of Left Ventricle and Epicardial Adipose Tissue Identifies SDHA and OGDH as Candidate Targets for Ischemic Heart Disease.
bioRxiv. 2025.
doi: 10.1101/2025.09.17.676232
```

---

## Contact

For questions about the study or code, please contact:

**Muhammad Arif**  
muhammad.arif@gu.se

---

## Notes

- The README currently refers to the **bioRxiv preprint** version of the manuscript.
- The citation can be updated once the article is formally accepted and published.
- Full reproducibility depends on access to both the repository data and the external public datasets described above.
