# breast-cancer-gene-expression

This project aims to predict people who will survive breast cancer using machine learning models with the help of clinical data and gene expression profiles of the patients. Using machine learning models on gene data helps us better understand the disease and determine how well treatment methods work.

# What is Breast Cancer? **

Breast cancer is a type of cancer that occurs when some cells in the breast grow excessively. This type of cancer causes the greatest number of cancer-related deaths among women.

There are 5 known types of breast cancer based on the occurrence of the tumor as you can see in the figure.

# Dataset

This dataset includes 31 clinical attributes, mRNA levels z-score for 331 genes, and mutation in 175 genes for 1904 breast cancer patients. The following table contains clinic data attributes along with their descriptions.

# Importance of the Genes

**BRCA1 and BRCA2:** The most common cause of hereditary breast cancer is an inherited mutation in the BRCA1 or BRCA2 gene. In normal cells, these genes help make proteins that repair damaged DNA. Mutated versions of these genes can lead to abnormal cell growth, which can lead to cancer.

**Other Genes:** These gene mutations are much less common, and most of them do not increase the risk of breast cancer as much as the BRCA genes. Some of them are ATM, TP53, CHEK2, PTEN, CDH1, STK11 and PALB2.

# Data Preprocessing
 
 In the preprocessing part, first I cleaned the data and according to skew-distribution fill the missing values with the mode of them. After that, I applied Label Encoding and One-Hot Encoding to the categorical clinic data respectively.

## Label Encoding:



## One-Hot Encoding:


# Data Visualization


## Correlation Matrix

<p align="center"> 
<img width="700" alt="Ekran Resmi 2021-06-27 19 12 24" src="https://user-images.githubusercontent.com/52889449/123551809-f8cbff00-d77b-11eb-99fc-2fe436a8a038.png">
</p>

## Treatment Types & Survivals

<p align="center"> 
  <img width="700" alt="Ekran Resmi 2021-06-27 19 12 41" src="https://user-images.githubusercontent.com/52889449/123551763-cde1ab00-d77b-11eb-94b8-87aaab431208.png">  
</p>

## Survived Patients by Treatment Groups

<p align="center"> 
  <img width="500" alt="Ekran Resmi 2021-06-27 19 12 58" src="https://user-images.githubusercontent.com/52889449/123551766-d0440500-d77b-11eb-99b4-2442bd28ee51.png">
</p>


# Choosing Best PCA

  <p align="center"> 
    <img width="600" alt="Ekran Resmi 2021-06-27 19 13 14" src="https://user-images.githubusercontent.com/52889449/123551772-d5a14f80-d77b-11eb-945d-ea587124ecd6.png">
</p>


# Machine Learning Models


# Conclusion
