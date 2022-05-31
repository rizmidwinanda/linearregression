# linearregression
This is code to predict housing price in boston using linear regression

# Data boston.csv Explanation
- Criminal rate (crim)
- Residential land zoned proportion (zn)
- Non-retail business acres proportion (indus)
- Is bounds with river (chas)
- Nitrogen oxides concentration (nox)
- Number rooms average (rm)
- Owner age proportion (age)
- Weighted distance to cities (dis)
- Accessibility index (rad)
- Tax rate (tax)
- Pupil-teacher ratio (ptratio)
- Black proportion (black)
- Percent lower status (lstat)
- Housing price (medv)


# Flow
1. Split the data for train, validate, and test
2. medv or housing price is a target and the rest of data will be a variable/feature
3. Make a correlation heatmap to identify which feature that highly correlated each other
4. Highly correlated feature will be dropped (tax and rad)
5. Train the data using LASSO and Ridge method
6. Ridge result: medv = 22.41 - 0.07 crim + 0.027 zn - 0.0008 indus + 3.28 chas - 17.31 + .....
7. LASSO result: medv = 26.08 + 0.008 zn + 0.0004 age + 0.015 black - 0.69 lstat
8. Evaluate the trained data using RMSE, MAE, and MAPE
9. The results are the prediction has deviation that not really far from the real value
