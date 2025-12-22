# SAR recommend system practice

## set up 
- **environment**: python 3.9 (package recommenders does not support python 3.14)
- **Core fix**: Install dependencies manually before the main package to avoid errors:
# SAR recommend system practice

## set up 
- **environment**: python 3.9 (package recommenders does not support python 3.14)
- **Core fix**: Install dependencies manually before the main package to avoid errors:

```bash
# Step 1: Upgrade Package Manager
/Library/Developer/CommandLineTools/usr/bin/python3 -m pip install --upgrade pip

# Step 2: Install Build Dependencies (Required for scikit-surprise)
python3.9 -m pip install --user numpy Cython setuptools

# Step 3: Install Main Library
/Users/newt/Library/Python/3.9/bin/pip3 install recommenders
```
### note for variables 
* **timestamp**: To record the time that the action is done by the user. Older actions are considered less important than recent ones (Time Decay), as they may not reflect current interests.

* **Stratified Splitting**: A method to split data based on userID. It ensures that every user in the Test set is also present in the Train set, so the model has a profile to learn from before being tested.

* **Total Ratings**: The total number of user-item interaction records in the dataset.

* **Unique Items**: The total number of distinct movies. The count may vary between sets because some movies might not be sampled into the Test set.