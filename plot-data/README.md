The following data underlies the plots in the paper:
# Figure 1
File `hamming_statistics.csv`
- *random_state*: random state describing the sampled dataset.
- *num_features*: number of features in the experiment.
- *h*: hamming distance.
- *eig_var*: variance of the eigenvalues of the experiment kernel matrix.
- *eig_var_scaled*: variance of the eigenvalues of the scaled to [0, 1] kernel matrix.
- *eig_pos_sum*: sum of the positive eigenvalues.
- *eig_neg_sum*: sum of the negative eigenvalues.
- *eig_pos_sum_scaled*: sum of the positive eigenvalues of the scaled kernel.
- *eig_neg_sum_scaled*: sum of the negative eigenvalues of the scaled kernel.
- *train_score*: training score of the problem
- *train_score_scaled*: training score of the problem obtained on the scaled kernel. 
- *loss_value*: kernel alignment loss value.
- *loss_value_scaled*: kernel alignment loss value on the scaled kernel.
- *distance_to_psd*: inner product between kernel matrix and closest PSD matrix as per kernel alignment definition.
- *distance_to_scaled_psd*: same but for scaled kernel.
- *m1*: norm of the difference between kernel and closest PSD scaled by the norm of kernel.
- *m2*: ratio of the trace of closest PSD and trace of kernel.
- *m3*: ratio of the sum of the negative eigenvalues and the sum of the positive eigenvalues.
- *m4*: ratio of the sum of the negative eigenvalues and the sum of all eigenvalues.
- *m5*: norm of the difference between normalized kernel and normalized closest PSD.

File `hamming_diagonal.csv` is derived from `hamming_statistics.csv`
- *num_features*: the number of features.
- *h*: hamming distance.
- *diagonal*: diagonal values of the kernel.

# Figure 2
File `paper_run_100_problems.csv`, only following columns are used:
- *sqrt_n*: square root of the number of train samples.
- *gcq*: $g_{CQ}$ value.

# Figure 3
File `train_data.csv`
- *iteration*: - iteration number in a QKA experiment.
- *loss_value*: - kernel alignment loss values.
- *score_value*: - training score obtained on the iteration.

File `score_data`
- *score_type*: a textual representation of the type of the score, describes when this score was obtained. 
- *score_value*: score on a particular configration of the problem.

File `pqk_paper_run_100_problems.csv`, only following columns are used:
- *qsvc_zz_featuremap_train*: training score obtained on `ZZFeatureMap` 
- *qsvc_zz_featuremap_test*: test score obtained on `ZZFeatureMap`

# Figure 4
File `qka_hw_scores.csv`
- *score_type*: type of score: untrained model, trained model, classical model, training score, test score.
- *score_value*: value of the score.

File `qka_hw_train.csv`
- *iteration*: kernel alignment iteration.
- *loss_value*: loss value on the iteration.
- *score_value*: training score on the iteration.

Files `qka_hw_scores_nh.csv` and `qka_hw_train_nh.csv` have the same columns as above, but obtained without bit-flip tolerance enabled. 

# Figure 5
The figure 5 is plotted using data from files `hamming_hw_248429624.csv` and `hamming_hw_495812423.csv`, 40 and 60 qubit experiments.
The structure of the files are the same:
- *h*: hamming distance
- *train_score*: training score for a particular hamming distance
- *test_score*: test score for a particular hamming distance

# Figure 6
The figure 6 is plotted using a numpy array stored in `kernel_example.npy`.
