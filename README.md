# GAPE Programming Assignment – Word Embeddings

## Domain
Agriculture (Crop Farming)

## Framework
Keras (TensorFlow backend)

---

## Corpus
- Single paragraph about agriculture practices:
  - Crop planning and seed selection
  - Soil moisture, rainfall, and pest resistance
  - Field preparation and irrigation
  - Harvest timing, market price, and storage
- Text is preprocessed (lowercase, punctuation removed, tokenized).

---

## Vocabulary
- Unique words are assigned IDs and frequency.
- Saved in `vocab.txt`.

---

## Models
1. **CBOW (Continuous Bag of Words)**
   - Input: Context words (window size 4)
   - Output: Target word
2. **Skip-gram**
   - Input: Target word
   - Output: Context words
- Both models use **one-hot encoding**.
- No pretrained embeddings used.

---

## Parameters
- Embedding dimension = 10  
- Context window = 4  
- Epochs = 50  
- Learning rate = 0.05  

---

## Files
- `corpus.txt` – Original text  
- `vocab.txt` – Word IDs and frequency  
- `cbow_dataset.csv` – CBOW training data  
- `skipgram_dataset.csv` – Skip-gram training data  
- `embeddings_cbow_0_1.csv` – CBOW embeddings (0-1)  
- `embeddings_skipgram_0_1.csv` – Skip-gram embeddings (0-1)  
- `loss_cbow.txt` – CBOW loss per epoch  
- `loss_skipgram.txt` – Skip-gram loss per epoch  
- `README.md` – Project description  

---

## Usage
1. Run the scripts in Google Colab or Python environment with TensorFlow/Keras.  
2. The scripts will preprocess the text, generate datasets, train CBOW and Skip-gram models, and save embeddings scaled to 0-1.  
3. Embeddings can be used for similarity analysis or nearest-neighbor queries.

---

## Output
- 10-dimensional embeddings for each word.  
- Loss per epoch saved in text files.  
- Example embedding (range 0-1):  
''



