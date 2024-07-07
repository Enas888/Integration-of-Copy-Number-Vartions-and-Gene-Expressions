# Integration-of-Copy-Number-Vartions-and-Gene-Expressions
a study to analyze multi-platform molecular data for different types of cancer. The cancer types are: 
1. Lung Squamous Cell Carcinoma (LUSC)
2. Kidney Renal Clear Cell Carcinoma (KIRC).


The data for each cancer type:
1. Gene expression (GE),
◦ Two GE files for each cancer type:
1. “type-rsem-fpkm-tcga-t_paired.txt”, where type {lusc, kirc}: GE ∈ data for tissues with
cancer,
2. “type-rsem-fpkm-tcga_paired.txt”: GE data for tissues in a healthy case.
◦ Data are paired: each GE file will have the same number of cases (patients) and in the same
order.
◦ Files are tab-separated.
2. Copy number alterations (CNAs).
◦ A single file per cancer having the CNAs data for chromosome segments: arm-level and
focal-level copy numbers.
◦ Files are tab-separated.
◦ The set of cases may differ from those of the GE data.

1. DEGs Identification. For each cancer type, infer the differentially expressed genes (DEGs).
◦ Use the volcano plot method (hypothesis testing + fold change) to identify DEGs.
▪ Consider samples are paired for the hypothesis testing step.
2. Regression. For each cancer type, perform a multivariable regression analysis.
◦ The dependent variable is the gene expression for one gene, and the independent variables
are all the CNAs.
◦ Pick up the five most differentially expressed genes in Requirement 1 and perform the
multivariable regression analysis on each one of these five genes separately.
◦ The set of cases (subjects) in the CNAs profiles and the GE profiles are not identical. You
need to make the regression analysis on the intersection of these cases.
◦ Report the significant copy number predictors for each gene.
• Support your findings/results/conclusions with figures.

Top 5 Most Differentially Expressed Genes:
      Hugo_Symbol  Fold Change  Abs Fold Change       P-value
14249        BAAT     7.983620         7.983620  5.970813e-07
19155        UMOD    -7.795541         7.795541  8.734004e-13
18642       FXYD4    -7.729625         7.729625  7.989555e-13
12591        AQP2    -7.649032         7.649032  7.987607e-13
17104        ELF5    -7.415541         7.415541  8.353644e-13
volcano plot:
![image](https://github.com/Enas888/Integration-of-Copy-Number-Vartions-and-Gene-Expressions/assets/86245745/93efff71-ef66-443b-a87b-0c774f4ad802)
