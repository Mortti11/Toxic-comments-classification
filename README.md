# Toxic Comments Classification

This project aims to automatically identify toxic comments using machine learning. It helps detect harmful content, making online spaces safer.

## How It Works

1. **Data**: We use a dataset with comments labeled as toxic, severe toxic, obscene, threat, insult, and identity hate.
2. **Model**: The model is trained using different algorithms to classify new comments into these categories.
3. **Prediction**: When you input a new comment, the model predicts whether it’s toxic and which type of toxicity it exhibits.

## Getting Started

### Installation

1. Clone this repository.
2. Install required packages: 
   ```bash
   pip install -r requirements.txt
   ```

### Dataset

The dataset is large, so it's not included in this repository. You can download it from Kaggle using the following command:
```bash
kaggle competitions download -c jigsaw-toxic-comment-classification-challenge
```

### CUDA (Optional but Recommended)

For faster training and prediction, it is recommended to use a GPU with CUDA support. Ensure that you have CUDA installed and configured properly if you plan to run the model on a GPU.

### Running the Model

1. Open the Jupyter Notebook `toxic_comments_classification.ipynb`.
2. Run the cells to load data, preprocess it, and train the model.
3. Use the model to classify new comments. For example:
   ```python
   comment = "You are so stupid!"
   prediction = model.predict([comment])
   print(prediction)
   ```
   This would output something like `['toxic', 'insult']`, indicating that the comment is toxic and an insult.

## Example Results

After running the notebook, you’ll see how different models perform in classifying toxic comments. The example below shows predictions on a few sample comments:

- "I love you" → `['non-toxic']`
- "You are a loser" → `['toxic', 'insult']`

## Requirements

- Python 3.x
- Jupyter Notebook
- CUDA (if using a GPU for faster performance)
