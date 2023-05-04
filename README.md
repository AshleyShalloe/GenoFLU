# GenoFLU

This tool uses BLAST to identify segments from a curated database. Pre-defined genotypes are cross-referenced with the top segment identifications, and a genotype is assigned. A cutoff of 2% difference from the closest curated sequence identifies new reassortment. New reassortment is reviewed using segment-based phylogenetic trees. If appropriate, new segment sequences will be added to the curated database and new genotype assignments updated.

# Installation

## GitHub install with necessary dependencies

Clone this repository
```
export PATH="<path to this clone repository>/GenoFLU/bin:$PATH"
```

While in conda base, make new environment
```
conda create --name genoflu
```
```
conda activate genoflu
```

```
conda install python=3.10
conda install pandas
conda install -c conda-forge biopython
conda install -c bioconda blast
conda install -c anaconda openpyxl
```

## Available once repo is made public
```
conda install GenoFlU -c conda-forge -c bioconda
```

# Usage

FASTA file containing a segmented influenza genome, with each segment having its own individually named header.
```
genoflu.py -f <*.fasta>
```

# Output

Genotype summary as Excel and tab delimited text file.