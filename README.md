# Multiple Instance Learning for Genetic Mutation Detection in Histopathology

## Setup
1. You will have to download the data from the Challenge Page: [Detecting PIK3CA mutation in breast cancer
by OWKIN](https://challengedata.ens.fr/participants/challenges/98/). Then you must upload the data to the folder called *Data* in this repo. In this folder you should save 3 files *train_metadata.csv*, *test_metadata.csv* and *train_output.csv* and 2 folders called *train* and *test*. In the *train* and *test* folders add the *moco_features* folder, which contains the *.npy* files of moco_features (note adding the tile images is not necessary).
2. Run the *Data_Prep* file, which processes the data and saves it in the *Processed_Data* folder
