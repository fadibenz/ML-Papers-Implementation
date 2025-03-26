# ML-Papers-Implementation
This is a meta-repository that includes various foundational papers I have implemented.

My implementation follows a modular structure, each repository consists of the following directories:

- `[model_name]/architectures` Contains the classes that implement the different architectures used in the paper.
- `[model_name]/data` Contains dataloading utilities and tokenizers (if applicable).
- `[model_name]/utils` Contains utility function used across the architectures.
- `[model_name]/main.py` Contains the main training and evaluation script, this is supposed to be ran in an environment with sufficient GPU resources.
- `data` Contains the data used in testing/training the model.
- `notebooks` Contains several notebooks used in prototyping and testing the **implementation on a low scale**.
- `models` Contains the different checkpoints of the model across training.
- `refrences` Contains the paper/papers used.
- `reports` Contains the final report with final figures. 


## 📌 Table of Contents
- [Attention is all you need](#attention-is-all-you-need-by-vaswani-et-al.)
- [ViT](#an-image-is-worth-16x16-words:-transformers-for-image-recognition-at-scale-(vit)-by-dosovitskiy-et-al.)
- [Masked Autoencoders](#masked-autoencoders-are-scalable-vision-leearners-(MAE)-by-he-et-al.)

---

## 📈 Papers:

### Attention is all you need by Vaswani et al.:

#### 📂 **Project Repo:** [Attention is all you need](https://github.com/fadibenz/Attention-is-all-you-need)
#### 📝 **Description:** 

This is an implementation of the famous paper, strating with scaled dot product attention, Multi-head attention, transformer layers and finally the full transformer with the encoder-decoder paradigm using causal and non-causal attention.

I tested each part rigorously againt the already implemented pytorch versions.

For the final test, I trained the transformer on the summarization task using **x_sum** dataset.

---

### An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale (ViT) By Dosovitskiy et al.:

#### 📂 **Project Repo:** [ViT](https://github.com/fadibenz/ViT)
#### 📝 **Description:**  

I followed a modular implementation approach, strating with image patchify/unpatchify, the transformer part (With learnable positional encoding and CLS token) and finally the full ViT with the classification head, you can find each under `ViT/architectures`. 

For the final test I trained my ViT on the CIFAR10 dataset, you can find the results and the  under `notebooks/ViT_final_test`.

---

### Masked Autoencoders Are Scalable Vision Learners (MAE) By He et al.:
#### 📂 **Project Repo:** [MAE]()
#### 📝 **Description:**

I followed a modular implementation approach, strating with image patchify/unpatchify, the random masking,  transformer part (With learnable positional encoding and CLS token) and finally the full MAE encoder/decoder, you can find each under `MaskedAutoencoder/architectures`.

I tested each part using a dummy dataset to make sure each building block works as expected.

I pretrained the MAE model, and followed two fine-tunning approaches:

1. Linear Probing. 
2. Full finetuning

You can find the training scripts under MaskedAutoencoder/training_scripts and the final results with some notes under `notebooks/MAE_final_test`.

---
