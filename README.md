# Enro_NLP_bot
# Context-Aware Conversational Chatbot

A command-line interface (CLI) chatbot that engages in context-aware conversations using NLP techniques. It understands user intent, maintains conversation history, and generates dynamic, relevant responses. Can be adapted to different themes — general Q&A, tutoring, or entertainment.

---

## Demo

> Screenshot or GIF coming soon

---

## Features

- **Natural Language Understanding (NLU)**
  - Tokenization and part-of-speech tagging
  - Named entity recognition
  - Sentiment analysis *(optional)*

- **Context Management**
  - Retains past inputs using a memory structure
  - Uses previous queries to shape new responses

- **Response Generation**
  - Template-based generation
  - Retrieval-based answers from a dataset
  - Optional integration with Hugging Face pretrained models or OpenAI API

- **CLI Interface**
  - Built with Python's `curses` or `cmd` module
  - Optional colored text output for improved UX

---

## Tech Stack

- Python
- NLTK / spaCy
- Hugging Face Transformers *(optional)*
- OpenAI API *(optional)*
- Python `curses` / `cmd` module

---

## Dataset

**Primary:** [Enron Email Corpus](https://www.cs.cmu.edu/~enron/) — a large collection of real-world emails with varied tones, structures, and intents, ideal for training and retrieval-based response generation.

**Supplementary:**
- [Brown Corpus](https://www.nltk.org/book/ch02.html) — additional language modeling
- [Google Ngrams](https://books.google.com/ngrams) — sentence structure variation

> To use the Enron dataset, download it from the link above and place it in the `data/` directory.

---

## Project Structure

```
chatbot/
├── main.py          # Entry point, CLI interface
├── nlu.py           # Tokenization, POS tagging, NER
├── context.py       # Dialogue history and memory management
├── response.py      # Response generation logic
├── data/            # Dataset files (not included, see Dataset section)
├── requirements.txt # Python dependencies
└── README.md
```

---

## Getting Started

### Prerequisites

Make sure you have Python 3.8+ installed.

### Install dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install nltk spacy openai transformers
python -m spacy download en_core_web_sm
```

### Set up environment variables

If using the OpenAI API, create a `.env` file in the root directory:

```
OPENAI_API_KEY=your_api_key_here
```

### Run the chatbot

```bash
python main.py
```

---

## Roadmap

- [ ] Parse and preprocess Enron emails into conversational pairs
- [ ] Design the full pipeline: NLU → context tracking → response generation
- [ ] Build minimal working CLI interface
- [ ] Add optional OpenAI / Hugging Face integration
- [ ] Iterate with user testing to refine response quality
- [ ] Add demo GIF to README

---

## Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m 'Add your feature'`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a pull request

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
