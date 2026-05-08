# HemoPI: A Web Server and Mobile App for Computing Hemolytic Potency

Welcome to the official documentation for **HemoPI**, a dedicated suite of computational tools designed for predicting, screening, and designing peptides with varying hemolytic potency.Hemolytic activity—the lysis of red blood cells—is a critical safety parameter and a major hurdle in translating therapeutic peptides into clinical drugs[cite: 8, 22]. [cite_start]HemoPI provides researchers with high-accuracy machine learning models to identify hemotoxicity before embarking on costly and time-consuming experimental synthesis.

**Web Server:** [http://crdd.osdd.net/raghava/hemopi/](http://crdd.osdd.net/raghava/hemopi/) 

---

## Citation

Chaudhary, K., Kumar, R., Singh, S., Tuknait, A., Gautam, A., Mathur, D., Anand, P., Varshney, G. C., & Raghava, G. P. S. (2016). 
**A Web Server and Mobile App for Computing Hemolytic Potency of Peptides.** *Scientific Reports*, 6, 22843. 
[https://doi.org/10.1038/srep22843](https://doi.org/10.1038/srep22843)

---

## About the Platform

HemoPI was developed to help researchers overcome the toxicity hurdles associated with peptide-based therapeutics. [cite_start]While peptides offer high specificity and better tissue penetration than small molecules, their clinical potential is often limited by high hemolytic activity.HemoPI utilizes models trained on experimentally validated data from the Hemolytik database to discriminate between hemolytic and non-hemolytic peptides with over **95% accuracy**.

The platform utilizes three distinct datasets:
* **HemoPI-1**: Contains 552 hemolytic peptides and 552 random non-hemolytic peptides (from Swiss-Prot).
* **HemoPI-2**: Designed to discriminate between high and low hemolytic potency using 442 positive and 370 negative examples from Hemolytik[cite: 49, 50, 51].
* **HemoPI-3**: A larger dataset consisting of 1623 peptides extracted from both DBAASP v.2 and Hemolytik.

---

## Key Features

### Prediction & Design Tools
* **Hemolytic Potency**: Predicts the hemolytic nature of a peptide and generates all possible single-substitution mutants (analogs) to identify variants with desired activity.
* **Virtual Screening**: Allows users to screen large libraries of peptides by submitting multiple sequences in FASTA format.
* **Protein Mapping**: Identifies specific hemolytic regions within a protein sequence by generating and ranking overlapping peptide segments.
* **Quantitative Matrices (QM)**: Provides single residue, dipeptide, and property-based propensities for visual analysis of residue preferences at different positions.

### Multi-Platform Accessibility
* **Web Interface**: User-friendly portal for online predictions and data visualization.
* **Mobile App**: An Android application providing "Predict" and "Mutant" modules for analysis on the go.
* **Standalone Software**: A JAVA-based offline tool for batch processing and local integration.

---

## Technical Overview

HemoPI employs various machine learning techniques, with Support Vector Machines (SVM) serving as the primary model for most features.

| Feature Type | Description |
| :--- | :--- |
| **Amino Acid Composition** |Encapsulates global information through the fraction of each of the 20 natural amino acids. |
| **Dipeptide Composition** | Captures local order and global information using 400-dimensional vectors. |
| **Binary Profiles** | Incorporates position-specific information for residues at the N and C termini. |
| **Hybrid Approach** | Integrates machine learning with motifs (e.g., "FKK", "LKL") extracted via MERCI software]. |

---

## Applications

* **Drug Discovery**: Accelerates peptide-based drug discovery by filtering out toxic candidates early.
* **Peptide Optimization**: Assists in designing analogs with minimized hemolytic potency without compromising therapeutic efficacy.
* **Physicochemical Analysis**: Calculates properties like amphiphilicity, hydrophobicity, and steric hindrance for submitted sequences.

---

## Contact & Authors

**Prof. G.P.S. [cite_start]Raghava** Bioinformatics Centre, CSIR-Institute of Microbial Technology, Chandigarh, India.  
*(Currently at IIIT-Delhi)*  
**Email**: raghava@imtech.res.in / raghava@iiitd.ac.in

---

## License

This work is licensed under a **Creative Commons Attribution 4.0 International License**, permitting unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.
