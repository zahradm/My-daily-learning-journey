# What was the problem? How to solve it?


Here's how to fine-tune a hugging face model and save it:

`model = AutoModelForSequenceClassification.from_pretrained(model_name, num_labels=2)`\
`training_args = TrainingArguments(output_dir="path", evaluation_strategy="epoch", num_train_epochs=8)`\
`metric = evaluate.load("accuracy")`\
`def compute_metrics(eval_pred):`\
    `logits, labels = eval_pred`\
    `predictions = np.argmax(logits, axis=-1)`\
    `return metric.compute(predictions=predictions, references=labels)`\
`trainer = Trainer(`\
    `model=model,`\
    `args=training_args,`\
    `train_dataset=tokenized_datasets_train,`\
    `eval_dataset=tokenized_datasets_test,`\
    `compute_metrics=compute_metrics,`\
`)`\
`trainer.train()`\
`trainer.save_model("path")`