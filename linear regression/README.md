# Linear Regression

Simple linear regression implemented by hand (no sklearn model), in `SMOLLR.ipynb`.
Example data: `placement (1).csv` — 200 rows of `cgpa,package`.

## The model

`SMOLLR` fits `y = mx + b` with the closed-form least-squares solution:

```
m = Σ(x - x̄)(y - ȳ) / Σ(x - x̄)²
b = ȳ - m·x̄
```

`fit(x_train, y_train)` computes `m` and `b` with a loop, `predict(x_test)` returns `m·x_test + b`.

The notebook loads the CSV, splits it 80/20 with `train_test_split`, fits on the training
half, and predicts the test half.

## Running it

```
pip install numpy pandas scikit-learn jupyter
jupyter notebook SMOLLR.ipynb
```

The CSV path at the top of the notebook is absolute and points to another machine; point it
at `placement (1).csv` before running.
