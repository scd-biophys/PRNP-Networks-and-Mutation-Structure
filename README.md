# PRNP-Networks-and-Mutation-Structure
Code to analyze PDB file via network methods

Network Analysis of Structural Determinants of Pathogenic Mutations in PRNP

A computational structural biology project investigating how protein network topology influences the pathogenicity of mutations in the human prion protein (PRNP). This study combines protein structure analysis, residue interaction networks, ClinVar variant data, and statistical modeling to identify structural features associated with disease-causing mutations.

Overview

Prion diseases, including Creutzfeldt–Jakob disease (CJD), arise from the misfolding and aggregation of the prion protein (PRNP). While many disease-associated PRNP variants have been identified, the structural factors that predispose specific residues to pathogenic mutations remain incompletely understood.

This project:

Builds a residue interaction network from the PRNP crystal structure (PDB: 1QLX)
Calculates network-based structural features such as:
Residue degree
Betweenness centrality
Maps ClinVar mutations onto the protein structure
Examines relationships between structural topology and mutation pathogenicity
Develops logistic regression models to predict pathogenicity
Identifies structurally important regions associated with disease
Key Findings
Residue degree was the strongest predictor of mutation pathogenicity.
Highly connected residues were more likely to harbor pathogenic variants.
High-centrality residues clustered significantly near known functional regions (p = 0.0122).
Pathogenic mutations were enriched in:
Helix 2
Helix 3
Model comparison using Akaike Information Criterion (AIC) showed that simple network-derived features can effectively predict pathogenic potential.
Methods
Structural Network Construction

The PRNP crystal structure (1QLX) was converted into a residue interaction network where:

Nodes represent amino acid residues
Edges represent residue-residue contacts within a distance threshold
Network Metrics

The following topological properties were calculated:

Degree
Betweenness centrality
Residue connectivity patterns
Variant Mapping

Clinical variants were obtained from ClinVar and mapped to corresponding residues in the PRNP structure.

Variants were categorized as:

Pathogenic
Benign / non-pathogenic
Statistical Analysis

Analyses included:

Logistic regression
Wilcoxon rank-sum testing
Permutation testing
AIC-based model comparison
Repository Structure
.
├── bioph.qmd              # Main Quarto manuscript
├── references.bib        # Bibliography
├── data/                 # Variant and structural datasets
├── figures/              # Generated figures and plots
└── README.md
Analyses Performed
Variant Distribution
Variant type frequency analysis
Residue-level mutation mapping
Protein Structure Analysis
Contact network generation
Distance mapping
Centrality calculations
Functional Site Analysis
Identification of top 10% most central residues
Permutation testing for clustering near functional regions
Amino Acid Analysis
Frequency comparison of amino acid substitutions
Pathogenic versus non-pathogenic mutation profiles
Predictive Modeling

Five logistic regression models were compared:

Full model
Degree + betweenness
Degree only
Region only
Betweenness only

Model performance was evaluated using AIC.

Software and Libraries

This project was developed in R using packages for:

Structural bioinformatics
Network analysis
Statistical modeling
Data visualization

Examples include:

bio3d
igraph
tidyverse
ggplot2
stats
Reproducing the Analysis
Requirements
R (≥ 4.0)
Quarto
Render the Manuscript
quarto render bioph.qmd

This will generate the manuscript and associated figures.

Scientific Significance

Understanding the structural determinants of PRNP pathogenicity may:

Improve prediction of disease-associated mutations
Reveal mechanistic drivers of protein misfolding
Identify structurally vulnerable regions in prion proteins
Inform future therapeutic development strategies

Citation

If you use this work, please cite:

Durbin, S.C. Network Analysis of Structural Determinants of Pathogenic Mutations in PRNP. California State University, Los Angeles.

Author

Samuel C. Durbin
Department of Biological Sciences
California State University, Los Angeles

License

This work is distributed under the CC BY license.
