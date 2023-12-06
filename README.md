# Machine Translation Checkpoint Experiments

## Overview

This Jupyter notebook conducts experiments with different machine translation models from HuggingFace to translate text from English to French. The models compared are:

- Helsinki-NLP/opus-mt-en-fr: Baseline model
- huggingface-course/marian-finetuned-kde4-en-to-fr: Finetuned model 

The objective is to evaluate the translation quality of these models by training them on different sized datasets and measuring the BLEU score and BERT score.

## Notebooks Contents

The notebook contains code and Markdown cells to:

- Set up the environment
- Define helper functions to load datasets, tokenize, train models etc. 
- Load and preprocess the kde4 English-French dataset
- Initialize the Helsinki-NLP and Marian models
- Train the models end-to-end on subsets of the data
- Evaluate using BLEU and BERT score
- Log metrics to Weights & Biases

## Conclusion

The key conclusions from the experiments are:

- The Marian model fine-tuned on the kde4 dataset significantly outperforms the baseline Helsinki model with over 10 BLEU score points difference
- Increasing training data from 1000 samples to 3000 further improves Marian's BLEU by 1 point showing the value of more data
- The optimization settings used including Adam optimizer and linear LR decay schedule work well 

Overall, the notebook provides a solid workflow to systematically benchmark and improve translation quality using HuggingFace transformers. The readme summarizes the key contents and findings.