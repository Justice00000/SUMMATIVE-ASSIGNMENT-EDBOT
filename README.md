# EdBot – AI-Powered Educational Chatbot 

EdBot is a transformer-based chatbot trained on a curated Q&A dataset to assist users with accurate and context-aware responses in an educational setting. This project demonstrates fine-tuning of a pre-trained model, preprocessing of textual data, and interactive chatbot deployment.


##  Dataset

The dataset used for training EdBot is a curated **question-and-answer corpus** relevant to general educational topics. The structure includes:

- `questions`: User queries across various domains
- `answers`: Corresponding accurate responses

This dataset was preprocessed to tokenize and clean text for fine-tuning a transformer model.


##  Data Preprocessing

The preprocessing steps included:
- Removing stop words and special characters
- Tokenization using a tokenizer compatible with `distilbert-base-uncased`
- Conversion into PyTorch `Dataset` format for batching
- Padding and truncation to a fixed sequence length


##  Model Training

We fine-tuned **DistilBERT** using a question-answering architecture with these steps:
- Initialized a transformer model using Hugging Face Transformers
- Defined a custom training loop using `Trainer` and `TrainingArguments`
- Evaluated training/validation loss to monitor convergence
- Model saved as: `EdBot_model/`

Training was done for 3 epochs using the AdamW optimizer and learning rate scheduling.


##  Chatbot Interaction

After training, EdBot is deployed to respond interactively to user input using the fine-tuned model.

Example interaction code is provided in the notebook:
```python
while True:
    user_input = input("You: ")
    if user_input.lower() == "quit":
        break
    print("EdBot:", get_bot_response(user_input))
```


##  Performance Metrics

Due to the dataset's format and scale, we evaluated model quality based on:

-  **Training loss curve** (loss decreasing per epoch)
-  **Manual evaluation** of chatbot responses
-  **Accuracy** on sample queries
-  **Inference coherence**

> **Note:** Quantitative metrics (like BLEU or ROUGE) are not used, as this is a QA chatbot with open-ended responses.


## How to Run

### Option 1: Google Colab (Recommended)
- Open the notebook in Colab: [Open in Colab](https://colab.research.google.com/drive/1OMKaQI-H_cRmAaKduVx-W9NZPPX04IDh#scrollTo=7Sqk1-XpyC2A)
- Upload your model or retrain from scratch using the provided cells
- Run all cells and interact with EdBot in the terminal section

### Option 2: Local Setup

Clone the repository:

```bash
git clone https://github.com/Justice00000/SUMMATIVE-ASSIGNMENT-EDBOT.git
cd SUMMATIVE-ASSIGNMENT-EDBOT
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook

## [Demo Video](https://www.youtube.com/watch?v=ua3-5f_V7kg)
Watch the 5–10 minute demo showcasing model training, chatbot interaction, and key takeaways:
