
# Figure 7a

Derived directly from raw files [/synthetic-data-raw/](/synthetic-data-raw)full_nonsplit_synthetic_dataset_2d_circle_subspaces_utility_exp.csv.

# Figure 7b

File `spsa_loss_10_iters.pickle`.

# Figure 7c

- Quantum: elaboration of `final_train_set_kernel_matrix_dict.pickle`, by setting different thresholds for the BFT.
- Classical: from `kernelafterclassical.pickle` (no processing).

Files:
- `final_train_set_kernel_matrix_dict.pickle` It contains a list of 900 records, each being an entry in the matrix. For a given item of the list, the first component is the coordinates in the matrix (say, `data[65][0]` is (2,5)), and the second component (`[data[65][1]`) is a dict matching sampled bistrings with their count.


# Figure 7d

The plot can be computed as
```
train_labels = [0]*11 + [1]*9 + [2]*10

svc = SVC(kernel='precomputed')
svc.fit(kmatrix_train, train_labels)
train_score = svc.score(kmatrix_train, train_labels)
test_score = svc.score(kmatrix_test, test_labels)
```
where test labels are taken from `y_test_3_class_adhoc_2d_100d_good3.npy` and kernel matrices are elaborated from `final_train_set_kernel_matrix_dict.pickle` and `final_train_set_kernel_matrix_dict.pickle`.

Files:
- `final_train_set_kernel_matrix_dict.pickle` See Fig 7c.
- `final_test_set_kernel_matrix_dict.pickle` Same as above, with test data.

# Figure 8
Files `156qubit_classicalkernel_5iter_kernel_2d_no_noise.pickle` and `156qubit_spsa_0_kernel_2d_no_noise_32BFT.pickle`.
