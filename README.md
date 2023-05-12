# Feature Selection README

## Description

This C++ program is designed to perform feature selection using Forward Selection and Backward Elimination algorithms. It takes a dataset file as input and outputs the best feature subset based on the Leave-One-Out Cross Validation (LOOCV) accuracy.

## Compilation

To compile the program, run the following command:

```
g++ -o feature_selection main.cpp
```

## Usage

To run the program, use the following command:

```
./feature_selection
```

The program will prompt you to enter the name of the file containing the dataset and the algorithm you want to run (Forward Selection or Backward Elimination).

## Input File Format

The input file should be a plain text file containing the dataset. Each line of the file represents a single instance, with the class attribute as the first value and the feature attributes following it. Values should be separated by spaces.

Example input file format:

```
1 2.2 3.1 1.5
0 3.3 2.1 0.9
1 1.1 3.3 2.8
...
```

## Output

The program will output the best feature subset and its accuracy based on the LOOCV evaluation. Additionally, it will display the total time taken for the feature search.

## Functions

- `printFeatures(vector<int> currFeatures)`: Outputs the current feature set.
- `leave_one_out_cross_validation(vector<vector<float>> data, vector<int> currFeatures, int feature, int choice)`: Performs the LOOCV evaluation and returns the accuracy.
- `feature_search(vector<vector<float>> data, int choice)`: Performs the feature search using the specified algorithm (Forward Selection or Backward Elimination) and outputs the best feature subset and its accuracy.
