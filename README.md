# Glioma-Grading-Classification

This project focuses on accurately categorizing the grade of a particular type of brain tumor, specifically gliomas. To do so, we use the dataset provided by [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/ccg/research/genome-sequencing/tcga). The dataset utilized is sourced from The Cancer Genome Atlas (TCGA). 
The strategy involves exploring possible dimensionality reduction methods, identifying the most effective model from a range of classifiers and enhancing its performance through various techniques, such as grid search and other optimization methods.

## What are gliomas? 
Gliomas are tumors of the glial cells of the central nervous system. Based on cytological characteristics such as cellular anaplasia, nuclear atypia, cell density, mitoses, microvascular proliferation and necrosis, gliomas are divided into the more treatable low-grade gliomas (LGGs) or the highly invasive high-grade gliomas (HGGs). Prognosis and life quality following diagnosis are vastly different between LGGs and HGGs. 
 Table 1 illustrates glioma types and grades, as per the World's Health Organization definitions:

<p align="center">
  <img src="https://github.com/irenebernardi/Glioma-Grading-Classification/blob/main/WHO_glioma_types.png" alt="Glioma Types">
</p>
<p align="center"><em>Table 1</em></p>

## Dataset description 
gene by gene description 

- **IDH1**: this gene provides instructions to make the isocitrate dehydrogenase 1 enzyme, ultimately protecting cells from oxidative stress. IDH1 mutations can lead to onco-metabolite 2HG production, which contributes to glioma formation. 

- **TP53**: this gene provides instructions to create a tumor suppressor protein called p53. Protein p53 regulates cell division and prevents excessive and uncontrolled cell proliferation. Mutations on the TP53 gene can lead to dysfunctional activity of the p53 protein, thus disrupting its tumor suppressing role.

- **ATRX**: this gene plays an important role in chromatin remodeling, thus regulating expression of other genes and preventing chromosomal instability. Its exact role in tumor development is not entirely clear. 

- **PTEN**: This gene encodes for a protein phosphatase that promotes cell survival and genomic stability. Its tumor suppressing properties derive from the negative regulation of the PI3K/AKT signaling pathway, which can go awry in case of mutations.
  
- **EGFR**: This gene codes for the epidermal growth factor receptor protein, thus regulating epithelial tissue development. Its mutation can cause overproliferation and tumorogenesis.
  
- **CIC**: This gene codes for the Capicua Transcriptional Repressor protein, which is responsible for preventing the activation of genes downstream of receptor tyrosine kinase (RTK)/Ras/ERK signaling. This tumor suppressing function is halted when the CIC gene is mutated.
  
- **MUC16**: This gene encodes for the glycoprotein CA125, which is an ovarian cancer-related tumor marker. Aberrant expressions of this gene contribute to tumorogenesis and metastatic invasion.
  
- **PIK3CA**: This gene is involved in cell survival, migration and transfer due to its encoding of the p110 alpha (p110α) protein, which helps phosphorylate specific signaling molecules. The unregulated signaling that results from PIK3CA mutations can lead to uncontrolled cell proliferation and development of malignant tissues.
  
- **NF1**: This tumor suppressing gene codes for the neurofibromin protein, which prevents cell overproliferation by inactivating Ras proteins. NF1 mutations decrease overall amounts of neurofibromin, thus halting its negative regulatory function on Ras proteins.
  
- **PIK3R1**: This gene encodes a subunit of the phosphatidylinositol 3-kinase (PI3K), whose function is to regulate the kinase's activity during phosphorylation of signalling molecules. Like for the PIK3CA gene, the role of the subunit in question is important for cell proliferation, migration and survival. Gain of function mutations on the PIK3R1 gene disrupt the subunit's ability to regulate the kinase, leading to uncontrolled signalling.
  
- **FUBP1**: 
  
- **RB1**: Responsible for coding the tumor suppressing pRB protein, this gene helps ensure normal levels of cell division. Mutations can lead to tumorogenic cell proliferation.
 
- **NOTCH1**: This gene codes for the Notch1 receptor protein, whose successful ligand bindings allows for normal tissue development. Both excessive activation and inactivation of Notch1 signalling can lead to tumor development.
  
- **BCOR**:
- **CSMD3**:
- **SMARCA4**:
- **GRIN2A**:
- **IDH2**:
- **FAT4**:
- **PDGFRA**:
```




##REFERENCES 

https://www.mycancergenome.org/
