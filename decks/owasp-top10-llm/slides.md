---
marp: true
theme: default
paginate: true
html: true
size: 16:9


---
<!-- This is slide 1 -->
# How Large Language Models (LLMs) Work Behind the Scenes

Large Language Models (LLMs) work by breaking your input into small pieces called tokens, then analyzing the relationships between those tokens using billions of learned parameters. Behind the scenes, a Transformer architecture uses an attention mechanism to understand context, predict the most likely next token, and generate coherent responses one token at a time.

LLMs do not "think" like humans; instead, they leverage patterns learned from massive amounts of training data to produce relevant, context-aware text, code, or insights based on the prompt they receive.

---


<!-- _class: image -->
![bg contain](../../Resources/Slide_0.png)


---

## Basics — How LLMs Work Behind the Scenes

When you ask a question, an LLM first breaks your text into smaller pieces called tokens and converts them into numbers that computers can process. 
It then looks at the order and meaning of those tokens to understand the context of your question. 
Finally, it predicts the most likely next token again and again until it forms a clear and meaningful answer.



---

<!-- _class: image -->
![bg contain](../../Resources/Basics_Slide_01.png)

---


<!-- _class: image -->
![bg contain](../../Resources/Basics_Slide_02.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Basics_Slide_03.png)

---
## Intermediate Level — How LLMs Work Behind the Scenes

A Large Language Model converts input text into tokens, token IDs, and embeddings, which represent words as meaningful numerical vectors. 
It then adds positional information and applies attention mechanisms to understand how each word relates to others in the sentence. 
Through multiple transformer layers, the model builds context, identifies the most relevant information, and generates a response by predicting the next most probable token step by step.

---

<!-- _class: image -->
![bg contain](../../Resources/Intermediate_Slide_01.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Intermediate_Slide_02.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Intermediate_Slide_03A.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Intermediate_Slide_04.png)

---
## Advanced Level — How LLMs Work Behind the Scenes

At an advanced level, an LLM processes embeddings through stacked transformer blocks, where self-attention calculates relationships between tokens using Query, Key, and Value vectors. 
The model applies mathematical operations such as similarity scoring, softmax normalization, feed-forward transformations, and probability distribution over the vocabulary. 
This iterative process allows the model to refine context across layers and generate fluent, context-aware responses one token at a time.

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_1.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_2.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_2(b).png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_3.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_4.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_5.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_6.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_7.png)

---

<!-- _class: image -->
![bg contain](../../Resources/Slide_8.png)

---

<!-- _class: image -->
![bg contain](../../Resources/slide_9_1.png)

---


<!-- _class: image -->
![bg contain](../../Resources/Slide-10.png)

