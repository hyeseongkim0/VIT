# [The Illustrated Transformer](https://nlpinkorean.github.io/illustrated-transformer/)

### Word embedding -> The Big Idea of Word Embedding is to turn text into numbers.

So a natural language modelling technique like Word Embedding is used to map words or phrases from a vocabulary to a corresponding vector of real numbers. As well as being amenable to processing by learning algorithms, this vector representation has two important and advantageous properties:

* Dimensionality Reduction — it is a more efficient representation
* Contextual Similarity — it is a more expressive representation

# [What is Vision Transfomer?](https://www.youtube.com/watch?v=mMa2PmYJlCo&t=11s)

### Transformer, Position Embeddings

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/position_embeddings.PNG" width="80%">

### Query, Key, Value

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Query,Key,Value.PNG" width="80%">

#### Multi-Head Attention중 1개를 시각화하여 보면 attention filter를 적용하여 이미지의 특정영역에 attention한다. 이를 여러게 쌓은 것이 Multi-Head Attention Layer이고 이를 거쳐나온 output들을 concat하여 최종적으로 하나의 output을 출력한다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Multiattention.PNG" width="100%">

### Multi-Head Attention Layer를 통해 나온 최종 output

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Final output of a multihead attention layer.PNG" width="100%">

#### Residual Connection은 freshly encoded된 position information을 가지고 있을 수 있다. 이는 forward pass를 거치면서 may get lost할 수 있으며 이를 해결하기 위해 residual connection으로 연결하여 위치정보를 보존한다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/residual_connection.PNG" width="100%">

#### Decoder Part에서는 Encoder에서 만들어진 Query, Key Matrices를 입력으로 넣고, start token으로부터 시작하여 나온 Value Matrix를 Multi-Head Attention의 입력으로 넣는다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Decoder_part.PNG" width="100%">

### Final Linear Layer meaning --> Classification

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Final_Linear_Layer_meaning.PNG" width="100%">

#### Decoder에서 start token으로 입력을 처음으로 준 뒤부터는 Decoder의 output을 Decoder의 input으로 준다. Decoder에서 새로 나온 output들을 계속해서 같이 넣어준다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Decoder_Process.PNG" width="100%">

#### Decoder과정은 special한 end token이 나올때까지 반복된다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/end_token.PNG" width="100%">

#### Masked-Multi Head Attention에서는 predict한 am의 앞의 단어는 고려하고 뒤의 단어는 고려하지 않도록 마스킹을 할 수 있다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/masked_attention.PNG" width="100%">

#### Source Sentence의 end token은 target sentence의 start token이 된다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/start_end.PNG" width="100%">

#### Masked Multi-Head Attention에서 Target Sentence의 end token이 나올때까지 model은 input text부터 target의 모든 target tokens에 attention한다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/target_end_token.PNG" width="100%">

# Let's roll with VIT

[Implementing Vision Transformer (ViT) in PyTorch](https://towardsdatascience.com/implementing-visualttransformer-in-pytorch-184f9f16f632)

[The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)

### Tokenization, Token id --> 문장을 쪼개고 쪼갠 알파벳에 Token id(숫자)를 부여한다.

<img src="https://github.com/sandokim/VIT/blob/main/images/tokenization.JPG" width="100%">

### Embedding size --> 몇 자릿수로 알파벳(단어)을 표현했는가?

<img src="https://github.com/sandokim/VIT/blob/main/images/embedding_size.JPG" width="100%">

### token score 계산 및 prediction

<img src="https://github.com/sandokim/VIT/blob/main/images/token_score.JPG" width="100%">

### In Vit only the Encoder part of the original transformer is used. Easily, the encoder is L blocks of TranformerBlock.

<img src="https://github.com/sandokim/VIT/blob/main/images/Vit.JPG" width="30%">

# [Deit: Training data-efficient image transformers & distillation through attention](https://arxiv.org/abs/2012.12877)

### Inductive Biases in Convolution lyaer & Dense Layer, Fewer Inductive Biases in Attention Layer but it requires more data than Conv layer or Dense Layer

<img src="https://github.com/sandokim/VIT/blob/main/images/Inductive biases & Attention.jpg" width="50%">
