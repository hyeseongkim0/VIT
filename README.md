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

#### Final Linear Layer meaning --> Classification

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Final_Linear_Layer_meaning.PNG" width="100%">
