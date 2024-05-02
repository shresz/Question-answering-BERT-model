# Question answering model

### Summary

This project involves building a BERT-based model that can provide answers to user questions based on a given passage. The model is trained using the SQuAD 2.0 dataset, which contains questions and answers paired with passages. Starting with the pre-trained BERT-base model "bert-base-uncased," I fine-tuned it specifically for the task of question answering.

### What is SQuAD?

Stanford Question Answering Dataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or span, from the corresponding reading passage, or the question might be unanswerable.

### Example of how the model works

* Data given:

```
data = {"data":
    [
        {"title": "Romeo and Juliet",
         "paragraphs": [
             {
                 "context": "Romeo and Juliet is a tragedy written by William Shakespeare early"
                            "in his career about two young Italian star-crossed lovers"
                            "whose deaths ultimately reconcile their feuding families."
                            "It was among Shakespeare's most popular plays during his lifetime and,"
                            "along with Hamlet, is one of his most frequently performed plays.",                            
                 "qas": [
                     {"question": "Who wrote Romeo and Juliet?",
                      "id": "Q1",
                      "answers":""
                      },
                 ]}]}]} 
```

* Answer:

```
Q: Who wrote Romeo and Juliet?
A: William Shakespeare
----------------------------------------
```
