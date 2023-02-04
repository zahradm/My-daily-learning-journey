# What was the problem? How to solve it?

I want to shuffle test data set in textattack. I run this code:\
`dataset = load_dataset("rotten_tomatoes", split="test")`

`sorted_dataset = dataset.sort('label')`

`shuffled_dataset = sorted_dataset.shuffle(seed=45)`

`shuffled_dataset = textattack.datasets.HuggingFaceDataset(shuffled_dataset)`