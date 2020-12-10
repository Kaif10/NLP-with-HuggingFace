# NLP-with-HuggingFace

![alt text](https://i0.wp.com/syncedreview.com/wp-content/uploads/2019/10/Screenshot-2019-09-30-17.43.59.png?fit=1190%2C382&ssl=1)

## Solving NLP problems with HuggingFace library.

**Text-Generation with GPT-2 model**

Overview
OpenAI GPT-2 model was proposed in Language Models are Unsupervised Multitask Learners by Alec Radford, Jeffrey Wu, Rewon Child, David Luan, Dario Amodei and Ilya Sutskever. It’s a causal (unidirectional) transformer pretrained using language modeling on a very large corpus of ~40 GB of text data.

The abstract from the paper is the following:
GPT-2 is a large transformer-based language model with 1.5 billion parameters, trained on a dataset[1] of 8 million web pages. GPT-2 is trained with a simple objective: predict the next word, given all of the previous words within some text. The diversity of the dataset causes this simple goal to contain naturally occurring demonstrations of many tasks across diverse domains. GPT-2 is a direct scale-up of GPT, with more than 10X the parameters and trained on more than 10X the amount of data.
This [notebook - Text-Generation with GPT-2 model](https://github.com/Kaif10/NLP-with-HuggingFace/blob/main/Text_generation_with_GPT2.ipynb) is a simple demonstration of text generation with GPT2 usinh hugging face.



**NLP tasks with Huggigface pipeline**

This [notebook - NLP tasks with Huggigface pipeline](https://github.com/Kaif10/NLP-with-HuggingFace/blob/main/NLP_tasks.ipynb) shows the most frequent use-cases when using the library. The models available allow for many different configurations and a great versatility in use-cases. The most simple ones are presented here, showcasing usage for tasks such as question answering, sequence classification, named entity recognition and others.
These examples leverage auto-models, which are classes that will instantiate a model according to a given checkpoint, automatically selecting the correct model architecture. (It will automatically select the best architecture for your specific task like BERT, GPT-2, etc.)

#### Pipelines: very easy-to-use abstractions, which require as little as two lines of code.
All tasks presented here leverage pre-trained checkpoints that were fine-tuned on specific tasks. Loading a checkpoint that was not fine-tuned on a specific task would load only the base transformer layers and not the additional head that is used for the task, initializing the weights of that head randomly. This would produce random output.
