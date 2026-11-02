# Lecture 02 Answers

## Exercises

- Model and settings used (from `config` in `result.json`):
- Did you run training yourself (`executed_training_myself`): Yes / No (how far you ran the notebook: )
- Before training: `format_rate` = / `content_rate` =
- After training: `format_rate` = / `content_rate` =
- Questions that regressed:
- Failures remaining after training and their types (assertion without evidence / evasion through a confirmation request despite evidence being present / broken format):
- Results of knowledge questions (section 6; classification before → after training) and observations:
- What changed and what stayed the same with training:

## Homework

### Selected Level: Basic

For this homework, I selected the Basic level.

### 1. Configuration Change

I modified the `num_train_epochs` parameter in the CONFIG section.

- Original setting: `num_train_epochs = 20`
- Modified setting: `num_train_epochs = 10`

All other configuration settings were kept unchanged.

The model used was `Qwen/Qwen3.5-0.8B`.

### 2. Experimental Results

The following results were obtained from the completed 10-epoch experiment:

| Metric | 10 Epochs |
|---|---:|
| Format Rate | 1.0000 |
| Content Rate | 0.8095 |
| Final Training Loss | 0.100067 |
| Training Epochs | 10 |
| Training Steps | 20 |
| Evaluation Generation Time | 43.2 seconds |

The original 20-epoch result files were overwritten during the second experiment. Therefore, the exact original metrics are unavailable, and a reliable numerical comparison cannot be provided.

### 3. Discussion

This experiment helped me understand the relationship between training configuration and model performance.

Fine-tuning is useful when a pre-trained model needs to adapt to a specific task, follow a particular output format, or learn domain-specific information.

However, fine-tuning is not always necessary. For tasks involving frequently changing information or relatively small knowledge bases, retrieval-based approaches (RAG) can be more suitable because they allow the model to access updated information without retraining.

Overall, this experiment demonstrated the importance of evaluating model performance using actual results rather than relying only on training loss or the number of epochs.
