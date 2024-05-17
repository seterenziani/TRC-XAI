# Temporal Relation Classification From An Explainable Perspective

Examining how BERT models of varying sizes handle temporal information in a temporal relation classification task, using a combination of saliency-based and counterfactuals explainability methods. 


## Repository Overview: 
This repository contains all code and created datasets for the project. All notebooks are initialised for BERT-base model. More information on the creation of counterfactual instances, annotations for token partition and analysis is found in the final report. 

[data/annotated](https://github.com/seterenziani/TRC-XAI/tree/main/data/annotated) contains the annotated instances and counterfactually altered instances, used for the analysis. 
* [counterfactuals](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/counterfactuals.csv): dataset containing the counterfactually altered instances from the randomly selected instances from the validation dataset
* [partitions](https://github.com/seterenziani/TRC-XAI/blob/main/data/annotated/partitions.csv): dataset containing the annotattion for positive and negative partition of tokens for the counterfactual instances selected from the validation dataset. 

[model_training](https://github.com/seterenziani/TRC-XAI/blob/main/model_training.ipynb) is a notebook containing the code for fine-tuning each model. 

[explainability](https://github.com/seterenziani/TRC-XAI/tree/main/explainability) contains all code for individual evaluation and includes the creation of saliency scores.  

* [countefactual_evaluation](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/counterfactual_evaluation.ipynb): contains all code for evaluating the countefactually altered instances.
* [integrated_gradients](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/gradients.ipynb): contains all code for computing the saliency-scores using Integrated Gradients.
* [occlusion](https://github.com/seterenziani/TRC-XAI/blob/main/explainability/occlusion.ipynb): contains all code for computing the saliency-scores using Occlusion. 

[explanation_alignment](https://github.com/seterenziani/TRC-XAI/blob/main/explanation_alignment.ipynb) is a notebook containing the code for evaluating the alignment of the used explainability methods.

