# Multiple Instance Learning for Genetic Mutation Detection in Histopathology

## Background
Some indiviudals have a genetic mutation which makes them resistant to certain types of breast cancer therapy, but respond well to other types. Specifically, being able to detect the PIK3CA genetic mutation in histopathlogy images is an ideal indicator for determining personalized treatment plans that have the highest potential of improving patient outcomes. Currently, expert DNA sequencers analyzed these large histopathology images (of sizes 150,000x200,000 pixels) to detect the mutation and hence determine the treatment. There are limited DNA sequencing experts and the process is time consuming, so not everyone has access to this vital resource. This project attempts to implement deep learning models that can automatically detect the mutation. This streamlining will make breast cancer response faster and its personalization more accessible, both of which increase the chance of better patient outcomes.  

For further details about the background, data, models and results please refer to the project report [TODO-Upload paper](placeholder)

## Setup
1. You will have to download the data from the Challenge Page: [Detecting PIK3CA mutation in breast cancer
by OWKIN](https://challengedata.ens.fr/participants/challenges/98/). Then you must upload the data to the folder called *Data* in this repo. In this folder you should save 3 files *train_metadata.csv*, *test_metadata.csv* and *train_output.csv* and 2 folders called *train* and *test*. In the *train* and *test* folders add the *moco_features* folder, which contains the *.npy* files of moco features (NB adding the tile images is not necessary).
2. Run the *Data_Prep* file, which processes the data and saves it in the *Processed_Data* folder.
3. Now you can run any other file in the repo.

## File Descriptions
- **EDA.ipynb** gives summary statistics of distributions between some of the following: samples with/without the mutation, the centers from which the sample was collected, the patients and the sample zooms.
- **Logistic_Regression.ipynb** creates baseline logistic regression models that make validation and test predictions. The test predictions are stored in the *Predictions* folder (these can be uploaded to the [Challenge Page](https://challengedata.ens.fr/participants/challenges/98/)) to get an AUC score.
- **CHOWDER.ipynb** is an implementation of the model described in this [Paper](https://arxiv.org/pdf/1802.02212.pdf). Predictions are made for validation and test (again the test will be saved in the *Predictions* folder).
- **CHOWDER_tuning.ipynb** is similar to **CHOWDER.ipynb**, except the architecture has been slightly modified and performance on the validation data is printed for different hyperparameter settings (no test predictions are made).
- **Hybrid.ipynb** is a modified version of the tuned CHOWDER model that includes coordinate data. Predictions are made for validation and test (with the test being saved in the *Predictions* folder).
- **Hybrid_Tuning.ipynb** tunes the hybrid model in a similar fashion to **CHOWDER_tuning.ipynb**.
- **Decisive.ipynb** accesses data in the *Decisive* folder and plots visualizations of how good the models in this repo are at making predictions.
- **Development Folder** has other files that were used to generate results for the project report.
  
   
