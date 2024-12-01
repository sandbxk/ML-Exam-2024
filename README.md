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