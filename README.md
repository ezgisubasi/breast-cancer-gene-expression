# breast-cancer-gene-expression

<p align="center"> 
   <img width="800" alt="Ekran Resmi 2021-06-28 01 15 28" src="https://user-images.githubusercontent.com/52889449/123560979-6b55d280-d7ae-11eb-8e97-82b997e5ab56.png">
</p>

This project aims to predict people who will survive breast cancer using machine learning models with the help of clinical data and gene expression profiles of the patients. Using machine learning models on gene data helps us better understand the disease and determine how well treatment methods work.

# What is Breast Cancer?

Breast cancer is a type of cancer that occurs when some cells in the breast grow excessively. This type of cancer causes the greatest number of cancer-related deaths among women. There are 5 known types of breast cancer based on the occurrence of the tumor as you can see in the figure. These genes can be also passed from parent to child. Therefore, breast cancer is also a genetically transmitted cancer type.

<p align="center">    
  <img width="300" alt="Ekran Resmi 2021-06-28 01 31 00" src="https://user-images.githubusercontent.com/52889449/123561347-83c6ec80-d7b0-11eb-8653-3aa61952e1fe.png">
   <img width="450" alt="Ekran Resmi 2021-06-28 01 27 32" src="https://user-images.githubusercontent.com/52889449/123561291-131fd000-d7b0-11eb-8481-1a0e362d6c2c.png">   
</p>

# Dataset

This dataset includes 31 clinical attributes, mRNA levels z-score for 331 genes, and mutation in 175 genes for 1904 breast cancer patients. 

# Importance of the Genes

**BRCA1 and BRCA2:** The most common cause of hereditary breast cancer is an inherited mutation in the BRCA1 or BRCA2 gene. In normal cells, these genes help make proteins that repair damaged DNA. Mutated versions of these genes can lead to abnormal cell growth, which can lead to cancer.

**Other Genes:** These gene mutations are much less common, and most of them do not increase the risk of breast cancer as much as the BRCA genes. Some of them are ATM, TP53, CHEK2, PTEN, CDH1, STK11 and PALB2.

# Data Preprocessing
 
In the preprocessing part, first I cleaned the data and according to skew-distribution fill the missing values with the mode of them. After that, I applied Label Encoding and One-Hot Encoding to the categorical clinic data respectively.

## Label Encoding:

The following categorical features are ordinal data encoded with the label encoding method.

* cellularity
* cancer_type_detailed
* type_of_breast_surgery
* her2_status_measured_by_snp6
* pam50_+_claudin-low_subtype
* her2_status_measured_by_snp6
* tumor_other_histologic_subtype
* integrative_cluster
* 3-gene_classifier_subtype
* death_from_cancer

## One-Hot Encoding:

The following categorical features are nominal data encoded with the one-hot encoding method.

* er_status_measured_by_ihc
* er_status, her2_status
* inferred_menopausal_state
* primary_tumor_laterality
* pr_status
* oncotree_code

# Data Visualization

In order to better understand the data and make some inferences, I analyzed using the following data visualization techniques.

## Correlation Matrix

<p align="center"> 
<img width="700" alt="Ekran Resmi 2021-06-27 19 12 24" src="https://user-images.githubusercontent.com/52889449/123551809-f8cbff00-d77b-11eb-99fc-2fe436a8a038.png">
</p>

## Treatment Types & Survivals

<p align="center"> 
  <img width="650" alt="Ekran Resmi 2021-06-27 19 12 41" src="https://user-images.githubusercontent.com/52889449/123551763-cde1ab00-d77b-11eb-94b8-87aaab431208.png">  
</p>

## Survived Patients by Treatment Groups

<p align="center"> 
  <img width="450" alt="Ekran Resmi 2021-06-27 19 12 58" src="https://user-images.githubusercontent.com/52889449/123551766-d0440500-d77b-11eb-99b4-2442bd28ee51.png">
</p>


# Choosing Best PCA

PCA is an algorithm that reduces the dimension of datasets that have a high number of features. When dealing with the PCA, the scikit-learn library can be used to determine the number of components of the newly created data set. As you can see in the below plot, to get 95% of variance explained I need 375 principal components.

<p align="center"> 
 <img width="580" alt="Ekran Resmi 2021-06-27 19 13 14" src="https://user-images.githubusercontent.com/52889449/123551772-d5a14f80-d77b-11eb-945d-ea587124ecd6.png">
</p>


# Accuracy Scores


   | Model                | Train Score  | Test Score   |
   | :-------------:      | :----------: | :-----------:|
   |  KNN                 | 0.75         | 0.73         |
   |  Logistic Regression | 0.82         | 0.89         |
   |  Random Forest       | 1.0          | 0.62         |
   |  Decision Tree       | 0.69         | 0.62         |
   |  Extra Trees         | 0.93         | 0.58         |
   |  AdaBoost            | 1.0          | 0.65         |



   <img width="430" alt="Ekran Resmi 2021-06-28 00 54 17" src="https://user-images.githubusercontent.com/52889449/123560540-7ce9ab00-d7ab-11eb-827a-092226e5500a.png">


# References:

1) https://www.nature.com/articles/s41523-018-0056-8
2) https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5461908/
