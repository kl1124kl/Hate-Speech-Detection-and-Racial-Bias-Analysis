Hate Speech Detection and Racial Bias Analysis
Overview
This project investigates racial and dialectal bias in automated hate speech classification systems. Toxic language detection models are increasingly deployed at scale, but prior research has shown they can disproportionately flag text written in African American English (AAE) as toxic, even when the content isn't hateful. This project analyzes that bias across two benchmark datasets and explores mitigation techniques including BERT-based classification, adversarial de-biasing, and up-sampling.
Team project completed for CSCI 544 (Applied Natural Language Processing) at USC, with contributions from multiple team members across dataset analysis, modeling, and bias mitigation.
My Contribution
I led the bias measurement analysis (dataset_bias_analysis.ipynb):

Merged AAE dialect-probability scores into two benchmark datasets, DWMW17 and FDCL18 (~125K combined tweets)
Computed Pearson correlations between AAE probability and label categories (hateful, abusive, offensive, normal/neither) on both datasets
Found that AAE probability was positively correlated with "abusive"/"offensive" labels and negatively correlated with "normal"/"neither" labels — quantitative evidence of racial bias in the datasets' ground-truth labels
This analysis motivated the team's subsequent mitigation work, including adversarial de-biasing and up-sampling approaches implemented by other team members

Datasets

DWMW17 (Davidson et al., 2017) — annotated tweets labeled as hate speech, offensive language, or neither
FDCL18 (Founta et al., 2018) — annotated tweets labeled across abusive, hateful, spam, and normal categories

Full Project Scope
Beyond my contribution, the team also implemented:

BERT-based hate speech classifiers (bert_dw.ipynb, bert_fdcl.ipynb)
LSTM-based classification and evaluation (LSTM_and_Bias_Evaluation.ipynb, LSTM_and_Bias_Evaluation-upsample.ipynb)
Adversarial de-biasing techniques (Adversarial Debiasing/)

See the original repository for full commit history and team attribution.
Tech Stack
Python, Pandas, NumPy, SciPy (Pearson correlation), NLTK
