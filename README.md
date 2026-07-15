# byte-pair-encoding-implementation
# Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch

A Python implementation of the **Byte-Pair Encoding (BPE)** algorithm built completely from scratch without using any external NLP libraries. This project demonstrates how modern tokenizers learn subword vocabularies by repeatedly merging the most frequent adjacent symbol pairs.

---

## 📌 Project Overview

Byte-Pair Encoding (BPE) is a subword tokenization algorithm widely used in Natural Language Processing (NLP) models such as GPT, RoBERTa, and other Transformer-based architectures.

This project implements the complete BPE workflow including:

- Reading a text corpus
- Building the initial vocabulary
- Finding adjacent symbol pairs
- Learning merge rules
- Building the final vocabulary
- Encoding new words
- Decoding tokens back into words

---

## 🚀 Features

- Read and preprocess text corpus
- Character-level tokenization
- Word frequency counting
- Adjacent symbol pair frequency calculation
- Most frequent pair selection
- Pair merging
- Learned merge rules
- Final vocabulary generation
- Encode function
- Decode function
- Simple and easy-to-understand implementation

---

## 🛠 Technologies Used

- Python 3.x
- collections.defaultdict

No external libraries are required.

---

## 📂 Project Structure

```
BPE-Tokenizer/
│
├── bpe_tokenizer.py
├── README.md
└── corpus.txt (Optional)
```

---

## ⚙️ Algorithm Workflow

```
Start
   │
   ▼
Read Corpus
   │
   ▼
Preprocess Text
   │
   ▼
Split Words into Characters + </w>
   │
   ▼
Count Word Frequencies
   │
   ▼
Find Adjacent Symbol Pairs
   │
   ▼
Count Pair Frequencies
   │
   ▼
Select Most Frequent Pair
   │
   ▼
Merge Pair
   │
   ▼
Update Vocabulary
   │
   ▼
Repeat Until Desired Merges
   │
   ▼
Store Merge Rules
   │
   ▼
Build Final Vocabulary
   │
   ▼
Encode New Words
   │
   ▼
Decode Tokens
   │
   ▼
End
```

---

## 📖 Example Corpus

```
low
lower
lowest
new
newer
widest
```

---

## ▶️ How to Run

Clone the repository

```bash
git clone https://github.com/yourusername/BPE-Tokenizer.git
```

Move into the project directory

```bash
cd BPE-Tokenizer
```

Run the program

```bash
python bpe_tokenizer.py
```

---

## 📸 Sample Output

```
Corpus
['low', 'lower', 'lowest', 'new', 'newer', 'widest']

Merge 1: ('l', 'o')
Merge 2: ('lo', 'w')
Merge 3: ('n', 'e')

...

Merge Rules

('l', 'o')
('lo', 'w')

Final Vocabulary

['</w>', 'low', 'lower', 'lowest', 'new', 'newer', 'widest']

Vocabulary Size : 7

Test Word : lowest

Encoded : ['lowest', '</w>']

Decoded : lowest
```

---

## 📚 Learning Outcomes

After completing this project, you will understand:

- What Byte-Pair Encoding (BPE) is
- Why subword tokenization is important
- How GPT-style tokenizers work
- Vocabulary construction
- Merge rule learning
- Token encoding and decoding

---

## 🎯 Applications

- Natural Language Processing
- Large Language Models (LLMs)
- Machine Translation
- Text Classification
- Text Generation
- Chatbots
- Language Modeling

---

## 📈 Future Improvements

- Support larger datasets
- Save learned vocabulary
- Save merge rules to file
- Token ID generation
- Unknown token handling
- Command-line interface
- Performance optimization using NumPy

---

## 👩‍💻 Author

**Sandhiya R**

B.Sc. Computer Science with Artificial Intelligence

---

## 📄 License

This project is developed for educational and learning purposes.
