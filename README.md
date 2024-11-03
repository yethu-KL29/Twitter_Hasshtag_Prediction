# Weather Forecast Tweet Analysis and Prediction

## Project Overview
In this project, we will create a Machine Learning model that analyzes tweets about the weather forecast and predicts all associated hashtags. The model will take tweets as input and categorize each word into three groups: “Sentiments,” “When,” and “Kind.”

### Categories:
1. **Sentiments**: Describes how people feel about the weather (e.g., happy, sad, neutral).
2. **When**: Describes the timing of the weather (e.g., past, present, future).
3. **Kind**: Describes the weather conditions (e.g., stormy, thunder, lightning).

#### Example:
If someone tweets, “Yesterday’s stormy weather was extremely frightening,” the model categorizes the words as follows:
- **Sentiments**: "extremely frightening" (How does the person feel about the weather?)
- **When**: "Yesterday" (When did it happen?)
- **Kind**: "stormy" (What kind of weather was there?)

Note: We can choose only one value from the “Sentiments” and “When” categories but are allowed multiple choices for the “Kind” category.

## Model Architecture
This project utilizes a Many-to-Many Encoder-Decoder Sequence Model. The sequence model accepts a stream of sentences as input and outputs another stream of sentences. The two main techniques used in sequence modeling are the encoder and decoder along with the neural network layer. We will be using the LSTM neural network along with Encoder and Decoder.

### Encoder Model
The encoder model takes the input sequence of tweets and passes it through three stacked layers of the LSTM network. After processing, it returns the hidden states (output of the previous layer) and cell states (stored values), which are passed to the next layers. The final output from the encoder model serves as the input for the decoder model.

### Decoder Model
The decoder model predicts the output sequence using one LSTM layer and an attention mechanism. The attention mechanism helps the model focus on specific words for the prediction.

## Requirements
- Python 3.x
- TensorFlow
- Keras
- NumPy
- Pandas

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/weather-tweet-analysis.git
