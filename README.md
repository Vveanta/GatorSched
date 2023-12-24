# GatorSched Project

## Overview
GatorSched is an innovative project that leverages the power of GPT-2 small model to process and generate responses to queries related to lifelog data. It aims to extract relevant schedule and historical information from structured lifelog data, offering personalized recommendations and insights.

## Structure
- `source/`: Contains the main scripts and data for running GatorSched.
- `TimelineQA/`: A Git submodule containing the TimelineQA code, with an additional `dataGenCode` folder for data generation.

## Getting Started
To use GatorSched, clone this repository along with the TimelineQA submodule:
```bash
git clone --recurse-submodules git@github.com:Vveanta/GatorSched.git
```


### Directory Contents
- `source/inference.ipynb`: Notebook to generate answers for the provided questions using the trained model.
- `source/myimplementation.ipynb`: Notebook for training and fine-tuning the GPT-2 model on lifelog data.
- `source/questions.txt`: Text file containing sample questions for model testing.
- `source/test_data/`: Folder containing test data used to train the model.

- `TimelineQA/`: Submodule from the TimelineQA project with added `dataGenCode` folder.
    - `dataGenCode/datagenerator.py`: Script for generating various datasets with different verbosity, sparsity, and time duration.

## Usage

### Data Generation
To generate new lifelog data, navigate to the `TimelineQA` submodule and use the `datagenerator.py` script:

```bash
cd TimelineQA/dataGenCode
python datagenerator.py
```

### Model Training and Fine-Tuning
Run the `myimplementation.ipynb` notebook in the `source` folder to train and fine-tune the GPT-2 model on your lifelog data. This notebook processes the data, trains the model, and saves the trained model for inference.

### Generating Responses
After training the model, use the `inference.ipynb` notebook to generate responses for questions listed in `questions.txt`. The notebook outputs the answers in `answers.txt`, forming a question-answer pair for each query.

## Contributions
Feel free to contribute to the GatorSched project by submitting pull requests or opening issues for any bugs or feature requests.

## License
This project is licensed under the [MIT License](LICENSE).

