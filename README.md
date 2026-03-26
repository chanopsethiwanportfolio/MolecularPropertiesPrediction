# Molecular Properties Prediction 
This university project focuses on predicting the biological activity of molecules across 12 different targets, including 7 nuclear receptors and 5 stress response pathways. To achieve this, we use two approaches:

* Traditional machine learning methods, such as tree-based models, which rely on molecular fingerprints as input features.
* Graph-based deep learning methods, which represent molecules as graphs—where atoms are nodes and bonds are edges—and learn directly from this structure using graph neural networks.

By comparing these approaches, the project aims to understand the strengths and limitations of feature-based models versus models that learn directly from molecular structure.

## Introduction
The prediction of molecular properties, particularly their interactions with critical biological targets
such as the androgen receptor, is a fundamental task in computational drug discovery and toxicology.
The androgen receptor, a type of nuclear hormone receptor, plays a key role in physiological processes
by binding to hormones like testosterone. Accurately predicting whether a molecule exhibits biological
activity toward such receptors is essential for identifying potential drug candidates with desirable
therapeutic effects and minimal side effects. In this study, activity is determined based on binary
assay outcomes (active or inactive) provided by the Tox21 dataset.
This study utilises the Tox21 dataset, a well-established benchmark in computational toxicology,
containing data on over 8,000 molecules and their activity across 12 different nuclear receptor and
stress response pathways. Molecules in this dataset are represented using the SMILES (Simplified
Molecular Input Line Entry System) notation, which encodes chemical structures as text, enabling
efficient storage and computational processing.
To predict molecular interactions with the 12 targets in Tox21, we explore two principal approaches:
1. Extended Connectivity Fingerprints (ECFP4): SMILES strings are transformed into
ECFP4 fingerprints, which encode the local atomic environment within a fixed radius. These
fingerprints serve as high-dimensional feature vectors suitable for input into traditional machine
learning models for binary classification tasks. The analysis for this is found in the Part_one directory
2. Graph-Based Representations: Alternatively, SMILES strings can be converted into molec-
ular graphs, where atoms are treated as nodes and chemical bonds as edges. This representation
allows for the application of Graph Neural Networks (GNNs), which are capable of learning
hierarchical and structural features directly from the graph topology. The analysis for this is found in the part_two directory

In this report, we benchmark and compare traditional machine learning models, Logistic Regression, Support Vector Machine (SVM), Random Forest, and XGBoost, with graph-based approaches, including single-task GCN (st-GCN), multi-task GCN (mt-GCN), and Message Passing Neural Networks (MPNN), to evaluate their effectiveness in predicting compound activity within the Tox21 framework.

> For full background, methodology, and evaluation details, please refer to the report Molecular_Properties_Prediction_Paper.pdf.
