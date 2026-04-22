# 📊 FASTA Composition Analyzer

A Python tool that reads a multi-sequence FASTA file, calculates the **purine and pyrimidine composition** of each DNA sequence, and visualises the results as a stacked bar chart.

Built independently as part of a self-directed bioinformatics project during the first year of a B.Tech Biotechnology program at VIT.

---

## What It Does

Given a `.fasta` file containing one or more DNA sequences, the tool:
- Parses each sequence and its organism/label name
- Counts A, G, C, T bases across the full sequence
- Calculates **purine %** (A + G) and **pyrimidine %** (C + T)
- Computes the purine-to-pyrimidine ratio
- Prints a summary table to the terminal
- Generates a **stacked bar chart** comparing composition across all sequences

---

## Example Output

Tested on insulin gene sequences (`all_insulin.fasta`) across multiple organisms:

**Terminal output:**
```
Homo sapiens
Total Bases: 333
Purine %: 51.65
Pyrimidine %: 48.35
Ratio: 1.07

Mus musculus
Total Bases: 333
Purine %: 50.45
Pyrimidine %: 49.55
Ratio: 1.02
```

**Chart:** Stacked bar graph with purines (blue) and pyrimidines (red) per organism.

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/fasta-composition-analyzer.git
cd fasta-composition-analyzer

# Install matplotlib if you don't have it
pip install matplotlib

# Add your FASTA file to the folder, then run
python allfasta.py
```

> By default the script looks for a file called `all_insulin.fasta`. Change the filename at the bottom of `allfasta.py` to point to your own FASTA file.

---

## Input Format

Standard multi-sequence FASTA format:

```
>Organism name
ATGGCCCTGTGGATGCGCCTCCTGCCC...
>Another organism
ATGGCCCTGTGGATGCGCCTCCTGAAA...
```

The script reads the first two words of each header line as the organism name label.

---

## Biological Context

Chargaff's rules state that in double-stranded DNA, purines and pyrimidines should be roughly equal (ratio ≈ 1.0). Comparing this ratio across species or gene variants can reveal compositional biases and is a useful first-pass quality check when working with new sequence data.

This script was tested on insulin gene sequences sourced from NCBI.

---

## Dependencies

- Python 3.x
- `matplotlib` — install with `pip install matplotlib`

---

## Author

**Sampriti Halder**  
B.Tech Biotechnology, SBST — Vellore Institute of Technology  
[sampriti.halder.2025@vit.student.ac.in](mailto:sampriti.halder.2025@vit.student.ac.in)
