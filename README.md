# Emotion Classification with Transformers

## Overview
This project compares the performance of DistilBERT and RoBERTa models for emotion classification on English text data. 
Part of my Master's coursework in Computational Linguistics.

## Models
- DistilBERT-based-cased: https://huggingface.co/distilbert/distilbert-base-cased
- RoBERTa-base: https://huggingface.co/FacebookAI/roberta-base

## Dataset
mteb/emotion: https://huggingface.co/datasets/mteb/emotion

## Project Status

## Results
*Qualitative Performance*

DistilBERT achieved superior test accuracy (89%) compared to RoBERTa (86%), despite being a smaller model. Both models performed best on joy and sadness (>90%), while struggling with anger (67%) and surprise (0% due to severe class imbalance). DistilBERT showed particularly strong performance on fear (100%) and love (91%), while RoBERTa struggled notably with love classification (55%).

*Quantitative Analysis*

Both models primarily confused similar types of emotions. Negative emotions (sadness/anger/fear) were frequently interchanged, as well as positive emotions (joy/love). Common challenges included distinguishing externally from internally focused emotions, identifying emotions in complex sentences with mixed emotional signals or in short sentences with little to no context.

*Visual Analysis* 

*Embedding visualizations were generated using TensorFlow Projector API from tensor files, providing dimensionality-reduced (PCA) views of token representations across training epochs and model layers.*

The embedding visualizations confirmed the learning process in both models. Early layers maintained generic representation, whereas the final layers showed distinct emotion specific clusters. DistilBERT achieved a well-defined separation after only two epochs due to the higher learning rate, RoBERTa required four epochs. Despite tighter clustering for RoBERTa, DistilBERT demonstrated better generalization.

*Key Finding*

The smaller DistilBERT model outperformed the larger RoBERTa on this limited dataset. This challenges the assumption that larger models always perform better.


---
*This is an academic project for learning purposes.*
