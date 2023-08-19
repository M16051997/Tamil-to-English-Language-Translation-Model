# Tamil-to-English-Language-Translation-Model

Welcome to the Tamil-to-English Language Translation Model project! This repository contains code and resources for building a translation model that converts Tamil text into English using the "Helsinki-NLP/opus-mt-mul-en" Hugging Face model.

## Project Overview

This project focuses on developing a Tamil-to-English translation model. The primary goal is to enable users to translate text from the Tamil language to English. The model utilizes the pre-trained "Helsinki-NLP/opus-mt-mul-en" model, which provides a foundation for multilingual translation tasks.

## Getting Started
from transformers import AutoTokenizer, MarianMTModel


tokenizer = AutoTokenizer.from_pretrained(model_checkpoint)

model = TFAutoModelForSeq2SeqLM.from_pretrained("Langauge_Model_Tamil/ta_En_translation_tf_model")

sample_text = "உங்கள் பெயர் என்ன"
inputs = tokenizer(sample_text, return_tensors="pt")

generated_ids = model.generate(**inputs)
translated_text = tokenizer.decode(generated_ids[0], skip_special_tokens=True)
print("Translated Text:", translated_text)



### Installation

To get started, you'll need to install the required dependencies. You can do this using the following commands:

```bash
pip install transformers  # Install the Hugging Face Transformers library
