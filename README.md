# HSP90-QSKR-ML-Models
This is a set of Jupyter Notebook scripts used in this study to construct regression models for various extracted features and the dissociation rate constants of HSP90 inhibitors. The goal is to predict the dissociation rate constant and residence times of HSP90 inhibitors.
==============================================================================================
-----------------------------------------------------------------------------------------------

 This script has been used to generate the results described in: 

 Chao Xu, Xianglei Zhang, Lianghao Zhao, Gennady M. Verkhivkerb,Fang Bai. 
 Accurate characterization of binding kinetics and allosteric mechanisms for the HSP90 chaperone inhibitors using AI-augmented integrative biophysical 
 studies, (2024) submitted.

-------------------------------------------------------------------------------------------

### 1.Prerequisite:

      Python 3 (the script was tested with version  3.11.5) 
      Python libraries required: 
      numpy v1.24.3,   pandas v2.0.3 ,   scikit-learn,   seaborn,   matplotlyb.

--------------------------------------------------------------------------------------------

### 2.Running scripts:

      Script jupyter_notebooks/Model A - ECFP6 - XGBoost - SVR.ipynb
      Script jupyter_notebooks/Model B PaDEL XGBoost SVM Model.ipynb
      Script jupyter_notebooks/Model C DSFE XGBoost SVR Model.ipynb

---------------------------------------------------------------------------------------------

### 3. Method

      Script construct:
		- Regression models, for the prediction of the dissociation rate constant:
	   		eXtreme Gradient Boosting (XGBoost) and Support Vector Machine (SVM) regression: 
                        models are trained on the experimental unbinding rates, koff, on the logarithmic scale

--------------------------------------------------------------------------------------------

### 4. Input Data 

      ../data/HSP90-kbbox-02-03-2020.xlsx
      The Excel file contains a set of kinetic rate constants and SMILE strings for more than 140 small molecule inhibitors of  the N-terminal domain of  heat shock protein 90 (HSP90).
      Date were obtained by SPR measurements (using a single protocol) as a part of the K4DD project
      The experimental data were collected from:
         Daria Kokh (daria.kokh@h-its.org)

####The features of 132 HSP90 inhibitors were extracted from 2D structures, 3D structures, and complex structures:

     1. ../data/ECFP6-fingerprint.csv  
     2. ../data/Descriptors_from_3D_PaDEL.csv
     3. ../data/DSFE_Residue_atom_pair.csv

-------------------------------------------------------------------------------------------------

### 5. Output Data

      - Top 10 Feature Importances.png - This file visualizes the results of feature selection and importance evaluation, highlighting the top ten most important features.
      - Learning curve.png - This image depicts a learning curve, which is used to evaluate the performance of machine learning models.
      - Regression curve of Predicted vs Actual Values.png - This image evaluates the closeness between predicted and actual values of models across ten random data splits.
    


