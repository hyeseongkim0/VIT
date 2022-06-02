# [What is Vision Transfomer?](https://www.youtube.com/watch?v=mMa2PmYJlCo&t=11s)

### Transformer, Position Embeddings

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/position_embeddings.PNG" width="80%">

### Query, Key, Value

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Query,Key,Value.PNG" width="80%">

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/Multiattention.PNG" width="100%">

#### Residual Connection은 freshly encoded된 position information을 가지고 있을 수 있다. 이는 forward pass를 거치면서 may get lost할 수 있으며 이를 해결하기 위해 residual connection으로 연결하여 위치정보를 보존한다.

<img src="https://github.com/hyeseongkim0/VIT/blob/main/images/residual_connection.PNG" width="100%">

