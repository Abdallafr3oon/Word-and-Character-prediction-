# Word and Character Prediction Models

This project includes two models designed for predicting text:
1. A **Word Prediction Model** for generating the next word in a sequence.
2. A **Character Prediction Model** for predicting the next character based on the input sequence.

Both models leverage natural language processing (NLP) techniques and are trained on a dataset derived from Wikipedia.

---

## Word Prediction Model

### Dataset
- The dataset consists of 4 pages from Wikipedia.
- Preprocessing steps:
  - Removal of HTML tags, URLs, punctuation, white spaces, and digits.
  - Application of lemmatization and tokenization to transform text into sequences of words.

### Model Architecture
- An embedding layer followed by 4 Simple RNN layers, each with 50 neurons.
- The final layer is a softmax layer with units equal to the total number of words in the dataset.

### Accuracy
- Achieves nearly **90% accuracy**, demonstrating exceptional ability to predict the next word in a sequence.

### Conclusion
The word prediction model effectively learns patterns and dependencies within input sequences, providing highly accurate predictions.

---

## Character Prediction Model

### Dataset
- The dataset consists of 4 pages from Wikipedia.
- Preprocessing steps:
  - Removal of HTML tags, URLs, punctuation, white spaces, and digits.
  - Tokenization at the character level.

### Model Architectures
1. **Model 1 (LSTM)**:
   - 2 LSTM layers: 
     - 256 neurons in the first layer.
     - 128 neurons in the second layer.
   - A softmax output layer with units equal to the number of unique characters in the dataset.
   - **Result**: The model performs well and generates coherent text outputs.

2. **Model 2 (Simple RNN)**:
   - 3 Simple RNN layers:
     - 256 neurons in the first layer.
     - 128 neurons in the second layer.
     - 64 neurons in the third layer.
   - A softmax output layer with units equal to the number of unique characters in the dataset.
   - **Result**: Performs reasonably well, but requires more data and architectural improvements for better accuracy.

### Conclusion
- The LSTM-based architecture achieves better results compared to the Simple RNN architecture.
- More data and a more powerful architecture are recommended for improved performance.

---

## Features
- **Word Prediction**: Predicts the next word based on context.
- **Character Prediction**: Predicts the next character in a sequence.
- **Comparative Analysis**: Highlights the performance differences between LSTM and Simple RNN models for character prediction.

---

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Abdallafr3oon/Word-and-Character-prediction-.git
