# Chaii-Hindi-Tamil-QA:
With nearly 1.4 billion people, India is the second-most populated country in the world. Yet Indian languages, like Hindi and Tamil, are underrepresented on the web. Popular Natural Language Understanding (NLU) models perform worse with Indian languages compared to English, the effects of which lead to subpar experiences in downstream web applications for Indian users. 

Predicting answers to questions is a common NLU task, but not for Hindi and Tamil. Current progress on multilingual modeling requires a concentrated effort to generate high-quality datasets and modelling improvements. Additionally, for languages that are typically underrepresented in public datasets, it can be difficult to build trustworthy evaluations.

In this competition, our goal is to predict answers to real questions about Wikipedia articles.

# Three scripts:
# 1.Training:
Training data was divided into six folds .Six models have been build.Each model was build by fine tuning xlm-roberta large squad2 transformer model provided in Huggingface Transformer library.xlm-robert-large is a very large model thats the reason only one epoch for each fold was used.
For example,ith model was trainned on data other than ith fold.
To train the six models we need to run the chaii-hindi-tamil.ipynb script six times because of memory contraints in Kaggle platform as well as in colab.
Each model's weight has been saved in separate folder. Those weights were used during inference.

# 2.Inference:
Prediction was done by just averaging the output of each model.

# 3. Validation:
Jaccard score was obtained for each fold corresponding to each model.For example ith model was trainned on data other than ith fold and Jaccard score(ith model score) was obtained on the ith fold which was not used during training of the ith model.



