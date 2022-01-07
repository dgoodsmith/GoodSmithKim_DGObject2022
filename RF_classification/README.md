
RF classification

matlab_rf_class_data contains variables: 
* First_pc_coef: coefficient for first principal component of second derivative of the waveform
* cl: classification assigned to testing data using classifier. 0: mossy cells, 1: granule cells
* model: Random forests classification model
* model_features: list of features used for classification.
* training_data: classification features (columns) for 141 cells (rows) recorded in foraging sessions used to train the random forests classifier
* training_class: putative cell types assigned to 141 cells used for training the classifier. 1 indicates putative granule cell (no place fields), 0 indicates putative mossy cell (field in 3 or more environments)
* testing_data: classification features (columns) for 366 cells (rows) analyzed in the present study


RF_MexStandalone-v0.02-precompiled:
matlab implementation of randomForest R package described in Liaw and Wiener, 2002. 
Downloaded from https://code.google.com/archive/p/randomforest-matlab/
