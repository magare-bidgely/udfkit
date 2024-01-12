# The first few thoughts that inspires this project
### Abstract
Essentially there is a lot of custom UDF development which annotates
a vast majority of the data science algorithm which mars the data science
world. A lack of standardization for these often lead to slower and 
incomplete testing cycle and also no actual sanity test. If there were
sufficient groud truth and the tagged output, then having a framework
which is similar to scikit-learn's cross validation framework, then this
be automated as well as all downstream applications should work out of
the box.

Today the scikit-learn's cross validation looks like the following
```python
from sklearn import preprocessing
# split the data into training and testing dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=0)
# fit the training data
scaler = preprocessing.StandardScaler().fit(X_train)
X_train_transformed = scaler.transform(X_train)
# or the following could have been `fit_transform`
clf = svm.SVC(C=1).fit(X_train_transformed, y_train)
X_test_transformed = scaler.transform(X_test)
# scoring mechanism to determine the efficacy of the parameters
clf.score(X_test_transformed, y_test)
```

### Few other considerations
- we could also use `n_permutation` if required
- 