# Integration-of-Copy-Number-Vartions-and-Gene-Expressions
This research project aims to investigate molecular data from various platforms for different cancer types. We will focus on Lung Squamous Cell Carcinoma (LUSC) and Kidney Renal Clear Cell Carcinoma (KIRC).

The data for each cancer type will include:

Gene expression (GE): Two datasets per cancer type:
"type-rsem-fpkm-tcga-t_paired.txt" (where "type" is either LUSC or KIRC): This dataset contains gene expression levels for cancerous tissues.
"type-rsem-fpkm-tcga_paired.txt": This dataset contains gene expression levels for healthy tissues (control group).
Both datasets have the same number of samples (patients) in the same order.
The data format is tab-delimited.
Copy number alterations (CNAs): A single file per cancer type containing data on chromosomal segment alterations, including both arm-level and focal-level copy numbers.
The data format is also tab-delimited.
The set of patients in this data might differ from the GE data.
Analysis Steps:

Differential Gene Expression (DEG) Identification:

We will use the volcano plot method (combining hypothesis testing and fold change) to identify genes with significantly different expression levels between cancerous and healthy tissues for each cancer type.
The paired nature of the samples will be considered during the statistical testing.

Top 5 Most Differentially Expressed Genes:

![image](https://github.com/Enas888/Integration-of-Copy-Number-Vartions-and-Gene-Expressions/assets/86245745/cb41c920-33ba-42f4-ac58-7fadd85cd499)

volcano plot:
![image](https://github.com/Enas888/Integration-of-Copy-Number-Vartions-and-Gene-Expressions/assets/86245745/93efff71-ef66-443b-a87b-0c774f4ad802)
