# Machine Learning for Natural Language Processing

./data contains three CONLL files (dev, train and test) to execute the evaluations on. 
./model contains the word embeddings model used.

Additionally, ./code contains the following Jupyter Notebooks and python scripts. For each notebook and script is shortly elaborated on the content and certain particularities. 

0. R_packages.py
This file consists of all packages used for this module. Also, the paths to the used files are defined so when the location of the files differentiates it only needs to be altered once. This file is used as input for every notebook created and can be used as a list of requirements to run the following notebooks and scripts. 

1. R_analyze_distribution.py
This script consists of functions to analyze the distribution of the conll2003.train.conll and conll2003.dev.conll data.

1.1 R_analyze_distribution.ipynb 
This notebook uses the code of R_analyze_distribution.py to analyze the distribution of the conll2003.train.conll and conll2003.dev.conll data. 

2. R_feature_extraction.ipynb
This notebook creates two additional files upon the conll2003.<>.conll files, where <> is dev, train or test. One named conll2003.<>_with_additional_features.conll and the other named conll2003.<>_with_advanced_features.conll. The first (with_additional_features) includes the new implemented features 'token_length', 'token_frequency', 'is_alpha', 'is_lower', 'is_upper' and 'is_digit. The other (with_advanced_features) includes the features of the additional_features and 'preceding_token', 'preceding_pos-tag', 'preceding_chunk-tag' and 'capitalization'. 

3. R_basic_evaluation.py
3.1 R_basic_evaluation.ipynb 
This notebook uses the code of R_basic_evaluation.py to run 

4. R_basic_system.ipynb
This script consists of functions to train the logistic regression model, naive bayes and support vector machines with one-hot representations on the different sets of selected features. 
4.1 R_basic_system.py
All code from R_basic_system.ipynb is collected in this python file for re-use of other notebooks.

5. R_evaluation_dev_LG_NB_SVM.ipynb
This notebook uses the code from R_basic_evaluation and R_basic_system to run and evaluate the Logisitc Regression, Naive Bayes and Support Vector Machine models using the dev data. Each method is evaluated using three settings (simple, additional and advanced) which are explained in section 2. For each evaluation the classic classification report is created and the self-generated classification report and confusion matrix are formed by using code from R_basic_evaluation.py. 

6. R_evaluation_test_LG_NB_SVM.ipynb
This notebook uses the code from R_basic_evaluation and R_basic_system to run and evaluate the Logisitc Regression, Naive Bayes and Support Vector Machine models using the test data. Each method is evaluated using three settings (simple, additional and advanced) which are explained in section 2. For each evaluation the classic classification report is created and the self-generated classification report and confusion matrix are formed by using code from R_basic_evaluation.py. 

7. R_evaluation_dev_LSTM.ipynb
This notebook uses the code from the original lstm_ner.ipynb notebook to run and evaluate the LSTM model using the dev data. Each method is evaluated using the simple settings which are explained in section 2. The evaluation is performed by creating a classification report and confusion matrix.

8. R_evaluation_test_LSTM.ipynb
This notebook uses the code from the original lstm_ner.ipynb notebook to run and evaluate the LSTM model using the test data. Each method is evaluated using the simple settings which are explained in section 2. The evaluation is performed by creating a classification report and confusion matrix.

9. R_word_embeddings.ipynb
This notebook integrates the option of using word embeddings to the system. The script provided as part of assignment2/ included a function that obtains the feature representations, which is used in this notebook. The Google word embeddings are used, which can be obtained here: https://code.google.com/archive/p/word2vec/

10. R_SVM_hyper-parameter_tuning.ipynb
This notebook tunes the hyper-parameters for the SVM. 

11. R_feature_ablation_analysis.py
This script consists of functions to run the feature ablation analysis in the next two mentioned notebooks.
11.1 R_feature_ablation_analysis_individual.ipynb
11.2 R_feature_ablation_analysis_combined.ipynb

12. R_error_analysis.py
This script consists of functions to run the error analysis in the next mentioned notebook.
12.1 R_error_analysis.ipynb


Order to run the evaluations: 
1. R_feature_extraction.ipynb
2. R_evaluation_dev_LR_NB_SVM.ipynb (or test)
2. R_evaluation_dev_LSTM.ipynb (or test)

