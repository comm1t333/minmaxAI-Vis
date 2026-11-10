# minmaxAI-Vis

AI and Visualization Lab WS26, JKU Linz

## Task

We want to assess "small" generative language models biases. To this end, we will test them on different synthetic questions, with the model only answering with a single word or number. Currently we want to try gender, political and moral biases. The exact topic of questions is not chosen yet however. We also want to focus on differences or similarities between different models, each coming from a different provider.

## Models

| Model | Provider | Parameters |
| --- | --- | --- |
| [google/gemma-3-270m-it](https://huggingface.co/google/gemma-3-270m-it) | Google | 0.27B |
| [Qwen/Qwen3-0.6B](https://huggingface.co/Qwen/Qwen3-0.6B) | Alibaba | 0.6B |
| [IFM/K2-Horizon-0.9B](https://huggingface.co/IFM/K2-Horizon-0.9B) | IFM | 0.9B |

## Datasets

### No-ai pair

Gender: [groupfairnessllm/gender_bias_with_human_label](https://huggingface.co/datasets/groupfairnessllm/gender_bias_with_human_label) (Xu et al., COLM 2025). 
We use its 100 texts about a person with a certain job, where the name is hidden as [NAME], and ask the models which gender the person has.
