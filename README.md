# Temporal Relation Classification From An Explainable Perspective

Examining how BERT models of varying sizes handle temporal information in a temporal relation classification task, using a combination of saliency-based and counterfactuals explainability methods. Defining valid reasoning strategies based on the linguistic principles that guide commonly used temporal annotations, explainability methods are applied to analyse whether a model's decisions are in line with these strategies. For model information about creation of counterfactual instances and analysis is found in the final report ([here](https://github.com/seterenziani/TRC-XAI/blob/main/report.pdf)). 


## Repository Overview: 
This repository contains all code and created datasets for the Bachelor Thesis in Data Science (Spring 2024) at IT University of Copenhagen. The repository is structured into four main components, all initialised for a BERT-base model: 

### 1. Fine-Tuning Model (``model``)
[training](https://github.com/seterenziani/TRC-XAI/blob/main/model_training.ipynb) is a jupyter notebook containing the code for data loading, processing, configuration, fine-tuning and evaluation of each model for a temporal relation classification tak.  
[training modules](https://github.com/seterenziani/TRC-XAI/tree/main/model) is a directory containing the python models for training a temporal relation classification task, including core modul, configuration and pipeline. 

### 2. Created Datasets (``data/annotated``)
A directory containing created and annotated datasets used for analysis. 

* [counterfactuals](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/counterfactuals.csv): dataset containing 200 counterfactually altered instances randomly selected instances from validation dataset
* [partitions](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/partitions.csv): dataset containing 200 counterfactually altered instances annotated for token partitionning

### 3. Individual Explainability Methods (``explainability``) 
A directory containing all code for procedure and evaluation of each individual selected explainability methods. 

* [countefactual_evaluation](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/counterfactual_evaluation.ipynb): a jupyter notebook for evaluating the countefactually altered instances.
* [integrated_gradients](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/gradients.ipynb): a jupyter notebook for computing the saliency-scores using Integrated Gradients.
* [occlusion](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/occlusion.ipynb): a jupyter notebook for computing the saliency-scores using Occlusion.

### 4. Explaination Alignment (``explanation_alignment.ipynb``) 
[explanation_alignment](https://github.com/seterenziani/TRC-XAI/blob/main/explanation_alignment.ipynb) a jupyter notebook containing code for evaluating the explanation alignment of all the selected explainability methods.
