# Temporal Relation Classification From An Explainable Perspective

Examining how BERT models of varying sizes handle temporal information in a temporal relation classification task, using a combination of saliency-based and counterfactuals explainability methods. 

This repository contains all code and created datasets for the Bachelor Thesis in Data Science (Spring 2024) at IT University of Copenhagen


## Repository Overview: 
All notebooks are initialised for BERT-base model. More information on the creation of counterfactual instances, annotations for token partition and analysis is found in the final report. 

[data/annotated](https://github.com/seterenziani/TRC-XAI/tree/main/data/annotated) contains the annotated instances and counterfactually altered instances, used for the analysis. 
* [counterfactuals](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/counterfactuals.csv): dataset containing 200 counterfactually altered instances randomly selected instances from validation dataset
* [partitions](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/partitions.csv): dataset containing 200 counterfactually altered instances annotated for token partitionning 

[explainability](https://github.com/seterenziani/TRC-XAI/tree/main/explainability) contains all code for individual evaluation and includes the creation of saliency scores.  

* [countefactual_evaluation](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/counterfactual_evaluation.ipynb): notebook for evaluating the countefactually altered instances.
* [integrated_gradients](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/gradients.ipynb): notebook for computing the saliency-scores using Integrated Gradients.
* [occlusion](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/occlusion.ipynb): notebook for computing the saliency-scores using Occlusion.


[model_training](https://github.com/seterenziani/TRC-XAI/blob/main/model_training.ipynb) is a notebook containing the code for fine-tuning each model. 

[explanation_alignment](https://github.com/seterenziani/TRC-XAI/blob/main/explanation_alignment.ipynb) is a notebook containing the code for evaluating the alignment of the used explainability methods.
