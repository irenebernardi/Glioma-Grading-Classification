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


## Molecular differences between LGGs and HGGs

## The Learning task 

This project utilizes several machine learning models in order to find the one yielding the best classification results: 
 - Logistic Regression;
 - Decision Trees;
 - Random Forest;
 - AdaBoost.


After data normalization and cleaning, Multiple Correspondance Analysis (MCA) was used as a means for features selection. Then, the two top performing models were selected for improvement via Stratified Cross Validation GridSearch and RandomSearch. 

####INSERT FINAL ACCURACY AND RECALL ####



## The TGCA Dataset

Below is a short description of the function of each gene in the TGCA dataset. 

- **IDH1**: this gene provides instructions to make the isocitrate dehydrogenase 1 enzyme, ultimately protecting cells from oxidative stress. IDH1 mutations can lead to onco-metabolite 2HG production, which contributes to cancer formation, especially gliomas. 

- **TP53**: this gene provides instructions to create a tumor suppressor protein called p53. Protein p53 regulates cell division and prevents excessive and uncontrolled cell proliferation. Mutations on the TP53 gene can lead to dysfunctional activity of the p53 protein, thus disrupting its tumor suppressing role.

- **ATRX**: this gene plays an important role in chromatin remodeling, thus regulating expression of other genes and preventing chromosomal instability. Its exact role in tumor development is not entirely clear. 

- **PTEN**: This gene encodes for a protein phosphatase that promotes cell survival and genomic stability. Its tumor suppressing properties derive from the negative regulation of the PI3K/AKT signaling pathway, which can go awry in case of mutations.
  
- **EGFR**: This gene codes for the epidermal growth factor receptor protein, thus regulating epithelial tissue development. Its mutation can cause overproliferation and tumorogenesis.
  
- **CIC**: This gene codes for the Capicua Transcriptional Repressor protein, which is responsible for preventing the activation of genes downstream of receptor tyrosine kinase (RTK)/Ras/ERK signaling. This tumor suppressing function is halted when the CIC gene is mutated.
  
- **MUC16**: This gene encodes for the glycoprotein CA125, which is an ovarian cancer-related tumor marker. Aberrant expressions of this gene contribute to tumorogenesis and metastatic invasion.
  
- **PIK3CA**: This gene is involved in cell survival, migration and transfer due to its encoding of the p110 alpha (p110α) protein, which helps phosphorylate specific signaling molecules. The unregulated signaling that results from PIK3CA mutations can lead to uncontrolled cell proliferation and development of malignant tissues.
  
- **NF1**: This tumor suppressing gene codes for the neurofibromin protein, which prevents cell overproliferation by inactivating Ras proteins. NF1 mutations decrease overall amounts of neurofibromin, thus halting its negative regulatory function on Ras proteins.
  
- **PIK3R1**: This gene encodes a subunit of the phosphatidylinositol 3-kinase (PI3K), whose function is to regulate the kinase's activity during phosphorylation of signalling molecules. Like for the PIK3CA gene, the role of the subunit in question is important for cell proliferation, migration and survival. Gain of function mutations on the PIK3R1 gene disrupt the subunit's ability to regulate the kinase, leading to uncontrolled signalling.
  
- **FUBP1**: This gene codes for a a single-stranded DNA and RNA binding protein which controls transcription and translation. In some cases, it can act as a tumor suppressor gene, thus mutations can lead to uncontrolled cell growth. In other cases, however, this gene is thought to promote tumor development.
  
- **RB1**: Responsible for coding the tumor suppressing pRB protein, this gene helps ensure normal levels of cell division. Mutations can lead to tumorogenic cell proliferation.
 
- **NOTCH1**: This gene codes for the Notch1 receptor protein, whose successful ligand bindings allows for normal tissue development. Both excessive activation and inactivation of Notch1 signalling can lead to tumor development.
  
- **BCOR**: This gene codes for the BCL6 corepressor, which enhances transcriptional repression and is involved in cell differentiation, stem cell pluripotency maintenance and body structure development. Mutations are common in various types of malignant tumors.
 
- **CSMD3**: Although little research is available on this gene's function, CSMD3 is thought to be involved in dendrite development and is generally highly associated with Tumor Mutation Burden (TMB).
  
- **SMARCA4**: This gene codes for the BRG1 subunit of the SWI/SNF protein complexes, which are involved in chromatin remodeling. Chromatin remodeling regulates gene expression and its disruption is linked tumorogenesis.
  
- **GRIN2A**: This gene encodes the GluN2A protein, which is a subset of the NMDA receptors in the brain. GRIN2A mutations can throw off ionotropic glutamate receptor signalling, which is a phenomenon occurring in malignant tissues.
  
- **IDH2**: This gene encodes for the NADP(+)-dependent isocitrate dehydrogenase, which is relevant for intermediary metabolism and energy production. Like for IDH1, mutations on the IDH2 genes disrupt its usual catalytic activity, thus leading to tumorogenis, especially in glial cells of the CNS.
  
 - **FAT4**: Encoding the FAT tumor suppressor homolog 4 protein, this gene helps regulating cell proliferation. Thus, mutations lead to uncontrolled cell division.
  
 - **PDGFRA**: This gene codes for a receptor termed the Platelet-derived growth factor receptor A, which is a tyrosine kinase receptor. Mutations are linked to idiopathic hypereosinophilic syndrome as well as a variety of cancers, including gliomas.
  
```




##REFERENCES 

https://www.mycancergenome.org/

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6595546/

https://www.ncbi.nlm.nih.gov/gene/114788
