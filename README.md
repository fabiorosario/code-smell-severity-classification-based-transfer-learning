# An Approach for Code Smell Detection and Severity Assessment based on Transfer Learning
Code smell detection and severity assessment are important for categorizing and prioritizing software maintenance efforts. In this sense, there is considerable research focusing on Deep Learning and Transformer-based models for code smell detection. This work aims not only to detect but also to make a severity assessment of code smells using a two-stage approach employing Ensembles and Transfer Learning. This work also explores the impact of applying data scaling, feature selection techniques, hyperparameter optimization, and data oversampling to enhance the Ensembles for code smell detection and severity assessment. Moreover, the proposed approach works at the two code smell levels (class and method) and is suitable for both Java and C# datasets. This work reveals that Transfer Learning improved model generalization, with detection accuracy on the C# dataset matching or exceeding that of the Java dataset with minimal performance loss. Experiments indicate that the proposed approach delivers promising results for code smell detection and severity assessment at both class and method levels.

To facilitate the linking of each directory and file in this repository to our work, I describe them below:

1) The "Datasets" directory contains the Java (merged dataset_FE_LM_GC_DC_class balancer.csv) and C# (GeneratedDataset_CSharp.csv) datasets used in our study. The datasets contain severity instances of four code smells (God Class, Data Class, Feature Envy, and Long Method). Each instance is associated with a feature vector of 84 object-oriented software metrics.

2) The files related to feature selection and hyperparameter optimization are contained in the "Feature selection and hyperparameter optimization" directory:

2.1) Feature selection significantly distinguishes between similar functions in design patterns [34]. Initially, we selected the features with the most significant impact in the Java dataset, dividing subsets into 10, 15, 20, 25, and 30% of the original features (see the files "Code Smell Detector_BinaryTarget.ipynb" and "Code Smell Detector_BinaryTarget.ipynb"). To focus on software metrics that play a significant role in distinguishing similar features, we used ANOVA and Chi-square. "Selected feature details of the best Ensemble Methods.xlsx" presents the features that make up the best models for code smell detection and severity assessment.

2.2) After selecting the main features of the Java dataset, we proceeded with optimizing the hyperparameters, using the Randomized Search (RS) and Bayes Search (BS) algorithms to determine the most appropriate settings for each Ensemble Method (Random Forest, Categorical Boosting, and Extreme Gradient Boosting) hyperparameter for code smell detection and severity assessment. 
"Details detectors.xlsx" shows feature selection results, hyperparameter optimization, and ensemble methods for code smell detection. 
"Details severity assessment.xlsx" presents the detailed results of the classifiers used for code smell severity assessment. 
"Best_Optimized Ensemble Methods.xlsx" shows the detailed results of the selected features from the dataset and the optimized hyperparameters for the best ensemble methods for code smell detection and severity assessment. 

2.3) the following files show the python scripts used for hyperparameter optimization of the best ensemble models for code smell severity assessment: "Severity Assessment_CB_anova-30_Bm_mean.ipynb", "Severity Assessment_XGB_anova-30_Bm_mean.ipynb"; "Severity Assessment_CB_chi-norm-20_Bm.ipynb", "Severity Assessment_RF_chi-norm-20_Bm.ipynb", "Severity Assessment_XGB_chi-norm-30_Bb_accuracy.ipynb", "Severity Assessment_CB_anova-25_Bb.ipynb", "CB_chi-original_R_accuracy.ipynb", "RF_chi-original_R_accuracy.ipynb", " XGB_chi-norm-25_Rb_accuracy.ipynb", and " RF_chi-norm-25_Rb_accuracy.ipynb".


