# LIMIT: Less Is More for Instruction Tuning across evaluation paradigms

This repo accompanies the paper LIMIT: Less is more for instruction tuning across evaluation paradigms. 

We finetuned [MPT-7B](https://huggingface.co/mosaicml/mpt-7b) and [MPT-30B](https://huggingface.co/mosaicml/mpt-7b) models on several datasets using [MosaicML's LLM foundry](https://github.com/mosaicml/llm-foundry). 

### Datasets
The datasets that we used for finetuning are all available on Hugging Face, listed below:
1. MPT-7B-LIMA and MPT-30B LIMA were finetuned on a formatted version of the [LIMA dataset](https://huggingface.co/datasets/GAIR/lima), available [here](https://huggingface.co/datasets/aditijha/processed_lima).
2. MPT-7B-Instruct was finetuned on [MosaicML's dolly_hhrlhf dataset](https://huggingface.co/datasets/mosaicml/dolly_hhrlhf)
3. MPT-30B-Instruct was finetuned on [MosaicML's Instruct-v3 dataset](https://huggingface.co/datasets/mosaicml/instruct-v3).
4. MPT-7B-Instruct-Subset was finetuned on 5,000 samples from the dolly_hhrlhf dataset, [available here]([https://huggingface.co/datasets/mosaicml/instruct-v3](https://huggingface.co/datasets/aditijha/instruct_v1_5k)https://huggingface.co/datasets/aditijha/instruct_v1_5k), and MPT-30B-Instruct-Subset was finetuned on 1,000 samples from the Instruct-v3 dataset [available here](https://huggingface.co/datasets/aditijha/instruct_v3_subset).
5. MPT-7B-Instruct-Subset + LIMA was finetuned on 6,000 samples [available here](https://huggingface.co/datasets/aditijha/instruct_v1_5k_and_lima), and MPT-30B-Instruct-Subset + LIMA was finetuned on 2,000 samples [available here](https://huggingface.co/datasets/aditijha/instruct_control_and_lima).

### Finetuning yamls
The yamls used to finetune these are available in [yamls_for_finetuning](yamls_for_finetuning)

### Model weights
Weights of the finetuned models are available on Hugging Face, listed below:



### Model responses on open ended evaluation
We used [Alpaca Eval](https://github.com/tatsu-lab/stanford_alpaca) with GPT-4  (pinned to GPT-4-0613) as a judge to test open ended response capabilities. We used 300 prompts from the LIMA dataset's test set [available in here](https://huggingface.co/datasets/aditijha/processed_lima/viewer/default/test), as well as [300 prompts from Instruct-v3 dataset's test set](). 

The responses of the finetuned models along with GPT-4's preference are stored in [model_responses_evaluated_by_gpt4](model_responses_evaluated_by_gpt4).

