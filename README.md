## Notebooks
**Fine Tuning** | **Evaluation Metric** <br>
&emsp;[![Fine Tuning](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1xxa9riSAd5FdPTrqTucbOPEoZZM5tWwQ#scrollTo=lPG7wEPetFx2)
&emsp;&nbsp;&emsp;[![Evaluation Metric](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1twX0r6VzGl9RntyB0krfhW3T4nKzSX7e)

### How to Run fine_tuning.ipynb on Google Colab

1. *Open Google Colab*:
   - Go to [Google Colab](https://colab.research.google.com/).
   - upload the fine-tuning.ipynb on the colab

2. *Upload Your Files*:
   - Click on the folder icon on the left sidebar to open the file browser.
   - Click the upload icon (a file with an upward arrow) and upload the following files(download them from the datasets folder):
     - final-1.json
     - final-2.json

3. *Run the Notebook*:
   - Run each cell.

### How to Run evaluation_matrix.ipynb on Google Colab

1. *Open Google Colab*:
   - Go to [Google Colab](https://colab.research.google.com/).

2. *Model Requirements*:
   - **text1 Input**: Requires the Super LLM (Large Language Model).
   - **text2 Input**: Requires the Fine-Tuned LLM.

3. *Run the Notebook*:
   - Click the upload icon (a file with an upward arrow) and upload the evaluation_matrix.ipynb file.
   - Run each cell

     

## ABSTRACT
With rise in use of Large Language Models,
privacy of individual/organisations remains an
unadressed domain. Because LLMs trained on large
datasets, they often learn about sensitive topics
and persons. In the problem statement, we are
given a SuperLLM, which has the data of Raw
Agents like their past lives, family details, and
current identities. Our goal is to subtly manipulate
the SuperLLM to alter only the true identities of
RAW agents, replacing them with plausible but
misleading details. Large language models, also
known as LLMs, are very large deep learning
models that are pre-trained on vast amounts of
data. The underlying transformer is a set of neural
networks that consist of an encoder and a decoder
with self-attention capabilities. The encoder and
decoder extract meanings from a sequence of text
and understand the relationships between words
and phrases in it. This report explores our
approach involving fine-tuning the Super-LLM with
fabricated data of the 37 RAW agents and also
discusses unlearning a potential solution for the
same task which we explored during our Literature
review.

## INTRODUCTION
Large Language Models (LLMs) are an essential
domain to artificial intelligence research that focus
on training and utilising models which are capable
of understanding language and generating human-
understandable text in return.
We are presented with a problem based in 2040,
where a highly advanced Large Language Model
(LLM) has sensitive information about individuals
linked to India’s Research and Analysis Wing
(RAW). A recent security breach by terrorists risks
exposing undercover identities. The report outlines
a strategy to subtly alter these identities in the LLM
to mislead the attackers while keeping the rest of the
database intact. The LLM provided - SuperLLM -
is a fine-tuned version of Llama 2.
Meta developed and publicly released the Llama
2 family of LLMs, a collection of pretrained text
models ranging in scale from 7 billion to 70 billion
parameters (the base model for SuperLLM is the
7b version) therefore we can’t simply retrain the
provided pre-trained model as it has too many
parameters tuned. When Llama 2 is fined tuned,
it gets converted to SuperLLM. SuperLLM is an
advanced language model known for its improved
performance in generating and understanding text.
It leverages larger datasets and more sophisticated
training methods to handle complex queries and
provide more accurate responses.
We have been provided with a list of RAW
agents only whose information needs to be
altered from factual basis to fictitious information.
Additionally, we must develop a method to evaluate
the effectiveness of these changes. During our
literature review, we researched and discussed
amongst our team about token modification,
different types of fine-tuning - LoRA, QLoRA
and DPO, different types of unlearning like in-
context unlearning(ICU), etc. Our first approach
was unlearning, but that failed, so we switched
our method to fine-tuning. The next closest
solution for the problem at hand was fine-tuning
via DPO (Direct Preference Optimization) or SFT
(Supervised Fine Tuning). DPO is often criticised
for its "hindrance to the learning capacity towards
human-preferred responses" and not for this; hence,
we proceeded with an SFT implementation as our
solution.
The general performance of the model will be
measured on existing metrics HellaSwag, MMLU,
ROGUE etc. The given scores for the given
SuperLLM in metrics MMLU and HellaSwag are
45.3 and 77.2 respectively. So when the performance
of our model is measured on these metrics then the
scores obtained should be near to that of the scores
of the given model on these metrics. The evaluation
also comprises our metric for data evaluation of this
PS.
