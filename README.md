# Computational Biology Assignment 2 - Finding Patterns in Sequences

**Course:** SCIE6062001 - Computational Biology  
**Semester:** Odd Semester 2025-2026 AY  
**Assignment:** Finding Patterns in Sequences

## Overview

This project implements solutions for 5 different pattern matching tasks in computational biology, demonstrating various algorithms for sequence analysis in DNA, RNA, and protein sequences.

## Project Structure

```
compBio-dna-genome-analyzer/
├── genome-analyzer.ipynb          # Main Jupyter notebook with all implementations
├── genome-dataset/                # Directory containing FASTA sequence files
│   ├── NC_000913.3_sequence.fasta    # E. coli K-12 genome
│   ├── NM_007294.4_sequence.fasta    # Human BRCA1 mRNA
│   ├── NC_012920.1_sequence.fasta    # Human mitochondrial DNA
│   ├── P00395_sequence.fasta         # Human COX1 protein
│   └── NM_000546.6_sequence.fasta    # Human p53 gene
└── README.md                      # This file
```

## Tasks Implemented

### Task 1: Exact Substring Search in DNA (E. coli genome)

- **Objective:** Find all occurrences of motif "ATGCG" in E. coli K-12 genome
- **Dataset:** GenBank accession NC_000913.3
- **Algorithms:** Naive search vs KMP (Knuth-Morris-Pratt)
- **Features:**
  - Performance comparison between algorithms
  - Runtime analysis and speedup calculation
  - Context display around matches

### Task 2: Approximate Pattern Matching in RNA (Human mRNA)

- **Objective:** Search for motif "AUGCU" in BRCA1 mRNA allowing up to 2 mismatches
- **Dataset:** GenBank accession NM_007294.4 (BRCA1 transcript)
- **Algorithm:** Edit distance (Levenshtein distance)
- **Features:**
  - Fixed window and sliding window approaches
  - Automatic DNA to RNA conversion (T→U)
  - Flexible mismatch tolerance

### Task 3: Reverse Complement Motif Search in DNA (Mitochondrial DNA)

- **Objective:** Search for "ATG" and its reverse complement in human mtDNA
- **Dataset:** GenBank accession NC_012920.1 (16,569 bp)
- **Features:**
  - Bidirectional motif search
  - Distribution analysis across genome
  - Statistical analysis and visualization

### Task 4: Protein Motif Recognition (Cytochrome c oxidase subunit I)

- **Objective:** Find PROSITE motif [ST]-x(2)-[DE] in COX1 protein
- **Dataset:** UniProt accession P00395
- **Features:**
  - PROSITE pattern to regex conversion
  - Multiple protein motif analysis
  - Motif position visualization

### Task 5: Multiple Motif Search in DNA (p53 gene)

- **Objective:** Simultaneous search for "TATA", "ATG", "TAG" in p53 gene
- **Dataset:** GenBank accession NM_000546.6
- **Algorithms:** Aho-Corasick vs Sequential KMP
- **Features:**
  - Multi-pattern search implementation
  - Performance comparison
  - Comprehensive motif distribution analysis

## Algorithms Implemented

1. **Naive String Matching** - O(nm) time complexity
2. **Knuth-Morris-Pratt (KMP)** - O(n+m) time complexity
3. **Edit Distance (Levenshtein)** - Dynamic programming approach
4. **Aho-Corasick** - Multi-pattern string matching, O(n+m+z) complexity
5. **Regular Expression Matching** - For PROSITE pattern recognition

## Requirements

### Python Dependencies

```
python >= 3.7
jupyter
matplotlib
pandas
numpy
```

### Installation

```bash
pip install jupyter matplotlib pandas numpy
```

## Usage

1. **Clone or download the project**
2. **Ensure all FASTA files are in the `genome-dataset/` directory**
3. **Start Jupyter Notebook:**
   ```bash
   jupyter notebook genome-analyzer.ipynb
   ```
4. **Run all cells sequentially**

## Key Features

- **Robust FASTA parsing:** Handles multi-line sequences by joining into single strings
- **Performance analysis:** Timing comparisons between different algorithms
- **Visualization:** Distribution plots and motif position charts
- **Comprehensive output:** Detailed match information with context
- **Error handling:** Proper sequence validation and processing

## Results Summary

The notebook provides detailed analysis including:

- Number of motif occurrences found
- Algorithm performance comparisons
- Statistical analysis of motif distributions
- Visualization of results
- Context around each match for verification

## Technical Notes

- All sequences are processed as single continuous strings to avoid newline character issues
- Multiple algorithm implementations allow for performance comparison
- Visualization components use matplotlib for clear result presentation
- Code is well-documented with type hints and docstrings

## Author

Riki Awal Syahputra

Computational Biology Assignment - SCIE6062001  
Odd Semester 2025-2026 AY
