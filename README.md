# Glioma-Grading-Classification

This project focuses on accurately categorizing the grade of a particular type of brain tumor, specifically gliomas. To do so, we use the dataset provided by [The Cancer Genome Atlas (TCGA)](https://www.cancer.gov/ccg/research/genome-sequencing/tcga). The dataset utilized is sourced from The Cancer Genome Atlas (TCGA). 
The strategy involves exploring possible dimensionality reduction methods, identifying the most effective model from a range of classifiers and enhancing its performance through various techniques, such as grid search and other hyperparameter optimization methods.

For more information on the approach used for this learning task, find the project's Final Report [here](https://docs.google.com/document/d/1WxLBC6T_l1TTZhtdoD_HsKLFNC4JgfH9i8zQkEs4j6g/edit).

For a different approach to this classification task, please refer to the *Glioma Grading Clinical and Mutation Features* paper by Tasci, E., Zhuge, Y., Kaur, H., Camphausen, K., & Krauze, A. V. (2022), available in the References section below. 

## What are gliomas? 
Gliomas are tumors of the glial cells of the central nervous system. Based on cytological characteristics such as cellular anaplasia, nuclear atypia, cell density, mitoses, microvascular proliferation and necrosis, gliomas are divided into the more treatable low-grade gliomas (LGGs) or the highly invasive high-grade gliomas (HGGs). Prognosis and life quality following diagnosis are vastly different between LGGs and HGGs. 
 Table 1 illustrates glioma types and grades, as per the World's Health Organization definitions:

<p align="center">
  <img src="https://github.com/irenebernardi/Glioma-Grading-Classification/blob/main/WHO_glioma_types.png" alt="Glioma Types">
</p>
<p align="center"><em>Table 1: WHO Glioma Types and Grade Classification</em></p>


## Molecular and clinical differences between LGGs and HGGs

The mutations most relevant for glioma development occur on genes IDH1/2, TP53, ATRX, EGFR and PTEN. 
Specifically, grade II and III gliomas are usually characterized by isocitrate
Dehydrogenase (IDH) mutations, which are also seen in secondary Glioblastomas, which evolve from lower grade tumors. 
On the other hand, IDH mutations are not present in primary Glioblastomas, which emerge spontaneously in patients with no prior history of glioma. In these cases, mutations usually occur on the proto-oncogene EGFR and on the phosphatase and tensin homologue PTEN.
Concerning the clinical features of age and gender,  it should be noted that GBM mostly occurs in people over 40 years old (referencethis https://www.mdpi.com/2072-6694/14/10/2412) whereas LGG tend to affect younger populations (https://www.nature.com/articles/d41591-023-00054-2). Across ages, males tend to be more affected than women, but the exact molecular reasons for gender differences in glioma development are unclear. This gender difference is more pronounced for GBM than for LGG. 


#####TODO: reference below:######
IDH mutation testing is a valuable diagnostic, prognostic and predictive biomarker for the management of patients with glial tumours. IDH1 and IDH2 mutations occur in a mutually exclusive manner in nearly 80% of grades II and III oligodendrogliomas and astrocytomas and secondary glioblastomas (i.e. glioblastomas that had progressed from lower grade gliomas) 10,11,12,3,13. Conversely, IDH mutations are found in only 6% of patients with primary glioblastoma. Molecular classification of gliomas divides these malignancies primarily into IDH-mutant and IDH-wild tumours, the latter being mainly represented by World Health Organization (WHO) grade IV primary glioblastomas 14. The presence of IDH mutations defines a distinct tumour subset with specific clinical and molecular characteristics, suggesting that these predominantly grades II and III tumours have distinct pathogenic origins from that of primary IDH-wild type glioblastomas 10,11,12,3. In gliomas, clinical features that have been associated with the presence of IDH mutation include younger age at presentation, tendency for frontal lobe location, more frequent non-enhancing tumour infiltrative component and more favourable outcome.


## The Learning task 

This project utilizes several machine learning models in order to find the one yielding the best classification results: 
 - Logistic Regression;
 - Decision Trees;
 - Random Forest;
 - AdaBoost.


After data normalization and cleaning, Multiple Correspondance Analysis (MCA) was used as a means for features selection. Then, the two top performing models were selected for improvement via Stratified Cross Validation GridSearch and RandomSearch. 

The final performance of our top two models is the following: 
- Logistic Regression:
  - Accuracy: 0.8611
  - Recall (Sensitivity): 0.9182
  - ROC AUC Score: 0.8675
- AdaBoost:
  - Accuracy: 0.8571
  - Recall (Sensitivity): 0.8909
  - ROC AUC Score: 0.8609

## Insight on the TGCA Dataset

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
  


## References

Molinaro, A. M., Taylor, J. W., Wiencke, J. K., Wrensch, M. R. (2019). Genetic and molecular epidemiology of adult diffuse glioma. Nature Reviews Neurology, 15(7), 405–417. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7014190/

National Cancer Institute (NCI). The Cancer Genome Atlas (TCGA). Retrieved from https://www.cancer.gov/ccg/research/genome-sequencing/tcga

Ostrom, Q. T., Gittleman, H., Truitt, G., Boscia, A., Kruchko, C., Barnholtz-Sloan, J. S. (2020). CBTRUS Statistical Report: Primary Brain and Other Central Nervous System Tumors Diagnosed in the United States in 2013–2017. Neuro-Oncology, 22(12), iv1–iv96. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7727433/

Stupp, R., Mason, W. P., van den Bent, M. J., Weller, M., Fisher, B., Taphoorn, M. J. B. & Mirimanoff, R. O. (2005). Radiotherapy plus concomitant and adjuvant temozolomide for glioblastoma. New England Journal of Medicine, 352(10), 987–996. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9826661/

Tasci, E., Zhuge, Y., Kaur, H., Camphausen, K., & Krauze, A. V. (2022). Hierarchical Voting-Based Feature Selection and Ensemble Learning Model Scheme for Glioma Grading with Clinical and Molecular Characteristics. International Journal of Molecular Sciences, 23(22), 14155.

Trusheim, M. R., Berndt, E. R., Douglas, F. L. (2007). Stratified medicine: strategic and economic implications of combining drugs and clinical biomarkers. Nature Reviews Drug Discovery, 6(4), 287–293. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7014190/

