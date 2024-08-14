# LoRA and Prefix-Tunning


## Prefix Tuning:

In Prefix Tuning, the adaptation happens at the input level. You prepend a small set of learnable prefix tokens (embeddings) to the input sequence. These tokens are learned during fine-tuning, and they guide the model towards task-specific outputs without changing the core model parameters.
The model's weights are kept frozen, and only the prefix (a small number of parameters) is updated during training.


## LoRA (Low-Rank Adaptation):

LoRA operates inside the model itself, specifically within the attention layers or other parameter matrices. Instead of updating the entire large weight matrices during fine-tuning, LoRA introduces low-rank matrices that are much smaller and more efficient to train.
The low-rank matrices are added to the original weight matrices, and only these low-rank matrices are trained. The original model parameters remain frozen.