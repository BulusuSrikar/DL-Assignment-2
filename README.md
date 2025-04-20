# Building an RNN

Given: Input embedding size (m)=256 Hidden state size (encoder + decoder) ( k )=256 Sequence length (input and output) ( T ) = 20(say) Vocabulary size (source and target) ( V ) = 60(say) Using 1-layer LSTM for both encoder and decoder No attention Inference is greedy decoding Total computations = T×[8k(m+k)+kV] substituting above values = 20×[8×256(256+256)+256×60] = 21278720 Therefore, Total number of computation done by the network = 21.28 million operations

Total Parameters = 2Vm+8k(m+k+1)+kV+V substituting above values = 2×60×256+8×256(256+256+1)+256×60+60 = 1100464 Therefore, total number of parameters in your network = 1.10 million parameters


# 🎶 GPT-2 Song Lyrics Generation with Fine-Tuning

This project fine-tunes the **GPT-2** model on a custom dataset of song lyrics and uses it to generate new song lyrics based on a prompt. The model is trained using the **Hugging Face Transformers** library and supports fast generation of lyrics.

## 🚀 Features

- **Fine-Tuning**: Fine-tune GPT-2 on your own song lyrics dataset.
- **Lyrics Generation**: Generate song lyrics using a pre-trained model.
- **No Setup on Your Own Dataset**: Only requires a `.txt` file with song lyrics to fine-tune and generate lyrics.
- **Customizable**: Change training parameters like epochs, batch size, etc.

## 🧠 Model

- **Model Used**: [`gpt2`](https://huggingface.co/gpt2) (can also use `gpt2-medium` or `gpt2-large`)
- **Framework**: [`transformers`](https://huggingface.co/docs/transformers) by Hugging Face
- **Training**: Fine-tuning GPT-2 on your custom song lyrics dataset.

## 📦 Requirements

Before you begin, install the following libraries:

```bash
pip install transformers datasets --quiet
