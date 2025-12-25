# ALS

## current progress: code 7

## set up 
* must donwnload pyspark first(careful with the version, might have conflict with java)
    ```%pip install pyspark==3.5.0```
### note for variables 
* **Explicit Feedback**:
    *   Refers to direct ratings given by users (e.g., 1-5 stars). The model uses these exact scores for training.

* **Implicit Feedback**:
    *   Refers to indirect user behavior (e.g., clicks, watch history, purchase records) rather than direct ratings.

* **`implicitPrefs=False`**:
    *   **False**: Tells the model to use **Explicit Feedback** data (predicting actual ratings).
    *   **True**: Tells the model to use **Implicit Feedback** data (predicting confidence/preference strength).
    *   *Note*: Since we are using MovieLens ratings (1-5 stars), we set this to `False`.

* **Non-negative (`nonnegative=False`)**:
    *   **True**: Constrains latent factors to be non-negative numbers.
    *   **False**: Allows latent factors to be negative numbers.
    *   **Why False?**: Setting this to `False` allows the model to capture **negative preferences** or "dislike". For example, a very low rating (like 1 star) represents a strong negative sentiment, which is better represented by negative values in the latent space rather than just low positive values.

### sar variables 

## conclusion