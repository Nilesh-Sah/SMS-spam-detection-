# SMS-spam-detection-
Detecting spam sms using tensorflow in python

# cell 1
 quick summary of what’s happening
Step	Purpose
drop()	Removes unnecessary columns
rename()	Makes column names meaningful
map()	Converts text labels to numeric values
head()	Previews the cleaned dataset

# cell 6

Key Points:
Set Data Structure: Uses set() which only stores unique elements
Nested Loops:
Outer loop: Iterates through each sentence in the dataframe
Inner loop: Iterates through each word in each sentence

String Splitting: sent.split() breaks sentences into words using whitespace

Automatic Deduplication: The set handles duplicate words automatically


# cell 7
1. Data Preparation
np.asanyarray(): Converts pandas Series to numpy arrays for better performance
X: Contains the text features (independent variables)
y: Contains the encoded labels (dependent variable)

2. DataFrame Creation
Creates a new DataFrame to ensure proper alignment between text and labels
Useful for data validation and debugging

3. Train-Test Split Parameters
test_size=0.2: 20% of data goes to test set, 80% to training set
random_state=42:
Ensures reproducible results
Same split every time code runs
Common practice in machine learning

4. Output Variables
X_train: Text data for model training
X_test: Text data for model evaluation
y_train: Labels for model training
y_test: Labels for model evaluation

5. Shape Output
Returns tuple showing dimensions:

X_train.shape: (number of training samples,)
y_train.shape: (number of training labels,)
X_test.shape: (number of test samples,)
y_test.shape: (number of test labels,)

Example Output:
If original dataset has 1000 samples:
X_train.shape: (800,) - 800 training texts
y_train.shape: (800,) - 800 training labels
X_test.shape: (200,) - 200 test texts
y_test.shape: (200,) - 200 test labels

This split ensures the model is trained on one portion of data and evaluated on unseen data to measure real performance.