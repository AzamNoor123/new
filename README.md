Character-Level Text Generation

This project trains a Recurrent Neural Network (RNN) with LSTM cells to generate text character by character.
It takes in raw text, learns the vocabulary of characters, and generates new sequences that mimic the style of the training data.
Features

Preprocesses text into integer-encoded characters.

Builds a vocabulary (char2idx and idx2char) for mapping characters ↔ integers.

Trains a TensorFlow/Keras model on the dataset.

Supports temperature-controlled sampling for text generation.

Can generate text starting from a given seed string.
Installation
git clone <this-repo-url>
cd <repo>
pip install -r requirements.txt


Requirements:

Python 3.8+

TensorFlow 2.x

NumPy

📊 Training

Put your dataset (plain text file, e.g. shakespeare.txt) inside the data/ folder.

Run training:

python train.py --data data/shakespeare.txt --epochs 20


Checkpoints will be saved in the model/ directory.
Text Generation

After training, you can generate text with:

python generate.py --start "The " --num_generate 500 --temperature 0.8


--start: Seed text to begin generation.

--num_generate: Number of characters to generate.

--temperature: Controls randomness:

Low (0.2) → more predictable & repetitive.

High (1.2) → more creative & random.
