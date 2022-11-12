
 
<h1> DBNex: Deep Belief Network and Explainable AI based Financial Fraud Detection</h1>

[Abhimanyu Bhowmik](https://scholar.google.com/citations?user=r3bzJ7oAAAAJ&hl=en), [Madhushree Sannigrahi](https://scholar.google.com/citations?user=Mtnm7igAAAAJ&hl=en), [Deepraj Chowdhury](https://scholar.google.com/citations?user=9sZgeV4AAAAJ&hl=en), [Ashutosh Dhar Dwivedi](https://scholar.google.com/citations?user=EjGUfp0AAAAJ&hl=en), [Raghava Rao Mukkamala](https://scholar.google.com/citations?user=VkhjFd4AAAAJ&hl=en)

[![paper](https://img.shields.io/badge/IEEE-Paper-brightgreen)](https://doi.org/10.1002/itl2.395) 
[![dataset](https://img.shields.io/badge/Kaggle-Dataset-blue)](https://www.kaggle.com/competitions/ieee-fraud-detection) 
[![dataset](https://img.shields.io/badge/Saved-Models-red)](https://github.com/abhimanyubhowmik/RiceCloud/tree/main/Model)
[![slides](https://img.shields.io/badge/Presentation-Slides-yellow)](https://docs.google.com/presentation/d/1gvCsCyNCn75RjuJnyyVfNFqU01OW1PKzvIrtb3buVqM/edit?usp=sharing) 



> **Abstract:** *The majority of financial transactions are now conducted virtually around the world. The widespread use of credit cards and online transactions encourages fraudulent activity. Thus, one of the most demanding real-world challenges is fraud detection. Unbalanced datasets, in which there are a disproportionately high number of non-fraud samples compared to incidents of fraud, are one of the key obstacles to effective fraud detection. A further factor complicating the learning process for cutting-edge machine learning classifiers is how quickly fraud behaviour changes. Thus, in this study, we suggest an efficient fraud detection methodology. We propose a unique nonlinear embedded clustering to resolve imbalances in the dataset, followed by a Deep Belief network for detecting fraudulent transactions.*

<hr />

<h2>About Dataset</h2>

<h3>Context</h3>

The Credit Card Fraud Detection dataset by Worldline and the Machine Learning Group of ULB (Universit´e Libre de Bruxelles) is used in this paper. It includes labelled anonymized credit card payments made by European card users in September 2013.

<h3>Content</h3>

The dataset contains `492 frauds` out of `284,807 transactions` that took place over the course of `2 days`.

Dataset Specifications:

* PCA (Principle Component Analysis) transformed into features V1, V2,... V28 
* Time
* Amount
* Class

**Note:** Only 0.172% of the transactions in the dataset are fraudulent,
which indicates a severe lack of balance.

Sample Dataset from the actual dataset can be found in the the folder `./Data and Model`.



<h2>Proposed Methods</h2>


<!--
  ======================Global Architecture===========================
                          -->

<h3>1. Globar Architecture</h3>


<br><br>

<div align="center">
<img src = "./Images/Main.png" width="100%">
<p>Overall view of the proposed model: DBNex </p>
</div>

<br>

<!--
  =========================Data Preprocessing========================= 
                          -->
 

<h3>2. Data Preprocessing</h3>

<h4>Uniform Manifold Approximation and Projection (UMAP)</h4>

<div align="center">
<img src = "./Images/UMAP.png" width="70%">
<p>Clustering of UMAP-based 2D embedding of non-fraud samples using DBSCAN </p>
</div>

<h4>Density-Based Spatial Clustering of Applications with Noise or DBSCAN</h4>

<div align="center">
<img src = "./Images/SH.png" width="70%">
<p>Silhouette score of DBSCAN Clusters for non-fraud samples where ϵ ranging from 0.1 to 0.6. </p>
</div>

<br>


<!--
  ============================Model=========================
                          -->

<h3>3. Proposed Model </h3>


<div align="center">
<img src = "./Images/Deep Belief Network.png" width="100%">
<p>Architecture of Deep Belief Network </p>
</div>

<br>




<!--
  ====================================RESULTS===============================
                          -->

<h2>Results </h2>
<h3>1. Classification Report</h3>

<div align="center">
<img src = ".Images/Classification Report.png" width="50%">
<p>Classification report for 70:30 train-validation ratio</p>
</div>


<h3>2. Confusion Matrix</h3>

<div align="center">
<img src = "./Images/Confusion Matrix.png" width="50%">
<p>Confusion matrix: Fraud-NonFraud classes</p>
</div>
<br><br>

<h3>3. ROC - AUC Curve</h3>

<div align="center">
<img src = "./Images/ROC_AUC.png" width="50%">
<p>Receiver operating characteristic curves: Fraud-NonFraud classes</p>
</div>
<br><br>

<h3>4. Classification Explainability using SHAP</h3>

<div align="center">
<table>
  <tr>
    <td width="50%"> <img src = "./Images/Shap 1.png" width="100%"><br>(a) </td>
    <td width="50%"> <img src = "./Images/Shap 2.png" width="100%"><br>(b) </td>
  </tr>
</table>
<p>(a), (b) Beeswarm plot of testing dataset for both the classes (left) Heatmap plot of testing dataset for both the classes (right).</p>
</div>
<br><br>


<hr />

<h2>Cite our work</h2>

    
    Bhowmik A., Sannigrahi M., Chowdhury D., Dwivedi A., Mukkamala R. (2022). DBNex: Deep Belief Network and Explainable AI based Financial Fraud Detection. Acepted in IEEE International Conference on Big Data (IEEE BigData 2022).


<hr />

<h2>Contact</h2>
For any queries, please contact: <a href="mailto:bhowmikabhimnayu@gmail.com">bhowmikabhimnayu@gmail.com</a>