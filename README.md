n this project, we will create a Machine Learning model that will analyze tweets about the weather forecast and then predict all of the hashtags associated with those tweets. The model will take tweets as input and separate each word of those tweets into three groups, namely “Sentiments”, “When,” and “Kind.”

The “Sentiment” category describes how people feel about the weather, whether they are happy, sad, or neutral. Weather timing is described in the “When” category, which includes the past, present, and future. The weather conditions like ‘stormy’, ‘thunder’, ‘lightning’ are described in the “Kind” category.

For example, if someone tweets “Yesterday’s stormy weather was extremely frightening.” So for “Sentiments”, we will say “how does the person feel about the weather?” So the answer is “extremely frightening”, for “When” we will say “when did it happen?” the answer is “Yesterday” now for “Kind” we will say “what kind of weather was there?” so the answer is “stormy”. We can choose only one value from the “Sentiment” and “When” categories but are allowed multiple choices for the “kind”.

For this, we are going to use the Many to Many Encoder-Decoder Sequence Model.

This Sequence model accepts a stream of sentences as input and outputs another stream of sentences. The two main techniques used in sequence modeling are encoder and decoder along with the neural network Layer. We will be using the LSTM neural network along with Encoder and Decoder.

The encoder model takes the input sequence of tweets and passes it to 3 stacked Layers of the LSTM network which after processing returns the hidden state(output of the previous layer) or cell states (stored value) and passes to the next layers. The final output from the encoder model is the input for the Decoder model which will then predict the output sequence using one LSTM layer and Attention mechanism. The attention mechanism helps the model to focus only on specific words for the prediction
