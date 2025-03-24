# CAR-T Sequence Detection in Single-Cell RNA-Seq Data

This repository contains workflows for analyzing and simulating single-cell RNA sequencing (scRNA-seq) data to detect Chimeric Antigen Receptor (CAR) sequence insertions.

## Overview

CAR-T cell therapy involves genetically modifying T cells to express chimeric antigen receptors (CARs) that target specific antigens on cancer cells. This project provides tools to:

1. Create a custom reference genome that includes the CAR sequence
2. Process scRNA-seq data using Cell Ranger to detect CAR-expressing cells
3. Analyze the transcriptional profiles of CAR-positive cells
4. Visualize CAR expression patterns and associated cellular phenotypes
5. Generate synthetic scRNA-seq data with CAR sequence insertions for testing analysis pipelines

## Requirements

- 10x Genomics Cell Ranger (v7.0 or later)
- Python 3.8 or higher
- Required Python packages (see `requirements.txt`)

## Getting Started

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Download Cell Ranger from the [10x Genomics website](https://support.10xgenomics.com/single-cell-gene-expression/software/downloads/latest)
4. Prepare your scRNA-seq FASTQ files
5. Run one of the Jupyter notebooks:
   - `car_t_detection.ipynb` - For real data analysis
   - `synthetic_cart_data.ipynb` - To generate synthetic data

## Workflow

### Real Data Analysis

The analysis workflow includes:

1. **Setting up a custom reference genome**: Adding the CAR sequence to a standard reference
2. **Processing with Cell Ranger**: Aligning reads and generating feature-barcode matrices
3. **Identifying CAR-positive cells**: Detecting cells expressing the CAR construct
4. **Analyzing transcriptional profiles**: Comparing CAR+ and CAR- cell populations
5. **T cell phenotyping**: Characterizing T cell subsets in relation to CAR expression

### Synthetic Data Generation

The synthetic data workflow includes:

1. **Simulating gene expression matrix**: Creating a realistic T cell population dataset
2. **Generating a synthetic CAR sequence**: Constructing a representative CAR construct
3. **Random CAR insertion**: Adding CAR expression to a subset of cells
4. **Visualization**: Examining the properties of the synthetic dataset
5. **Exporting data**: Saving in formats compatible with standard analysis tools

## Customization

- Modify the CAR sequence in the notebooks to match your specific construct
- Adjust Cell Ranger parameters based on your dataset characteristics
- Add custom marker genes for specific cell populations of interest
- Tune synthetic data parameters to match characteristics of your experimental system

## Citation

If you use this workflow in your research, please cite:

```
[Your citation information here]
```

## License

[Your license information here]