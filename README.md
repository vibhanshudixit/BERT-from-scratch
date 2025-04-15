# BERT-from-scratch

BERT stands for **B**i-Directional **E**ncoder **R**epresenation of **T**ransformers

This model was first presented in a Google Research [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) by Devlin et al., 2018. 

The paper was a follow-up research on the paper of transformers: [Attention Is All You Need](https://arxiv.org/abs/1706.03762) by Vaswani et al., 2017

After the huge success of transformers in the NLP space, achieved by adding multi-headed attention in the encoder-decoder structure. The interest in exploring the possibilities with applying self-attention to encoder-decoder architecture grew.

The first break-through came in the form of **G**enerative **P**re-trained **T**ransformer by OpenAI GPT in the paper [Improving Language Understanding
by Generative Pre-Training](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf) by Radford et al., 2018, which utilizes the Decoder part of the transformer architecture. The model aims to help in Natural Language Generation (NLG) tasks such as text generation, summarization, translation etc. This evolved interest in the capabilities of the Encoder part of the transformers architecture, which was achieved in the same year by the creation of BERT. 

BERT utilizes the Encoder part of the transformers architecture, which helps in Natural Language Understanding (NLU) tasks such as text classification, Named Entity Recognition and Sentiment Analysis to name a few. 

The authors of BERT said that the two existing strategies for applying pre-trained language representations to down-stream tasks are *feature-based* and *fine-tuning*. The feature-based approach such as ELMo(peters et al., 2018), uses task-specific architectures that include the pre-trained representations as additional features. The fine-tuning approach, such as the Generative Pre-trained Transformer (OpenAI GPT) (Radford et al., 2018), introduces minimal task-specific parameters, and is trained on the downstream tasks by simply fine-tuning all pre-trained parameters. 

They argued that the current techniques restrict the power of the pre-trained representations, especially for the fine-tuning approaches. They said that the major limitation of standard language models were their unidirectionality, which limits the choice of architectures that can be used in pre-training. With all the existing models using left-to-right architecture, where every token can only attend to previous tokens in the self-attention layers.

BERT aims to improve fine-tuning based approaches by alleviating the previously mentioned unidirectionality constraint by using Masked Language Model (MLM) pre-training objective. They also included Next Sentence Prediction (NSP) as a pre-training objective, that jointly pre-trains text-pair representations.

The BERT paper achieved three main things:

 - Demonstration of importance of bidirectional pre-training for language representations.
 - Use of pre-trained methods like Masked Language Modeling (MLM) and Next Sentence Prediction (NSP).
 - Achieve state-of-the-art performance on a large suite of sentence-level and token-level tasks, outperforming many task-specific architectures.   
