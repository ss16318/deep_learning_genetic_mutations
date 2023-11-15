# Multiple Instance Learning for Genetic Mutation Detection in Histopathology

## Setup
1. You will have to download the data from the Challenge Page: [Detecting PIK3CA mutation in breast cancer
by OWKIN](https://challengedata.ens.fr/participants/challenges/98/). Then you must upload the data to the folder called *Data* in this repo. In this folder you should save 3 files *train_metadata.csv*, *test_metadata.csv* and *train_output.csv* and 2 folders called *train* and *test*. In the *train* and *test* folders add the *moco_features* folder, which contains the *.npy* files of moco features (note adding the tile images is not necessary).
2. Run the *Data_Prep* file, which processes the data and saves it in the *Processed_Data* folder.
3. Now you can run any other file in the repo.

## File Descriptions
- **EDA.ipynb** gives summary statistics of distributions between some of the following: samples with the mutation, the center from which the sample was collected, the patient id and the sample zoom.
- **Logistic_Regression.ipynb** creates baseline logistic regression models that make validation and test predictions. The test predictions are stored in the *Predictions* folder (these can be uploaded to the [Challenge Page](https://challengedata.ens.fr/participants/challenges/98/)) to get an AUC score. 
  
   
