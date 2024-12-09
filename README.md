# NLP Model Accuracy Enhancement

This project aims to improve the accuracy of NLP models by testing various datasets and experimenting with different configurations. The original methodology comes from a research paper on https://github.com/nlpdata/dream , and my contribution focuses on testing it with new datasets.

## Dataset Download Instructions

This project uses the following datasets. Due to their large size, they are not included in this repository. Please follow the instructions below to download the datasets:

### 1. **Numberbatch Embeddings (numberbatch-en-17.06.txt.gz)**

- **Description**: Numberbatch is a large-scale word embedding dataset.
- **Download from**: [Zenodo - Numberbatch-en-17.06](https://zenodo.org/record/3243701/files/numberbatch-en-17.06.txt.gz)
- **After downloading**, place the file in the `data/` folder of this repository.

### 2. **Natural Questions Dataset**

- **Description**: Natural Questions (NQ) is a large-scale question answering dataset by Google.
- **Download from**: [Google Research - Natural Questions](https://ai.google.com/research/NaturalQuestions/download)
- **After downloading**, extract the files and place the relevant JSONL files in the `dsw++/data/` folder of this repository.

## How to Run

1. **Clone this repository**:
    ```bash
    git clone https://github.com/darsshil22/nlp-model-accuracy-enhancement.git
    cd nlp-model-accuracy-enhancement
    ```

2. **Download the datasets**:
    - Follow the links above to download the datasets and place them in the appropriate directories.

3. **Reproduce the results**:
    - Follow the instructions in the original repository to reproduce the results using the `numberbatch-en-17.06.txt.gz` dataset.

4. **Testing with the Natural Questions Dataset**:
    - Replace the numberbatch-en-17.06.txt.gz with files from the Natural Questions dataset and run the model again to evaluate its performance.

## Project Structure

- `evaluate.py`: This script evaluates the model's accuracy by comparing the predicted answers with the actual ones.
- `run.py`: This script runs the core implementation of the model. It loads the dataset, processes it, and performs calculations such as tokenization, vectorization, and prediction.
- `data/`: This directory contains the `train.json`, `dev.json`, and `test.json` datasets.

## Methodology

1. **Replicating Original Research**: Initially, the repository was cloned and the results were replicated using the **Numberbatch** embeddings. 
2. **Contribution**: For the contribution, the **Natural Questions dataset** was tested, and the model's performance was compared between the two datasets.

## Results

### Numberbatch Embedding
- Accuracy on `data/train.json`: 0.494
- Accuracy on `data/dev.json`: 0.512

### Natural Questions Dataset
- Accuracy on `data/train.json`: 0.461
- Accuracy on `data/dev.json`: 0.467

The results show that the model performs slightly better with the **Numberbatch** dataset compared to the **Natural Questions** dataset. This indicates that the Numberbatch embeddings might be better suited for the task or data structure used in this model.

## Contribution

- **Dataset Testing**: The main contribution was introducing the **Natural Questions** dataset to the existing methodology and evaluating its impact on the model's performance.
- **Performance Comparison**: Results demonstrated that the **Natural Questions** dataset led to slightly lower accuracy, suggesting the need for further tuning or fine-tuning of embeddings for better performance.

## Future Work

- **Hyperparameter Tuning**: Further experiments with hyperparameters like learning rate, batch size, and epochs can help improve the model's performance on the **Natural Questions** dataset.
- **Fine-Tuning Embeddings**: Fine-tuning embeddings specifically for the **Natural Questions** dataset could potentially improve accuracy and model generalization.

## Conclusion
This project demonstrated how different word embeddings (Numberbatch vs. Natural Questions) affect the performance of an NLP model. While the Numberbatch embeddings performed better, there is potential for improvement by fine-tuning or experimenting with additional models.
