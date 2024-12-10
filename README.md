# ML-Exam-2024
 
To download from Kaggle, you must create a Kaggle API token. This token will then be used in a .env file in the '/Notebooks'  directory. The .env file should contain the following:
```
KAGGLE_USERNAME=your_kaggle_username
KAGGLE_KEY=your_kaggle_key
```


## Libraries
The following libraries are used in this project:
Python Libraries
- pandas: For data manipulation and analysis.
- numpy: For numerical computations.
- Pillow (PIL): For image processing tasks.
- matplotlib: For visualization and plotting.
- glob: For handling file path patterns.
- os: For interacting with the operating system, e.g., file paths and directories.
- tensorflow: For deep learning and TensorFlow-based operations.
- keras: Keras is part of TensorFlow as tensorflow.keras, but including it as a standalone dependency is good practice if you rely on standalone Keras features.
- scikit-learn: For splitting datasets and other machine learning utilities.
- kagglehub: For downloading datasets from Kaggle.
- python-dotenv: For loading environment variables from .env files.
- warnings: Part of the standard library, no need to install.
- System Dependencies
- Python 3.8 or later: Ensure TensorFlow and other dependencies are compatible.
- CUDA/cuDNN (optional): Required if you intend to leverage GPU acceleration for TensorFlow. Match the versions specified by TensorFlow's GPU compatibility matrix.



## Results

| Notebook Model  | Test Accuracy | Test Loss | Change 1                                          | Change 2                         | Other Changes                | Notes                                                                                                                   |
| --------------- | ------------- | --------- | ------------------------------------------------- | -------------------------------- | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Attempt 1       | 49.79%        | 69.37%    | Initial                                           |                                  |                              |                                                                                                                         |
| Attempt 2       | 43.54%        | 69.5%     | Remove ReduceLROnPlateau                          |                                  |                              |                                                                                                                         |
| Attempt 3       | 96.2%         | 13.36%    | Remove Data Augementation                         |                                  |                              |                                                                                                                         |
| Attempt 4       | 97.07%        | 11.39%    | Add "SAME" padding to Conv2D Layers               | Add Dropout Layer with 0.5 value |                              | Was unable to reach extactly 97% when running again                                                                     |
| Attempt 5       | 96.58%        | 12.28%    | Change from single 50% dropout to 4x 10% dropouts |                                  |                              |                                                                                                                         |
| Attempt 6       | 96.73%        | 12.95%    | Change to 4x 20% dropouts                         | Readd ReduceLROnPlateau          |                              |                                                                                                                         |
| Attempt 7       | 96.61%        | 13.03%    | Re-remove ReduceLROnPlateau                       |                                  |                              |                                                                                                                         |
| Attempt 8       | 96.31%        | 12.9%     | Go back to Attempt 4 architecture                 | Use SGD optimizer                |                              | Ran for 26m instead of ~9m                                                                                              |
| Attempt 9       | 96.46%        | 12.33%    | RMSProp with Learning Rate Scheduling             |                                  |                              |                                                                                                                         |
| Attempt 10      | 96.93%        | 12.3%     | Back to Adam optimizer                            | Larger Batch size (64)           |                              |                                                                                                                         |
| Attempt 11      | 96.37%        | 12.95%    | Smaller batch size (16)                           |                                  |                              |                                                                                                                         |
| Attempt 12      | 96.62%        | 12.63%    | Leaning rate reduction to 0.0001                  | Back to default batch size (32)  |                              |                                                                                                                         |
| Bonus attempt   |               |           | Change learning rate back to 0.001                | SGD, Large Batch size            | ML Compulsory 1 architecture | Inspecting if SGD performs better with multiple samller dropouts. Cancelled due visibly bad performance during training |
| Attempt 4 Bonus | 97.03%        | 11.74%    | Use attempt 4 model                               | Add ReduceLROnPlateau            |                              | Done due to visible decrease when disabling ReduceLROnPlateau for other models                                          |