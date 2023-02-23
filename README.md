Class Parameters
n_estimators — the number of trees that are being built as part of the boosting.

lr is the Learning Rate, the coefficient by which the predictions of each new tree in the algorithm are multiplied (each tree learns to predict the lambda value, but it is not a fact that adding such a value to the current predictions will give an optimum, so the whole “path” of optimization is divided into small steps).

subsample — the proportion of objects from the sample on which each tree is trained (the proportion is the same for all trees, but the subsample itself is generated separately at each step).

colsample_bytree — the proportion of features from the sample on which each tree is trained (the proportion is the same for all trees, but the subsample itself is generated separately at each step).

The combination of the above two parameters makes it possible to implement the method of random subspaces. To apply trees (to obtain a prediction), you need to store indexes of the used features (but not objects).

max_depth and min_samples_leaf are the parameters of the DecisionTreeRegressor responsible for the depth of the tree construction and the minimum number in the terminal (final) leaves of the tree, respectively. 

Methods of the class
_get_data, _prepare_data, _scale_features_in_query_groups, _ndcg_k are already familiar to you — you can transfer their implementation from the last homework with the only difference that for the convenience of slices by the ys_train and ys_test dimension indexes should be N*1, where N is the number of objects (without this, the grader will report an error).

save_model and load_model are the methods responsible for saving and loading the model.  Save and upload made via the pickle module. 