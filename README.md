# AutoCurrect-DS
# 🔤 Autocorrect Web App

This project is a simple web-based autocorrector built using Python, Flask, and a basic NLP approach. It suggests the most probable and similar corrections for a misspelled word using **Jaccard Similarity** and **word probabilities** calculated from a given text corpus.

## 📂 Project Structure

```
AUTOCORRECTER/
│
├── templates/
│   └── index.html           # HTML front-end interface
│
├── app.py                   # Flask backend server
├── autocorrect book.txt     # Text corpus used for word frequency
└── README.md                # Project documentation (this file)
```

## 🚀 Features

* Accepts a word input from the user
* Uses Jaccard similarity to suggest closest matching words
* Ranks suggestions based on similarity and frequency in the corpus
* Simple web UI using HTML and Flask templating

---

## ⚙️ How It Works

1. **Text Preprocessing**:

   * Reads the `autocorrect book.txt` file.
   * Converts text to lowercase.
   * Extracts words using regular expressions (⚠️ currently there is a small bug; see "Bugs" section).

2. **Word Frequency**:

   * Uses `collections.Counter` to calculate the frequency of each word.
   * Computes probabilities based on total word count.

3. **Suggestion Logic**:

   * For the input word, calculates Jaccard similarity with every word in the corpus.
   * Combines the similarity and probability to sort suggestions.

---

## 🧪 How to Run

1. **Install dependencies**:

   ```bash
   pip install flask pandas textdistance
   ```

2. **Run the app**:

   ```bash
   python app.py
   ```

3. **Open in browser**:
   Visit `http://127.0.0.1:5000/` to access the web interface.

---


## 💡 Future Improvements

* Add fuzzy matching using edit distance or Levenshtein
* Display top N results instead of all
* Highlight corrections in real-time using JavaScript
* Support sentence correction

---

## 📜 License

This project is open-source and free to use under the MIT License.




