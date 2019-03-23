# Billboard

## MSD
The Million Songs Dataset, but we only keep the Additional/subset_unique_tracks.txt file since we only need the title and artist name for each tracks.

## tmp

If you don't care how we fetch the data, just ignore this folder.

We store all the temperory file here. The order is:
* hot_100.xlsx: inlcudes all the tracks in hot-100 from 1990-01-01 to 2019-03-21
* MSD_10000.xlsx: includes all the tracks (10000 in total) in MSD dataset
* feature_1990_2019.xlsx: includes features we extract from spotify API for all the tracks in hot_100.xlsx and MSD_10000.xlsx
* feature_complete_1990_2019.xlsx: here we add "artist_score" feature to feature_1990_2019
* feature_complete_normalized_1990_2019.xlsx: we normalized the features to have zero mean and one std in feature_complete_1990_2019

## test_set and train_set:
Training data and testing data are splited from ./tmp/feature_complete_normalized_1990_2019.xlsx by 75:25 ratio.
* train.xlsx: includes 8624 samples, of which 4695 are positve and 3929 are negative.
* test.xlsx: includes 2875 samples, of which 1553 are postive and 1322 are negative.

## weights
Here we store the weights of neural network.

## history
Here we store the training and testing history of neural network.

## nn.py
Implementation of neural network mdoel.

## SVM.py
Implementation of SVM.

## tree.py
Implementation of tree.

## forest.py
Implementation of random forest.

## Basic Result

|   Model |      train accuracy     |  test accuracy |
|----------|:-------------:|------:|
| SVM |  0.7968 | 0.8055 |
| nn |    0.7908	   |   0.7968 |
| tree | 1.0 |    0.7540|
|forest|    0.9087           |   0.8302     |