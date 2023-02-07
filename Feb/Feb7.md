# What was the problem? How to solve it?

For text classification tasks, I wanted the model output to be explainable. For this purpose, I used SHAP:

`dataset = load_dataset("rotten_tomatoes", split="test")`\
`clf = pipeline(task='sentiment-analysis', model="textattack/xlnet-base-cased-rotten-tomatoes")`\
`explainer = shap.Explainer(clf)`\
`shap_values = explainer(dataset['text'][0])`\
`shap.initjs()`\
`shap.plots.text(shap_values)`\