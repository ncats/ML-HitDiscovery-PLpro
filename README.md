# Applications of Machine Learning Approaches for Discovery of SARS-CoV-2 PLpro Inhibitors
This repository is under the NCATS organization. It documents computational workflows, datasets, and results from a study focused on discovering potential inhibitors for the SARS-CoV-2 PLpro protein. The study uses machine learning (ML) models and high-throughput screening data to identify promising hit compounds

**Project Overview**

The primary goal of this research work is to identify and validate compounds with potential inhibitory activity against the SARS-CoV-2 PLpro protein, an essential viral protein involved in viral replication. This work was conducted as part of the APP project at NCATS.

**Key Objectives**

•	Develop ML models based on high-throughput screening data to predict activity against PLpro.  
•	Perform virtual screening using optimized ML models to identify promising hit compounds from the in-house Genesis molecular library.  
•	Provide all workflows, datasets, and selected hit compounds here for reproducibility and further research.

**Repository Contents**

This repository contains the following:

**KNIME Workflows**  
-	_Hyperparameter Optimization Workflows_:
    -	`random_forest_hyperopt.knwf`: A workflow for hyperparameter optimization of Random Forest model, using different combinations of Avalon, Morgan, and Atom-pair fingerprints along with RDKit descriptors.  
    - `gradient_boost_hyperopt.knwf`: A workflow for hyperparameter optimization of Gradient Boosting model, with the same variations of fingerprints and descriptors.  
    - `xgboost_hyperopt.knwf`: A workflow for hyperparameter optimization of an XGBoost model, using the fingerprint and descriptor combinations mentioned above.  

- _Virtual Screening Workflow_:
  - virtual_screening_workflow.knwf: Represents the virtual screening workflow against the Genesis molecular library, using the best optimized ML model for hit discovery.

**Screening Data**

- `Genesis_library/`: Contains high-throughput screening data for a small subset of the Genesis library.
    - `primary_assay_data.csv`: Data from the initial primary assay screening.
    - `confirmed_active_compounds.csv`: List of active compounds confirmed by follow-up assays.
- `NPCAT_library/`: Contains high-throughput screening data for a subset of the NPCAT library.
    - primary_assay_data.csv: Data from the initial primary assay screening.
    - confirmed_active_compounds.csv: List of active compounds confirmed by follow-up assays.
