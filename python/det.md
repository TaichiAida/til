# det, slogdet
in a hyperparameter tuning of the Gaussian Process Regression, an error is occurred.

```
def loglik(params, X_train, y_train, kernel, kgrad):
	K = kernel_matrix(X_train, kernel)
	K_inv = inv(K)
	return log(det(K)) + y_train.T @ K_inv @ y_train

> overflow encountered in det
```

This error is occurred when det(K) is too large/small.  
To avoid this error, replace `np.log(np.linalg.det())` with `np.linalg.slogdet()`

```
def loglik(params, X_train, y_train, kernel, kgrad):
	K = kernel_matrix(X_train, kernel)
	K_inv = inv(K)
	return slogdet(K)[1] + y_train.T @ K_inv @ y_train

# slogdet() returns (sign, logdet)
```

reference: [numpy document](https://numpy.org/doc/stable/reference/generated/numpy.linalg.slogdet.html)
