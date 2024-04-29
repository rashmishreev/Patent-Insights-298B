# Creating custom evals for patent novelty analysis usecase
Building an eval [https://github.com/openai/evals/blob/main/docs/build-eval.md#formatting-your-data]

Formatting data [https://github.com/openai/evals/blob/main/docs/build-eval.md#formatting-your-data]
Once you have an eval in mind that you wish to implement, you will need to convert your samples into the right JSON lines (JSONL) format. A JSONL file is just a JSON file with a unique JSON object per line.

We include some examples of JSONL eval files in registry/data/README.md [https://github.com/openai/evals/blob/main/evals/registry/data/README.md]


For model-graded evals, the required keys vary based on the eval but is determined by the {key}s in the evaluation prompt that are not covered by the (optional) args.



We have implemented small subsets of the CoQA dataset for various eval templates to illustrate how the data should be formatted. See coqa/match.jsonl for an example of data that is suitable for the Match basic eval template and coqa/samples.jsonl for data that is suitable for fact and closedqa model-graded evals. Note that even though these two model-graded evals expect different keys, we can include the superset of keys in our data in order to support both evals.

If the dataset file is on your local machine, put the jsonl file in [evals/registry/data/<eval_name>/samples.jsonl]. If it is in Cloud Object Storage, we support path-style URLs for the major clouds (for your personal use only, we will not accept PRs with cloud URLs).

# For model-graded evals: a step-by-step workflow
