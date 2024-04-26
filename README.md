# COMP90051 Statistical Machine Learning 
## Project 1 - Group 14
This repo has all the docs for our project. We were tasked with building a model to classify text data from two different domains, one of which had unbalanced data labels. We tried different NLP methods for feature extraction and contextual representation, and tested different method of ML and DL on them.

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-2-blue.svg?style=flat-round)](#contributors-)

## Table of Contents

  1. [Results obtained](#results-obtained)
  2. [Repository Structure](#repository-structure)
  3. [Contributors](#contributors)

## Results Obtained
The best obtained model positioned us in the 2nd position in the public leaderboard at the time of the close of the competition. The main reason for such a result is related to the contextual representation of the features, where the combination of the CountVectorizer with the n-grams of each text retains the most important features of each text class making them easily differentiable. Bellow there is a detail of the obtained results:

| Model                        | Accuracy | F1 Score | Roc AUC | Kaggle Score |
|------------------------------|----------|----------|---------|--------------|
| Weighted Logistic Regression |   0.933  |   0.933  |  0.933  |     0.925    |
| Support Vector Machine       |   0.933  |   0.933  |  0.933  |     0.926    |
| Ridge Classifier             |   0.928  |   0.929  |  0.897  |     0.922    |
| BoW + FFNN                   |   0.928  |   0.929  |  0.928  |     0.914    |
| BiLSTM + DANN                |   0.730  |   0.674  |  0.730  |     0.730    |
| **Ensemble (Top 3 models)**  |   **-**  |   **-**  |  **-**  |   **0.934**  |

On the private score publication the obtained score increased to 0.941:

<center><img src=/Documents/Competition_results.png></center>

## Repository Structure
The repository is organized in 3 main folders:  
```  
├── /Data -> Contains the input files to train and test the models  
├── /Documents -> Contains the meeting minutes and the final report of the project  
├── /Models -> Contains the final models used within the project.   
│   ├── /BiLSTM_DANN.ipynb           -> Bidirectional Long Sort Term Memory Neural Network (BiLSTM) feeding a Domain Adversarial Neural Network (DANN) for data generalization  
│   ├── /BoW_NN.ipynb                -> CoutVectorizer Bag of Words (BoW) passed through a Feed Forward Newran Network (FFNN)  
│   ├── /Ridge regression.ipynb      -> Ridge regression applied to the BoW contextual representation.  
│   ├── /Weighted LR.ipynb           -> Weighted Logistic Regression applied to the BoW contextual representation.  
│   ├── /SVM.ipynb                   -> Linear Weighted Support Vector Machine applied to the BoW contextual representation.   
│   ├── /Ensemble.ipynb              -> Ensemble model with majority voting.  
```  

## Contributors

Thanks to this great team!

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://www.linkedin.com/in/andres-felipe-gutierrez-carre%C3%B1o-62242378/"><img src="https://drive.google.com/uc?export=view&id=1IDlBkB-iwdk8pSx7dLAciDCAumrnsGhq" width="100px;" alt=""/><br /><sub><b>Andrés Gutierrez</b></sub></a><br /></td>
    <td align="center"><img src="https://avatars.githubusercontent.com/u/131924187?v=4" width="100px;" alt=""/><br /><sub><b>Ojaswi Dheer</b></sub></a><br /></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
