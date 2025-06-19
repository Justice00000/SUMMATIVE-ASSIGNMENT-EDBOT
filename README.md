# EdBot – My Educational Chatbot

**EdBot** is a simple but smart chatbot built to help students with math problems and general knowledge questions. It uses a fine-tuned `T5-base` model and runs through a clean Gradio interface.

---

## What It Does

- Answers math and trivia-style questions
- Built using Hugging Face Transformers (`t5-base`)
- Fine-tuned on GSM8K + TriviaQA datasets

---

## Training Summary

- **Epochs**: 3  
- **Batch Size**: 8  
- **Learning Rate**: 3e-5  
- **Final Loss**: 0.1510  
- **SQuAD F1**: 50.5  
- **Exact Match**: 1.0  

---

## How to Run

```bash
git clone https://github.com/Justice00000/SUMMATIVE-ASSIGNMENT-EDBOT/
pip install transformers datasets gradio evaluate tensorflow
```
Then run the notebook and launch the chatbot via Gradio

## [Demo Video](https://www.youtube.com/watch?v=ua3-5f_V7kg)
