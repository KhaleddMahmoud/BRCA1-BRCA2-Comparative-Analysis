# Comparative Analysis of BRCA1 and BRCA2 Genes Across Mammalian Species

## Project Overview

This project focuses on the comparative analysis of the BRCA1 and BRCA2 genes across ten mammalian species. These genes are crucial for maintaining genomic stability and are associated with elevated risks of breast and ovarian cancers when mutated. The analysis aims to elucidate evolutionary relationships, conservation patterns, and functional domains of these genes using advanced bioinformatics tools and databases.

## Objectives

- Retrieve protein sequences for BRCA1 and BRCA2 from multiple mammalian species.
- Conduct pairwise sequence alignment to compare sequence similarities.
- Perform multiple sequence alignment (MSA) to identify conserved regions and functional domains.
- Construct phylogenetic trees to analyze evolutionary relationships.
- Identify conserved motifs and domains in the BRCA1 and BRCA2 proteins.

## Methods

### I. Data Retrieval
Protein sequences for BRCA1 and BRCA2 were retrieved from NCBI and UniProt databases. The species included:
- **BRCA1**: Norway rat, human, dog, chimpanzee, house mouse, rhesus monkey, desert hamster, western gorilla, Bornean orangutan, and cattle.
- **BRCA2**: House mouse, human, dog, woodchuck, American wolverine, desert hamster, Norway rat, domestic cat, chimpanzee, and Egyptian rousette.

Sequences were fetched using Biopython's `Entrez` and `SeqIO` modules, with error handling for missing files and retrieval issues.

### II. Pairwise Sequence Alignment
Pairwise alignments were performed using Biopython’s `pairwise2` module. Global alignments were conducted with a simple scoring scheme, and results were visualized using heatmaps generated with Matplotlib. The heatmaps and tables provided insights into sequence conservation across species.

### III. Multiple Sequence Alignment (MSA)
MSA was performed using Clustal Omega through Biopython's `ClustalOmegaCommandline` module. The aligned sequences were analyzed to identify conserved regions and functional domains. The MSA highlighted essential domains for DNA repair and genomic stability.

### IV. Phylogenetic Tree Construction
Phylogenetic trees were constructed to analyze evolutionary relationships. Distance matrices and neighbor-joining trees were created using BioPython's `DistanceCalculator` and `DistanceTreeConstructor`. The trees were visualized using `Phylo.draw` and `Matplotlib`, revealing genetic similarities and divergences among species.

### VI. Identification of Conserved Domains
Conserved Domain Database (CDD) domains were identified using Entrez and custom Python functions. Results were systematically recorded to facilitate the analysis of conserved protein domains across species.

## Results

### Pairwise Sequence Alignment
- **High Conservation**: Observed among primates (human, chimpanzee, gorilla) with bright yellow in heatmaps indicating high alignment scores.
- **Moderate Conservation**: Seen in non-primates like dogs, cows, and rodents, reflecting evolutionary divergence while retaining functional regions.
- **Low Conservation**: Noted between distantly related species, highlighting evolutionary differences.

### Multiple Sequence Alignment (MSA)
- **BRCA1**: Revealed high conservation in functional domains such as RING finger and BRCT domains.
- **BRCA2**: Identified conserved domains including BRCA2DBD_OB2 and BRCA-2_OB1, with unique domains like 235kDa-fam in certain species.

### Phylogenetic Tree Construction
- Phylogenetic trees demonstrated close relationships between humans, chimpanzees, and gorillas, and between house mice and Norway rats.
- Branch lengths indicated varying degrees of evolutionary divergence among species.

### Motif Analysis
- Identified 20 distinct motifs in BRCA1 with significant sequence similarity and statistical significance.
- Motif correlations indicated functional roles within the BRCA1 protein structure, with high E-values suggesting robust matches.

## Conclusion

The analysis underscores the high conservation of BRCA1 and BRCA2 across diverse mammalian species, particularly in essential functional domains. The study highlights evolutionary patterns and functional adaptations, providing valuable insights into these critical genes' roles in DNA repair and cancer biology.

## Dependencies

- Biopython
- Clustal Omega
- Matplotlib

## Instructions

1. **Install Dependencies**: Ensure all required packages are installed. Use `pip` to install Biopython, Matplotlib, and other necessary libraries.
2. **Data Retrieval**: Download BRCA1_seq_id.txt, BRCA2_seq_id.txt and use the provided Python scripts to fetch sequences from NCBI and UniProt.
3. **Pairwise Alignment**: Run the pairwise alignment scripts to generate alignment scores and heatmaps.
4. **MSA**: Perform multiple sequence alignment using Clustal Omega and analyze the results.
5. **Phylogenetic Trees**: Construct and visualize phylogenetic trees using the provided methods.
6. **Domain Analysis**: Use CDD to analyze conserved domains.

For detailed scripts and data files, refer to the project directory.



