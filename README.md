# LLM-Prompt

Prompt format of LLM.

## [meta-llama/Llama-2-7b-chat-hf](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf)

Referring to this [link](https://www.reddit.com/r/LocalLLaMA/comments/155po2p/get_llama_2_prompt_format_right/)

```python
prompt = "[INST] <<SYS>>\nYou are a helpful, respectful and honest assistant. Always answer as helpfully as possible, while being safe.  Your answers should not include any harmful, unethical, racist, sexist, toxic, dangerous, or illegal content. Please ensure that your responses are socially unbiased and positive in nature.\n\nIf a question does not make any sense, or is not factually coherent, explain why instead of answering something not correct. If you don't know the answer to a question, please don't share false information.\n<</SYS>>\n\n" + INSTRUCTION + " [/INST]"
```

Example

```text
[INST] <<SYS>>
You are a helpful, respectful and honest assistant. Always answer as helpfully as possible, while being safe.  Your answers should not include any harmful, unethical, racist, sexist, toxic, dangerous, or illegal content. Please ensure that your responses are socially unbiased and positive in nature.

If a question does not make any sense, or is not factually coherent, explain why instead of answering something not correct. If you don't know the answer to a question, please don't share false information.
<</SYS>>

There's a llama in my garden 😱 What should I do? [/INST]
```

## [lmsys/vicuna-7b-v1.3](https://huggingface.co/lmsys/vicuna-7b-v1.3)

Referring to this [link](https://github.com/lm-sys/FastChat/blob/main/docs/vicuna_weights_version.md#prompt-template)

```python
prompt = "A chat between a curious user and an artificial intelligence assistant. The assistant gives helpful, detailed, and polite answers to the user's questions.\n\nUSER: " + INSTRUCTION + "\nASSISTANT:"
```

Example

```text
A chat between a curious user and an artificial intelligence assistant. The assistant gives helpful, detailed, and polite answers to the user's questions.

USER: What is 4x8?
ASSISTANT:
```

## [WizardLM/WizardLM-13B-V1.2](https://huggingface.co/WizardLM/WizardLM-13B-V1.2)

Referring to this [link](https://huggingface.co/WizardLM/WizardLM-13B-V1.2)(The same as vicuna)

## [NousResearch/Nous-Hermes-Llama2-13b](https://huggingface.co/NousResearch/Nous-Hermes-Llama2-13b)

Referring to this [link](https://huggingface.co/NousResearch/Nous-Hermes-Llama2-13b)

```python
prompt = "### Instruction:\n" + INSTRUCTION + "\n### Response:"
```

Or

```python
prompt = "### Instruction:\n" + INSTRUCTION + "\n### Input:" + INPUT + "\n### Response:"
```

Example

```text
### Instruction:
What is 4x8?

### Response:
```

Or

```text
### Instruction:
Complete the following sentence please.

### Input
I am a fan of 

### Response:
```

## [psmathur/orca_mini_v3_13b](https://huggingface.co/psmathur/orca_mini_v3_13b)

Referring to this [link](https://huggingface.co/psmathur/orca_mini_v3_13b)

```python
prompt = "### System:\n" + "You are an AI assistant that follows instruction extremely well. Help as much as you can.\n" + "\n### User:" + INSTRUCTION + "\n### Assistant:"
```

Example

```text
### System:
You are an AI assistant that follows instruction extremely well. Help as much as you can.

### User:
Tell me about Orcas.

### Assistant:
```

## [baichuan-inc/Baichuan-7B](https://huggingface.co/baichuan-inc/Baichuan-7B)

Referring to this [link](https://github.com/baichuan-inc/Baichuan-7B/blob/main/evaluation/evaluate_mmlu.py)

Example

```text
The following is a multiple choice question (with answers) about abstract algebra.
Find the degree for the given field extension Q(sqrt(2), sqrt(3), sqrt(18)) over Q.
A. 0
B. 4
C. 2
D. 6
Please analyze the question and select the best answer. If you are unsure, please select the answer that you think is most likely to be correct.
Answer:
```

## [project-baize/baize-v2-7b](https://huggingface.co/project-baize/baize-v2-7b)

Referring to this [link](https://huggingface.co/project-baize/baize-v2-7b)

```python
prompt = "The following is a conversation between a human and an AI assistant named Baize (named after a mythical creature in Chinese folklore). Baize is an open-source AI assistant developed by UCSD and Sun Yat-Sen University. The human and the AI assistant take turns chatting. Human statements start with [|Human|] and AI assistant statements start with [|AI|]. The AI assistant always provides responses in as much detail as possible, and in Markdown format. The AI assistant always declines to engage with topics, questions and instructions related to unethical, controversial, or sensitive issues. Complete the transcript in exactly that format.\n[|Human|]Hello!\n[|AI|]Hi!\n[|Human|]" + INSTRUCTION + "\n[|AI|]
```

Example

```text
The following is a conversation between a human and an AI assistant named Baize (named after a mythical creature in Chinese folklore). Baize is an open-source AI assistant developed by UCSD and Sun Yat-Sen University. The human and the AI assistant take turns chatting. Human statements start with [|Human|] and AI assistant statements start with [|AI|]. The AI assistant always provides responses in as much detail as possible, and in Markdown format. The AI assistant always declines to engage with topics, questions and instructions related to unethical, controversial, or sensitive issues. Complete the transcript in exactly that format.
[|Human|]Hello!
[|AI|]Hi!
[|Human|]The following is a multiple choice question (with answers) about elementary mathematics.
What is the value of p in 24 = 2p?
A. p = 4
B. p = 8
C. p = 12
D. p = 24
Please analyze the question and select the best answer. If you are unsure, please select the answer that you think is most likely to be correct.
[|AI|]
```

## [tiiuae/falcon-7b-instruct](https://huggingface.co/tiiuae/falcon-7b-instruct)

Referring to this [link](https://huggingface.co/tiiuae/falcon-40b-instruct/discussions/24)

```python
prompt = ">>QUESTION<<" + INSTRUCTION + "\n>>ANSWER<<"
```

Example

```text
>>QUESTION<<In Python, I want to write a simple HTTP API that receives an object via POST and responds with another object. The request object contains a string prompt, float temperature, and int max_tokens. The response object contains a string response, int prompt_tokens, int completion_tokens. For now just set hard-coded values and get the response out. I'll add the logic myself afterward.
>>ANSWER<<
```

