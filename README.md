English → Kannada Neural Machine Translation

This project implements an English-to-Kannada Neural Machine Translation (NMT) system using a Sequence-to-Sequence (Seq2Seq) Encoder–Decoder architecture with Attention. The model learns cross-lingual mappings from parallel corpora to generate fluent and context-aware Kannada translations from English input sentences.

Dataset
The model is trained on a parallel English–Kannada corpus, where each English sentence is aligned with its corresponding Kannada translation.

Dataset Processing Steps:
Text normalization (lowercasing, punctuation cleaning),
Tokenization of English and Kannada text,
Vocabulary creation for both source and target languages,
Conversion of text to integer sequences,
Padding sequences to fixed length,
Train–validation split for performance evaluation,
The preprocessing ensures proper handling of linguistic differences between English (SVO structure) and Kannada (SOV structure).

Model Architecture
The system uses a Seq2Seq architecture with Attention, consisting of:
1. Encoder
Embedding layer to convert tokens into dense vectors
LSTM/GRU layers to encode the input English sentence into a context vector
Captures semantic representation of the source sequence
 2. Attention Mechanism
Computes alignment scores between encoder outputs and decoder states
Assigns dynamic weights to relevant input tokens
Improves translation quality for long sentences
 3. Decoder
Embedding layer for target tokens
LSTM/GRU layers to generate Kannada output sequentially
Softmax output layer to predict next word probabilities

Tech Stack:
Python
TensorFlow / PyTorch
NumPy
NLP Preprocessing
Seq2Seq + Attention Mechanism
