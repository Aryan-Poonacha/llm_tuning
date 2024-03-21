
# Finetuning Superlightweight Gemma-2B and Comparing Baseline Vs. Finetuned For Humor Detection
This project aims to finetune a lightweight Gemma-2B model with a custom dataset for humor detection. The project involves several steps:

## 1. Setting Up The Data
The first step is to import the necessary libraries and load the dataset. The dataset is split into training and testing sets. The training set is converted into a Dataset object from the datasets library.

## 2. Loading the Tokenizer and the Model for 2B
The tokenizer and the model for 2B are loaded using the AutoTokenizer and AutoModelForCausalLM classes from the transformers library.

## 3. Testing the Baseline Model on the Test Set
The baseline model is tested on the test set. The model is prompted to classify humor with the provided text. The function classify_humor_2b takes a text as input and returns whether the text contains humor or not.

## 4. Finetuning the Model
The model is finetuned using the SFTTrainer class from the trl library. The finetuned model is saved for later use.

## 5. Testing the Finetuned Model
The finetuned model is loaded and tested on the test set. The function classify_humor_tuned2b is similar to classify_humor_2b, but uses the finetuned model instead of the baseline model.

The results of the finetuned model are compared with the baseline model to evaluate the performance improvement. The classification report and confusion matrix are generated and saved for further analysis.