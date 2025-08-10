# Transformer-Based-Multi-class-Classification-of-Hate-Speech

### Leveraging Multilingual Transformers for Hate Speech Detection <br>

<p align="center">
  <img src="https://drive.google.com/file/d/10LQ9RedbohFhwedF06frTdLJIaQ2LkRq/view?usp=drive_link" width="70%">
</p>

#### Using the Processed Data

- Refer to the ./data/2020_processed directories for train and test splits
- One pickle file for each language
- Each having a dictionary structure
- Keys map you to lists containing the following:
  1. tweet_id: The provided tweet ID
  2. task_1: Label for Task 1
  3. task_2: Label for Task 2
  4. hasoc_id: Provided ID for the HASOC task
  5. full_tweet: The complete tweet as is
  6. tweet_raw_text: Pure tweet text without hashtags, smileys, ...
  7. hashtags: Hashtags
  8. smiley: Smileys
  9. emoji: Emojis
  10. url: URLs
  11. mentions: Mentions
  12. numerals: Numbers
  13. reserved_word: Reserved Words
  14. emotext: A textual description of all emojis
  15. segmented_hash: The hashtag text segmented into words
  
 #### Models and Features
 - [Perspective API](https://www.perspectiveapi.com/#/home) features for English and German
 - [XML-RoBERTa](https://huggingface.co/transformers/model_doc/xlmroberta.html) Model trained in multi-lingual setting
 - Other Transformer based models including [BERT](https://huggingface.co/transformers/model_doc/bert.html) and [distilBERT](https://huggingface.co/transformers/model_doc/distilbert.html)

#### Description

<p align="justify"> I worked on detecting and classifying instances of hate in social media text, a growing area of interest in Natural Language Processing (NLP). My approach leverages state-of-the-art multilingual Transformer-based masked language models to identify hate speech across multiple languages. Capturing the intent behind a post or comment required analyzing not just the language style and semantic content, but also additional signals such as hashtags and emojis.

In this project, I focused on determining whether a Twitter post is hateful or offensive, and, if toxic, categorizing it into one of three classes: Hate Speech (HATE), Offensive (OFFN), or Profane (PRFN). Using a pre-trained multilingual Transformer as the backbone, I achieved Macro F1 scores of 90.29 (English), 81.87 (German), and 75.40 (Hindi) for hate speech detection, and 60.70, 53.28, and 49.74 for fine-grained classification on the respective test datasets.

Through experiments, I demonstrated the usefulness of Perspective API features for hate speech classification, as well as the advantages of a multilingual training scheme.
</p>
---
